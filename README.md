# AppCivico
Documentação de Endpoints para acesso à plataforma de AppCivicos do TCU.
## Dados Abertos
Visando facilitar o acesso à dados abertos do governo para a comunidade de desenvolvedores o Tribunal de Contas da União criou a plataforma AppCívico, que fornece através de uma API de serviços REST informações abertas. Exemplo:
- Informações georreferênciadas sobre estabelecimentos de saúde públicos e privados do país, sendo as mesmas providas do   [Cadastro Nacional de Estabelecimentos de Saúde (CNES)](http://cnes.datasus.gov.br/) que é a base do próprio DataSUS.
- Informações também georreferênciadas sobre escolas públicas e privadas do país providas do Censo Escolar [Instituto      Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP)](http://portal.inep.gov.br/).
- Informações sobre remédios fabricados no Brasil providas da [Agência Nacional de Vigilância Sanitária](http://portal.anvisa.gov.br/).
- Entre outros dados de utilidade pública.

O objetivo é fazer com que mais desenvolvedores, interessados em desenvolver aplicações cívico sociais possam ter acesso de maneira fácil à dados abertos, gerando cada vez mais aplicações de utilidade pública, que poderão prover tranparência das informações e de certa forma ajudar a população.

## Metamodelo
  Muitos desenvolvedores na comunidade que tem idéias de aplicações de utilidade pública, muitas vezes esbarram em vários problemas que acabam atrapalhando o desenvolvimento. Alguns dos maiores problemas encontrados são o custo de serviços de *cloud* e a dificuldade de se desenvolver um serviço de *backend*, em geral webservices REST, para armazenamento de dados da sua aplicação. Desenvolver uma aplicação de cívico social de utilidade não visa lucro, então o desenvolvedor acaba não tendo como arcar com os custos de uma hospedagem ou de um serviço de *cloud* e a aplicação acaba não sendo desenvolvida por causa disso. Além desse problema com os custos, existe a parte do desenvolvimento desse serviço. Contruir um serviço em *cloud* para servir de *backend* para uma aplicação é uma tarefa a mais que o desenvolvedor tem no processo de contrução da aplicação e que muitas vezes consome até mais tempo do que o desenvolvimento da própria aplicação.
  
  Pensando nisso a plataforma AppCívico disponibiliza conjunto de serviços que são a abstração de um metamodelo genérico que é capaz de prover serviços básicos para qualquer aplicação. O metamodelo provê serviços como cadastro e armazenamento de usuários genéricos, criação de perfis específicos para determinado aplicativo , *login* com senha ou com redes sociais **Facebook**, **Twitter**, **Intagram** e **GooglePlus**. Além de dar suporte à dados de usuários o metamodelo também proporciona a criação de grupos de usuário relacionados a um aplicativo, provê também suporte à notificações para aplicativos móveis. Para armazenamento de dados bastante genéricos é dado ao desenvolvedor o objeto de **Postagem** onde criada uma postagem, pode - se associar vários conteúdos a mesma seja ele objetos da aplicação ou arquivos binários como por exemplo fotos ou vídeos. Os conteúdos que são objetos objetos são salvos como no formato **JSON**, fazendo com que ele seja dinâmico e genérico podendo armazenar qualquer objeto. Podendo posteriormente alterar, excluir e fazer buscas nos mesmos. A seguir iremos abordar cada *endpoint* do metamodelo especificando como funciona, como cada entidade se relaciona e como usa - lo na sua aplição. Umas das grandes utilidades desse metamodelo, além de facilitar o trabalho do desenvolvedor é contribuir a geração de informação aberta e dados de utilidade pública que podem ajudar a população e contribuir para que os dados abertos se tornem mais precisos. Um exemplo dessa geração de informação, são aplicativos que já usam a base de estabelecimentos de saúde e de escolas, e que por meio de uma mecânica colaborativa o usuário pode dar *feedback* na localização do local, dando assim sugestões de onde seria a localização correta, o que ajuda a tornar a qualidade da informação melhor o que faz com que os aplicativos construidos a partir dessa informação, consigam ser mais efetivos no dia-a-dia da população que utiliza os mesmo.

##API Reference
  Links para Documentação das API
  [API de Estabelecimentos de Saúde](#../EstabelecimentosAPI.md)
