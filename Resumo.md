# Resumo de Aulas

## Aulas

- [Aula 01 – Puts](praticando/01.rb)
- [Aula 02 – Variáveis](praticando/02.rb)
- [Aula 03 – Saída e Entrada](praticando/03.rb)
- [Aula 04 – Condicionais](praticando/04.rb)
- [Aula 05 – Operadores Relacionais e Aritméticos](praticando/05.rb)
- [Aula 06 – Estruturas de Repetição](praticando/06.rb)
- [Aula 07 – Arrays e Vetores](praticando/07.rb)

---

## Conceitos Básicos-Ruby

### Puts
[Aula 01 – Puts](praticando/01.rb)

-> Utilizado para imprimir informações na saída padrão (STDOUT).

---

### Variáveis
[Aula 02 – Variáveis](praticando/02.rb)

* Variáveis em Ruby são declaradas apenas ao serem usadas.
* O Ruby infere automaticamente o tipo da variável no momento da atribuição.

**Exemplo:**

```ruby
x = 1
y = 2.3
z = "Rails 5.x.x"
```

-> Para verificar o tipo de uma variável, utilize o método `.class`.

```ruby
a = 2
a.class # => Integer
```

---

### Entrada e Saída Padrão
[Aula 03 – Entrada e Saída](praticando/03.rb)

* **STDOUT** representa a tela (saída)
* **STDIN** representa o teclado (entrada)

```ruby
puts "Olá Mundo"
```

```ruby
puts "Qual seu nome?"
name = gets
puts "Olá " + name
puts name.inspect
```

Saída:

```
Qual seu nome?
Luan
Olá Luan
"Luan\n"
```

* `\n` representa uma quebra de linha (new line)
* O método `.chomp` remove o `\n`

```ruby
name = gets.chomp
```

---

### Coerção (Casting)

-> Transformação do tipo de um valor sem alterar a variável original.

```ruby
gets.to_i  # Integer
x = "2.5"
x.to_f     # Float
```

---

### Condicionais
[Aula 04 – Condicionais](praticando/04.rb)

* `if`
* `unless`
* `case`
* Operador ternário

---

### Operadores
[Aula 05 – Operadores Relacionais e Aritméticos](praticando/05.rb)

**Relacionais**

* Maior: `>`
* Menor: `<`
* Maior ou igual: `>=`
* Menor ou igual: `<=`
* Igual: `==`
* Diferente: `!=`

**Aritméticos**

* Soma: `+`
* Subtração: `-`
* Multiplicação: `*`
* Divisão: `/`
* Potência: `**`
* Módulo: `%`

---

### Estruturas de Repetição
[Aula 06 – Estruturas de Repetição](praticando/06.rb)

#### while

-> Executa um bloco de código enquanto uma condição for verdadeira.

```ruby
c = 1
num = 10

while c <= num
  puts "Contando... #{c}"
  c += 1
end
```

#### each

-> Iterador utilizado para percorrer coleções.

```ruby
(0..5).each do |i|
  puts "O valor lido foi: #{i}"
end
```

---

### Vetores / Array
[Aula 07 – Arrays e Vetores](praticando/07.rb)

-> Coleções ordenadas que armazenam múltiplos valores.
-> Você pode declarar/usar de duas formas:

``` ruby
a = [15, 62, 73, 48]
```
Ou 
``` ruby
a = [] ou a.Array.new
a.push(15)
a.push(62)
```
-> Para acessar, use o índice:
``` ruby
puts a.[0] # Primeiro item do array
```
---

## Comandos e Ferramentas

* [Pry](arquivos/pry.txt)
* [IRB](arquivos/IRB.txt)
* [Comandos RVM](arquivos/comandos_rvm.txt)

---

## Versões do Ruby (2.3 vs 2.4+)

### Ruby 2.3

* `Fixnum`: inteiros
* `Bignum`: inteiros muito grandes

### Ruby 2.4+

* `Integer`: unifica Fixnum e Bignum

**Exemplo:**

```ruby
w = 1_000_000
w.class # => Integer
```

Em Ruby 2.3:

```ruby
x = 1
x.class # => Fixnum

y = 1_000_000_000_000_000_000
y.class # => Bignum
```
