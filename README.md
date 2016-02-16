# java - validation
Biblioteca de validação de dados desenvolvida em Java, possibilitando vericiar se campos preenchidos possuem as informações conforme o esperado pela aplicação.

## Regras
#### Lista de regras `rules`
+ **integer `isInteger()`:** regra para validação de números inteiros.

+ **float `isFloat()`:** regra para validação de números decimais. 

+ **date `isDate()`:** regra para validação de data.

+ **time `isTime()`:** regra para validação de hora.

+ **datetime `isDateTime()`:** regra para validação de date/hora.

+ **required `isRequired()`:** regra para validação de preenchimento requerido.

+ **email `isEmail()`:** regra para validação de e-mail válido.

+ **minlength[0] `isMinLength()`:** regra para validação de quantidade mínima de caracteres.

+ **maxlength[0] `isMaxLength()`:** regra para validação de quantidade máxima de caracteres.

## Métodos
#### Detalhamento dos métodos de validação
+ **public boolean isInteger(java.lang.String value):** recebe uma `string` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isFloat(java.lang.String value):** recebe uma `string` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isDate(java.lang.String value):** recebe uma `string` no formato `dd/MM/yyyy` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isTime(java.lang.String value):** recebe uma `string` no formato `HH:mm:ss` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isDateTime(java.lang.String value):** recebe uma `string` no formato `dd/MM/yyyy HH:mm:ss` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isRequired(java.lang.String value):** recebe uma `string` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isEmail(java.lang.String value):** recebe uma `string` como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isMinLength(java.lang.String value, java.lang.Integer min):** recebe uma `string` e um `integer` de tamanho mínimo como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public boolean isMaxLength(java.lang.String value, java.lang.Integer max):** recebe uma `string` e um `integer` de tamanho máximo como parâmetro retornando `true` caso valor seja válido ou `false` caso seja inválido.

+ **public void clear():** método responsável por limpar as listas de dados para validação e lista de erros geradas após a chamada do método **validade()**.

+ **public void add(java.lang.String field, java.lang.String label, java.lang.String rule, java.lang.String message):** método responsável por adicionar dados a serem validados pelo método **validade()**. Parmâmetros: `field` nome do campo responsável pelo valor informado, `label` valor presente no campo responsável, `rule` lista de regras para validação, caso queira utilizar mais de uma regra para o mésmo field, utilizar o delimitador `;` e `message` mensagem de erro a ser utilizada caso o valor seja inválido.

  ***Exemplo:***
  **add(**'`nome`', '`Nome do usuário`', '`required;minlength[3];maxlength[150]`', '`Informe o nome do usuário`'**)**;

+ **public boolean validate():** método responsável pela validação dos field's adicionados pelo método **add()**.

+ **public java.util.List<java.lang.String[]> getErrors():** método responsável por retornar uma lista de erros de validação.

+ **public boolean findError(java.lang.String field):** método responsável pela localização de field's que originaram um erro após sua validação.
