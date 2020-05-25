# Código aberto em 12 passos 👣🔓

Um guia para começar a contribuir em open source.

## Para quem é esse guia?

Quem quer contribuir com open-source mas não sabe por onde começar. Foco em contribuição de código para os projetos [Ignition Robotics](https://ignitionrobotics.org) e [ROS 2](https://index.ros.org/doc/ros2/).

## Formas de colaborar

* Código
    * Adicionar funcionalidades
    * Consertar bugs
* Conteúdo
    * Design gráfico
    * Tradução
    * Documentação
    * Usabilidade
* Comunidade
    * Tirar dúvidas
    * Triagem
etc...

## O que você ganha colaborando?

* Experiência no mundo real
* Colaboração em equipes grandes
* Exposição a boas práticas da indústria
* Portfólio
* Dinheiro

## O que você precisa para começar?

* Inglês
    * Ler e escrever
    * Ninguém está preocupado com sua gramática. O importante é se comunicar.
    * Existem projetos sendo desenvolvidos em português, mas a grande maioria dos projetos desenvolvidos no mundo inteiro são em inglês.
* Controle de versão ([git](https://git-scm.com/))
* Habilidades específicas de cada projeto

👣👣👣👣👣👣👣👣👣👣👣👣

# 12 passos

# 1 👣 Escolher o software

* Organizações participando do [Google Summer of Code](https://summerofcode.withgoogle.com/organizations/)
* [Tópicos no GitHub](https://github.com/topics)

<details>
  <summary>🔥 Ignition Robotics</summary>

  [IgnitionRobotics.org](https://ignitionrobotics.org)
</details>

<details>
  <summary>🐢 ROS 2</summary>

  [ROS 2 Documentation](https://index.ros.org/doc/ros2/)
</details>

# 2 👣 Familiarizar-se com o software

* Se ainda não é usuário, use!
* Faça tutoriais
* Rode exemplos
* Faça perguntas

<details>
  <summary>🔥 Ignition Robotics</summary>

  * [Tutoriais: Ignition Citadel](https://ignitionrobotics.org/docs/citadel/gui)
  * [Tutoriais: Ignition Gazebo](https://ignitionrobotics.org/api/gazebo/3.0/tutorials.html)
  * [Gazebo Answers](https://answers.gazebosim.org/)
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * [Tutoriais: ROS 2](https://index.ros.org/doc/ros2/Tutorials/#tutorials)
  * [ROS Answers](https://answers.ros.org/)
</details>

# 3 👣 Descobrir processo de contribuição

* Faça uma busca
* Fóruns
* Chats (IRC, Slack...)
* Mailing lists
* Arquivo `CONTRIBUTING.md`

<details>
  <summary>🔥 Ignition Robotics</summary>

  * [Contributing to Ignition Robotics](https://ignitionrobotics.org/docs/all/contributing)
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * [Contributing: ROS 2](https://index.ros.org/doc/ros2/Contributing/)
</details>

# 4 👣 Escolher como contribuir

* Lista de problemas (issue tracker)
* Pergunte se alguém já começou a fazer o que você quer fazer, se tem dicas, sugestões...

<details>
  <summary>🔥 Ignition Robotics</summary>

  * [Ignition Robotics: good first issues](https://github.com/search?q=org%3Aignitionrobotics+label%3A%22good+first+issue%22&type=Issues)
  * [Ignition Robotics: todos os issues](https://github.com/search?q=org%3Aignitionrobotics&state=open&type=Issues)
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * [ROS 2: good first issues](https://github.com/search?q=org%3Aros2+label%3A%22good+first+issue%22&type=Issues)
  * [ROS 2: help wanted](https://github.com/search?q=org%3Aros2+label%3A%22help+wanted%22&type=Issues)
</details>

# 5 👣 Familiarizar-se com o código

* Organização do código
* Workflow
* Tente mudar qualquer coisinha pra ver se funciona

<details>
  <summary>🔥 Ignition Robotics</summary>

  Recomendações:
  
  * Clone e compile todas as bibliotecas (leva uma meia hora)
  * Use [colcon](https://colcon.readthedocs.io/) para manter seu código isolado
  * Não misture instalação de binários com instalação da fonte
</details>

<details>
  <summary>🐢 ROS 2</summary>

  Recomendações:
  
  * Clone e compile somente os pacotes necessários
  * Desinstale binários desses pacotes
</details>

# 6 👣 Programar!

* Escolha o "branch" por onde começar
* Crie um "branch" separado
* [grep](https://pt.wikipedia.org/wiki/Grep)e muito!
* Não tente entender tudo!
* Organize as `commit`s

<details>
  <summary>🔥 Ignition Robotics</summary>

  * Comece de um "release branch" (`ign-<biblioteca>N`) ou `master`
  * Os headers ficam em `include`, a implementação em `src`
  * Os testes ficam em `test` e `src` e terminam com `_TEST.cc`
  * Cada biblioteca tem uma pasta de exemplos, `examples`
  * Lembre de assinar as commits (`git commit -s`)
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * Comece do branch padrão, geralmente `master`
  * Os headers ficam em `include`, a implementação em `src` e testes em `test`
  * Lembre de assinar as commits (`git commit -s`)
</details>

# 7 👣 Testes

* Escreva testes para que o problema não volte no futuro
* Verifique que não quebrou nenhum teste existente
* Verifique que não introduziu avisos (warnings)
* Muitos projetos iniciam testes automaticamente (CI, continuous integration)

<details>
  <summary>🔥 Ignition Robotics</summary>

  * Quando fizer o pull request, seu código será testado em todas as plataformas (Linux, OSX, Windows)
  * Os testes ficam em `build/bin` (ou `build/<pacote>/bin` com colcon)
  * Rode todos os testes da biblioteca com `make test` / `colcon test --package-select <pacote>`
  * Rode testes individuais com `./build/bin/<teste>`
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * Se fizer um pull request ao branch `master`, um membro da organização irá iniciar CI manualmente
  * Rode todos os testes do pacote com `colcon test --package-select <pacote>`
  * Rode testes individuais com `./build/<pacote>/bin/<teste>`
</details>

# 8 👣 Estilo

* Tente manter o estilo atual do projeto (nomes de funções, indentação...)
* Siga o estilo oficial, se houver
* Tente mudar somente o necessário para facilitar a revisão
* Certifique-se que os linters estão passando

<details>
  <summary>🔥 Ignition Robotics</summary>

  * [Ignition style guide](https://ignitionrobotics.org/docs/all/contributing#style-guides)
  * Vários aspectos do estilo não são checados por linters e podem ser apontados durante a revisão.
  * Teste com `bash tools/code_check.sh`
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * [ROS 2: Code style and language versions](https://index.ros.org/doc/ros2/Contributing/Code-Style-Language-Versions/)
  * Os pacotes principais do ROS 2 têm todo seu estilo checado por linters.
  * Rodam como parte dos testes.
</details>

# 9 👣 Documentação

* Documentação para APIs novas
* Comentários no código
* Exemplos de como usar
* Tutoriais, vídeos...

<details>
  <summary>🔥 Ignition Robotics</summary>

  * APIs são documentadas usando [Doxygen](https://www.doxygen.nl/) e publicadas online em [Ignition Robotics: Development libraries](https://ignitionrobotics.org/libs).
  * Tutoriais globais ficam no [ignitionrobotics/docs](https://github.com/ignitionrobotics/docs) e são publicados online em [Ignition Robotics: Docs](https://ignitionrobotics.org/docs/citadel).
  * Tutoriais para cada biblioteca ficam na pasta `tutorials` e são publicados junto às APIs em [Ignition Robotics: Development libraries](https://ignitionrobotics.org/libs).
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * APIs são documentadas usando [Doxygen](https://www.doxygen.nl/) e algumas são publicadas online em [http://docs.ros2.org](http://docs.ros2.org/eloquent/api/rcutils/index.html).
  * Tutoriais globais ficam no [ros2/ros2_documentation](https://github.com/ros2/ros2_documentation) e são publicados no [ROS Index](https://index.ros.org/doc/ros2/).
</details>

# 10 👣 Pull request

* Veja outros pull requests como exemplo da cultura do projeto
* Explique bem o que foi feito na descrição, qual problema está sendo resolvido e como testar a solução
* Facilite ao máximo a vida de quem vai revisar
* Se possível, divida em pedaços menores (vários pull requests)

<details>
  <summary>🔥 Ignition Robotics</summary>

  * Por exemplo, veja os [pull requests mergidos no ign-gazebo](https://github.com/ignitionrobotics/ign-gazebo/pulls?q=is%3Apr+is%3Aclosed+review%3Aapproved).
  * O resultado dos testes será linkado na interface do GitHub
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * Por exemplo, veja os [pull requests mergidos no rclcpp](https://github.com/ros2/rclcpp/pulls?q=is%3Apr+is%3Aclosed+review%3Aapproved).
</details>

# 11 👣 Revisão

* Responda comentários
* Faça as mudanças necessárias
* Pode levar desde horas até meses!
* Seja educad@!

<details>
  <summary>🔥 Ignition Robotics</summary>
 
  * Requer ao menos uma aprovação de um mantenedor
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * Requer ao menos uma aprovação de um mantenedor
</details>

# 12 👣 Merge

* Seu código passa a fazer parte do código fonte oficial
* Seu código aparecerá no próximo release oficial
* Agora os mantenedores sdo projeto manterão seu código, e você também pode ficar de olho caso apareçam problemas
* 🍾

<details>
  <summary>🔥 Ignition Robotics</summary>

  * Se fez o pull request em um branch `ign-<biblioteca>N`, seu código sairá no próximo release "minor" ou "patch".
  * Se foi ao `master`, sairá no próximo release "major".
</details>

<details>
  <summary>🐢 ROS 2</summary>

  * Se fez o pull request em um release branch, seu código sairá no próximo "sync" ou "patch".
  * Se foi ao `master`, sairá na próxima distribuição.
</details>

---

Este guia foi escrito para a Meetup ROS Brasil em maio de 2020.

Apresentação anterior:

* [Comece a desenvolver projetos open source](https://www.youtube.com/watch?v=H0baE1LGsks) (março de 2016).
