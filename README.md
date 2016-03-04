# Simples Dental

###Objetivo

Desenvolva uma API que execute o CRUD completo utilizando uma interface REST que atenda aos requisitos descritos abaixo. Como framework e plataforma para executar seu BACK-END utilize o PLAY Framework conectado ao Postgresql utilizando Hibernate ou queries nativas.

Ao finalizar o projeto faça um pull request nesse projeto em um branch órfão, e pronto =) não esqueça de deixar seus contatos no corpo do pull-request caso não os possua no `github`.

####Contatos

CHEMA DE CONTATO
  nome: String
  contato: String

#####API HTTP INTERFACE
```
GET /contacts
  params
    q: Busca
      RETURN Lista de contatos que contenham o texto passado em qualquer um dos seus atributos.
    fields: List<String>
      RETURN Lista de contatos apenas com os fields passados.
RETURN Lista de profissionais.

GET /contatcts/:id
RETURN Recupera os contato que atende ao ID indicado.

POST /contacts
RETURN Sucesso contato cadastrado.

PUT /contacts/:id
RETURN Altera o contato que atende ao ID indicado.

DELETE /contacts/:id
RETURN Sucesso contato excluído
````




####Profissionais

SCHEMA DE PROFISSIONAL
  nome: String
  cargo: ENUM
    0: Desenvolvedor
    1: Designer
    2: Suporte
    3: Tester
  nascimento: Date
  create_data: Date
  contatos: List<SCHEMA DE CONTATO>

#####API HTTP INTERFACE
```
GET /professeonals
  params
    q: Busca
      RETURN Lista de profissionais que contenham o texto passado em qualquer um dos seus atributos.
    fields: List<String>
      RETURN Lista de profissionais apenas com os fields passados.
RETURN Lista de profissionais.

GET /professeonals/:id
RETURN O profissional que atende ao ID indicado.

POST /professeonals
RETURN Sucesso profissional cadastrado.

PUT /professeonals/:id
RETURN Altera o profissional que atende ao ID indicado.

DELETE /professeonals/:id
RETURN Sucesso profissional excluído

/**
* Ao criar um profissional os contatos também são criados.
 * Ao editar um profissional os contatos também são editados.
 */
```
