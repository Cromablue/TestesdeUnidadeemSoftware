# Projeto de Testes de Unidade em Software

## Introdução
Os testes de software são fundamentais para garantir a qualidade e a funcionalidade de sistemas complexos. Eles ajudam a identificar falhas antes que o software chegue aos usuários finais, evitando problemas que podem causar prejuízos significativos. Neste trabalho, nosso objetivo é estudar testes de unidade, focando em uma implementação prática usando a biblioteca Google Guava. Ao longo do processo, aprendemos sobre a estrutura dos testes, as técnicas de validação e a importância de realizar testes eficazes no desenvolvimento de software.

## Código dos Testes de Unidade
Abaixo está o código dos testes de unidade que foram fornecidos. Cada método de teste será analisado em detalhes.

### Teste: `testRepeat`
```java
@Test
public void testRepeat() {
    String input = "20";
    assertEquals("", Strings.repeat(input, 0));
    assertEquals("20", Strings.repeat(input, 1));
    assertEquals("2020", Strings.repeat(input, 2));
    assertEquals("202020", Strings.repeat(input, 3));
}
```
- **Explicação do Código**:
  - `@Test`: Anotação que indica que este método é um teste de unidade.
  - `String input = "20";`: Define a string que será utilizada para os testes.
  - `assertEquals(...)`: Verifica se o valor retornado pelo método `Strings.repeat` é igual ao valor esperado.
- **Propósito**: Testar a funcionalidade do método `repeat` da biblioteca Google Guava, garantindo que ele repita a string correta um número especificado de vezes.
- **Técnicas Utilizadas**: Utilização de asserções para validar o comportamento esperado.

### Teste: `testContains`
```java
@Test
public void testContains() {
    assertFalse(Ints.contains(EMPTY, (int) 1));
    assertFalse(Ints.contains(ARRAY1, (int) 2));
    assertFalse(Ints.contains(ARRAY234, (int) 1));
    assertTrue(Ints.contains(new int[] {(int) -1}, (int) -1));
    assertTrue(Ints.contains(ARRAY234, (int) 2));
    assertTrue(Ints.contains(ARRAY234, (int) 3));
    assertTrue(Ints.contains(ARRAY234, (int) 4));
}
```
- **Explicação do Código**:
  - Verifica se determinados valores estão contidos em arrays específicos.
- **Propósito**: Validar o comportamento do método `Ints.contains` para diferentes cenários.
- **Técnicas Utilizadas**: Asserções booleanas para verificar a presença ou ausência de valores.

### Teste: `testReverse`
```java
@Test
public void testReverse() {
    testReverse(new int[] {}, new int[] {});
    testReverse(new int[] {1}, new int[] {1});
    testReverse(new int[] {1, 2}, new int[] {2, 1});
    testReverse(new int[] {3, 1, 1}, new int[] {1, 1, 3});
    testReverse(new int[] {-1, 1, -2, 2}, new int[] {2, -2, 1, -1});
}
```
- **Explicação do Código**:
  - Chamadas do método `testReverse` com diferentes arrays para validar a reversão.
- **Propósito**: Testar a funcionalidade de reversão de arrays utilizando `Ints.reverse`.
- **Técnicas Utilizadas**: Validação de igualdade de arrays.

## Simulação da Execução dos Testes
Durante a apresentação, realizaremos a execução dos testes em tempo real. Mostraremos a saída do console, destacando os resultados e discutindo qualquer falha que possa ocorrer. Utilizaremos um ambiente de desenvolvimento integrado (IDE) para facilitar a visualização e a execução.

## Apresentação de Cenários Alternativos
Vamos apresentar um novo método de teste que aborda uma funcionalidade semelhante, como a concatenação de strings. Discutiremos como essa abordagem amplia a cobertura dos testes e proporciona uma visão mais abrangente da funcionalidade do sistema.

### Novo Cenário: `testConcatenate`
```java
@Test
public void testConcatenate() {
    assertEquals("HelloWorld", Strings.nullToEmpty("Hello") + Strings.nullToEmpty("World"));
    assertEquals("Hello", Strings.nullToEmpty("Hello") + Strings.nullToEmpty(null));
}
```
- **Explicação**: Esse método verifica se a concatenação de strings funciona corretamente, mesmo lidando com valores nulos.

## Atividade Interativa com a Turma
Propomos uma atividade prática onde a turma deve criar um teste de unidade para uma função que soma dois números. Cada grupo pode discutir e implementar seu teste, permitindo que todos participem ativamente na prática de testes de unidade.

## Conclusão
Concluímos que os testes de unidade são cruciais no desenvolvimento de software moderno. Eles não apenas garantem que as funcionalidades estejam corretas, mas também promovem um código mais limpo e sustentável. Esperamos que esta apresentação tenha demonstrado a importância dos testes e que todos tenham compreendido como implementá-los efetivamente em projetos de software.

## Dicas Visuais e Estilo
- **Design Atraente**: Usaremos slides com cores vibrantes e gráficos relevantes para ilustrar os conceitos discutidos.
- **Interação**: Estimularemos perguntas e discussões durante a apresentação, criando um ambiente participativo.
- **Humor e Estilo**: Incorporaremos exemplos engraçados ou histórias pessoais relacionadas ao tema para manter o engajamento da audiência.

## Documentação
O código e a documentação estarão organizados no GitHub, com comentários explicativos e um README que guiará o professor e a turma através do projeto.
