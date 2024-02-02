# entrevista Spring Boot = Junior
## 1 - Fale sobre sua experiência em projetos Java e Spring Boot. Quais foram os desafios que você enfrentou e como os superou?

- Eu desenvolvi dois projetos que foram mais extensos, o primeiro seria uma API de vídeos onde a própria API controla o fluxo de postagens de vídeos, o segundo projeto foi um sistema de blog de viagens, uma API que compartilha um título, imagem e comentário de usuários, ambos os projetos utilizaram o Spring Security para controlar o login/cadastro. A principal dificuldade foi na elaboração, pensar no modelo do banco de dados, e como seria o fluxo e a relação entre as camadas.

## 2 - Como você lida com a injeção de dependência no Spring Boot? Pode explicar o conceito e fornecer um exemplo prático de uso?

- Para a injeção de dependência no Spring Boot, eu utilizo o próprio recurso do Spring Boot, a anotação @Autowired, e em alguns casos específicos eu utilizo a injeção por construtor.
 
    @Autowired
    private InjecaoDeDependencia injecaoDeDependencia;

  ou

  private InjecaoDeDependencia injecaoDeDependencia;

  public MyClass(InjecaoDeDependencia injecaoDeDependencia){
  
     this.injecaoDeDependencia = injecaoDeDependencia;
  
  }

## 3 - Como você abordaria a resolução de um problema de performance em uma aplicação Spring Boot? Pode mencionar algumas estratégias que você consideraria?

- Para problemas de performance, uma solução seria a organização do código em algum padrão de projeto/design patterns como o MVC, e em alguns casos a implementação de paginação da API iria controlar o fluxo de dados requisitados no banco de dados, e a utilização de custom query do JPA para a otimização de buscas no banco de dados.

## 4 - Descreva sua experiência com testes unitários. Você já utilizou JUnit ou TestNG em projetos anteriores? Como você garante uma boa cobertura de testes no código?

- Resposta: Para a resolução de um processo seletivo eu utilizei o JUnit, replicando a camada de service no pacote test, dentro dos testes eu procurei manter a estrutura do service(em alguns casos dentro do service uma exceção é retornada) então ao nível de teste eu procurei manter todos os cenários possíveis.

## 5 - Qual a diferença entre uma aplicação web RESTful e uma aplicação SOAP? Você tem experiência prática com a construção e consumo de APIs RESTful em Java?

- Uma aplicação web SOAP é menos flexível do que a API REST enquanto a SOAP so aceita mensagens XML a API REST aceita diversos tipos, como: HTML, XML e JSON. Todos os meus projetos têm o foco no desenvolvimento RESTful.

## 6 - Como você garantiria a segurança de uma aplicação Spring Boot? Pode mencionar algumas práticas ou frameworks de segurança que você consideraria?

- A forma mais recomendada é a utilização do Spring Security com o OAuth2 para o uso de tokens, uma boa prática também é usar o padrão DTO ou Object Value na requisição de dados.

## 7 - Como funciona o ciclo de vida de uma requisição HTTP em uma aplicação Spring MVC? Pode explicar as principais etapas?

- (Resposta corrigida) = DispatcherServlet recebe a requisição e indentifica o controller pelo mapeamento da URL e então o controller processa a requisição e retorna uma Model para o DispatcherServlet que processa a view e retorna a resposta

## 9 - Como você lida com a persistência de dados em uma aplicação Spring Boot? Já teve experiência com Hibernate ou outro framework ORM?

 - Em todos os meus projetos, eu utilizo o pacote JPA que inclui o Hibernate.

## 10 - Como você escolhe entre usar um banco de dados relacional ou NoSQL em um projeto Spring Boot? Quais fatores influenciariam sua decisão?

 - Todos os meus projetos foram desenvolvidos utilizando um banco de dados relacional, o principal fator que influenciou a escolha foi a facilidade de criar relações entre as entidades com as chaves estrangeiras.

## 11 - Você pode compartilhar uma situação em que teve que aprender rapidamente uma nova tecnologia ou framework para resolver um problema em um projeto? Como você abordou esse desafio?

 - No projeto da API de vídeos, eu tive que aprender o Spring Security para implementar o sistema de login.
