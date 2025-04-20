
<h1>Portfólio das APIs - Cauana Dias Costa</h1>

<h4>Introdução</h4>

<p align="justify">Trabalho de Graduação na modalidade Portfólio das Aprendizagens a partir de Projeto Integrador (APIs), apresentado na Faculdade de Tecnologia de São José dos Campos - curso: Banco de Dados.</p>

<h4>Sobre mim</h4>

<p align="center"><img src="https://github.com/Cauana/bertoti/assets/77700346/fa566986-fa26-4d55-9d05-57cb6117387c" width="30%"></p>

<p align="justify">Bacharel em Administração Pública pela Universidade Estadual Paulista (UNESP) e regularmente matriculada no 6º semestre do curso tecnólogo em Banco de Dados pela Faculdade de Tecnologia de São José dos Campos (FATEC).</p>

<p align="justify">Possuo experiência na área de Tecnologia, tive a oportunidade de realizar meu estágio na General Electric (GE Taubaté) por um ano, onde trabalhei com o desenvolvimento de um projeto de melhoria das traduções técnicas com termos de Engenharia utilizando VBA e Python. Além disso, atuei realizando tratamento de dados, dashboards para entendimento de listas de documentos e principalmente desenvolvimento de automações de processos.</p>

<p align="justify">Atualmente sou Assessora de Tecnologia do Banco do Brasil (BB), onde atuo como desenvolvedora Backend Java, em projetos que envolvem mensageria e APIs que recebem, processam e enviam transações.</p>

<p align="center">• <a href="https://www.git.com/Cauana">LinkedIn</a> • <a href="https://www.linkedin.com/in/cauanadias/">GitHub</a> •</p>

<h4>Meus Projetos</h4>

<h4>1ª API - 2º semestre 2022</h4> 
<p align="justify"> Os professores da FATEC, precisavam de uma forma prática de avaliar e visualizar o desempenho dos alunos em equipes Scrum durante as sprints. Ele queria centralizar as notas de autoavaliação, avaliação entre pares e avaliação do próprio professor, com base na Escala Likert, para todos os grupos da sala em um único sistema. A solução desenvolvida, chamada "Agile Assessment" foi um sistema que realiza a avaliação 360° entre os membros de uma equipe scrum, sendo uma avaliação de seus pares de equipe, a si mesmo e de professores, utilizando a Escala Likert como parâmetro.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/5063a5ed-99b7-4fff-ba57-8ea1fe8242ba" width="70%"></p>

    
[GIT]([https://github.com/oJavaLi/doisrponto?tab=readme-ov-file](https://github.com/Pythonators/API_semestre1_pythonators?tab=readme-ov-file))

<summary><b>Tecnologias Utilizadas</b></summary>
<br>

![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) 
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) 
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) 
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) <strong>TinyDB</strong>


<b>Contribuições Pessoais</summary></b>
<br>
<p align="justify">Desempenhei o papel de Desenvolvedora, fui responsável pela estruturação de telas de avaliações construindo a interface gráfica, a estrutura de avaliações e o formulário de submissão, permitindo a interação do frontend por meio de formulários ao backend, que foi realizado através de banco de dados e json. Além disso trabalhei no CRUD (Criação, Deleção, Edição e Leitura) de dados de cadastro de professores.</p>
  
 

<details><Summary><b>Interface de Avaliação dos Professores</b></Summary>

![image](https://github.com/user-attachments/assets/529d760a-47f4-41fe-ac5a-0679fdd78cc2)


<code>
    
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Lista de Alunos</title>
        <script src="script/script.js"></script>
    <!--    https://fontawesome.com/   -->
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.1.0/css/all.css" integrity="sha384-lKuwvrZot6UHsBSfcMvOkWwlCMgc0TaWr+30HWe3a4ltaBwTZhyTEggF5tJv8tbt" crossorigin="anonymous">
    <link href="https://fonts.googleapis.com/css?family=Poppins" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-Zenh87qX5JnK2Jl0vWa8Ck2rdkQ2Bzep5IDxbcnCeuOxjzrPF/et3URy9Bv1WTRi" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-OERcA2EqjJCMA+/3y+gxIOqMEjwtxJY7qPCqsdltbNJuaOe923+mo//f6V8Qbsw3" crossorigin="anonymous"></script>
    <link rel="stylesheet" href="{{ url_for('static', filename='style_avaliacao.css') }}">
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
    </head>
    <body>
<!-- BARRA SUPERIOR-->
    <!--  começo do flashcard-->
      {% with messages = get_flashed_messages() %}
      {% if messages %}
        <ul class=flashes>
        {% for message in messages %}
          <li>{{ message }}</li>
        {% endfor %}
        </ul>
      {% endif %}
    {% endwith %}
    {% block body %}{% endblock %}
    <!--fim flashcard, FAVOR, PERSONALIZAR! Fonte: https://flask.palletsprojects.com/en/1.1.x/patterns/flashing/-->
    <nav class="navbar " id="barraSuperior">
      <div class="container-fluid" id="barraSuperior">
        <span class="intername" >{{session['usuario_logado']}}</span>
       
    
        <button class="navbar-toggler" type="button" data-bs-toggle="modal" data-bs-target="#exampleModal" id="OBotao">
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>
    </nav>
    
            <div class="modal true" id="exampleModal" tabindex="1" aria-labelledby="exampleModalLabel" aria-hidden="true">
              <div class="modal-dialog">
                <div class="modal-content">
                  <div class="modal-header" id="menuInter">
                    <h5 class="modal-title">MENU</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                  </div>
                  <div class="modal-body">
            
                    <ul class="list-group list-group-flush">
                      <li class="list-group-item"><a style="text-decoration:none; color:#2D3142" href="/aluno/avaliacao">Avaliar</a></li>                  
                      <li class="list-group-item"><a style="text-decoration:none; color:#2D3142" href="/dashboard">Visualizar suas notas</a></li>
                      <li class="list-group-item" ><a style="text-decoration:none; color:red" href="/logout">SAIR</a></li>
                    </ul>
            
                  </div>
                  <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                  </div>
                </div>
              </div>
            </div>
            <div class="container text-center"></div>
      </body>
      {% block conteudo %}
      {% endblock %}  
    <h1>REALIZAR AVALIAÇÕES</h1>
    <div class = "centralizar">
        {% for itens2 in alunos_turma%}
            <details>
                 <summary>PO: {{itens2}}</summary>
                 {% for pergunt in perguntas %}
                    <ul>
                        <il>{{pergunt.pergunta_}}</il>
                        <form action="/aluno/notas" method="POST">
                        <ul>
<!--                        <li >Extramamente -->
                                <input type="radio" value="5" name="{{itens2}}{{pergunt.name}}"required>Extremamente</input>
    <!--                            </li>-->
    <!--                        <li >Muito -->
                                <input type="radio" value= '4' name="{{itens2}}{{pergunt.name}}"required>Muito</input>
    <!--                        </li>-->
    <!--                        <li >médio -->
                                <input type="radio" value='3' name="{{itens2}}{{pergunt.name}}"required> Médio</input>
    <!--                            </li>-->
    <!--                        <li >pouco -->
                                <input type="radio" value='2' name="{{itens2}}{{pergunt.name}}"required>Pouco</input>
    <!--                            </li> nada-->
                                <input type="radio" value='1' name="{{itens2}}{{pergunt.name}}"required>Nada</input>
    <!--                            </li>-->
                        </ul>

    </ul>
                {% endfor %}
                

            </details>
        {%endfor%}

        {% for itens in alunos_turma2%}
            <details>
                 <summary>SCRUM MASTER: {{itens}}</summary>
                 {% for pergunt in perguntas %}
                    <ul>
                        <il>{{pergunt.pergunta_}}</il>
                        <form action="/aluno/notas" method="POST">
                        <ul>
<!--                        <li >Extramamente -->
                                <input type="radio" value="5" name="{{itens}}{{pergunt.name}}"required>Extremamente</input>
    <!--                            </li>-->
    <!--                        <li >Muito -->
                                <input type="radio" value= '4' name="{{itens}}{{pergunt.name}}"required>Muito</input>
    <!--                        </li>-->
    <!--                        <li >médio -->
                                <input type="radio" value='3' name="{{itens}}{{pergunt.name}}"required> Médio</input>
    <!--                            </li>-->
    <!--                        <li >pouco -->
                                <input type="radio" value='2' name="{{itens}}{{pergunt.name}}"required>Pouco</input>
    <!--                            </li> nada-->
                                <input type="radio" value='1' name="{{itens}}{{pergunt.name}}"required>Nada</input>
    <!--                            </li>-->
                        </ul>

    </ul>
                {% endfor %}
                <textarea rows="8" cols="50" name="justificativa" id="coment" maxlength="3000"></textarea>

            </details>
        {%endfor%}
                <br>
        <button type="submit">ENVIAR AVALIAÇÕES</button>
    </form>
    </div>
    </body>
    </html>
    </form>
</pre></code>
</details>


<details><Summary><b>Interface de Cadastro e Gerenciamento de Professores</b></Summary>

![image](https://github.com/user-attachments/assets/fed6be23-5d00-41f4-ae73-dbfe7ed6930d)



<code>
    
    {% extends 'admin.html' %}
    
    {% block conteudo %}
    <body>
        <div class="content">
          <div class="card-body">
            <h1>Cadastro de Professores</h1>
            <hr>
            <form style="width: 20rem;" action="cadastrar" method="POST">
              <div class="form-floating mb-3">
              </div>
        
        <div class="form-floating mb-3">
          <input type="text" class="form-control"  id="nome" name="nome" nome_completo="floatingInput" style="background-color:#ADACB5;" placeholder="NOME COMPLETO"required>
            <label for="floatingInput">NOME COMPLETO</label>
        </div>
        <div class="form-floating mb-3">
          <input type="text" class="form-control" name="usuario" usuario="floatingInput" style="background-color:#ADACB5;" placeholder="cargo" id="usuario"required>
            <label for="floatingInput">USUARIO</label>
        </div>
        <div class="form-floating mb-3">
          <input type="text" class="form-control" id="senha" name="senha" senha="floatingInput" style="background-color:#ADACB5;" placeholder="SENHA"required>
            <label for="floatingInput">SENHA</label>
        </div>
        <div class="form-floating mb-3">
        <div>
          <button type="submit" name="Enviar" class="btn btn-primary">Cadastrar</button>
        </div></form>
      </div>
    </div>
    <hr>
    <h1>Professores cadastrados</h1>
    <table class="table">
      <tr>
        <th>id</th>
        <th>nome_completo</th>
        <th>usuario</th>
        <th>senha</th>
       </tr>
      {% for contato in result %}
      <tr>
        <td>{{contato.id}}</td>
        <td>{{contato.nome}}</td>
        <td>{{contato.usuario}}</td>
        <td>{{contato.senha}}</td>
        <td><a class="btn btn-danger" href='/deletar/{{contato["id"]}}'>
          <i class="bi bi-trash"> </i>Deletar</a>
          <a href='/atualizar/{{contato["id"]}}'class="btn btn-secondary">
            <i class="bi bi-arrow-clockwise"> </i>Atualizar</a></td>
      </tr>
      {% endfor %}

    </table>
    <div class="opacMenu"></div>
    {% endblock %}
</code>
</details>

<details><Summary><b>Definição do backlog do produto.</b></Summary>

## Backlog do Produto <br id=c>
    
| Sprint |           Descrição               |                                            User Storie                                            | Prioridade |
|:------:|:--------------------------------: | :----------------------------------------------------------------------------------------: |         :------:  |
|   01   | Haverá um painel mostrando todas perguntas e possibilidades de avaliação, com 5 botões de avaliação | Eu como aluno quero poder realizar minhas avaliações para manter uma informação sobre o desempenho do time | Imprescindível |
|   01   | Haverá um painel com dados da sprint | Eu como aluno quero poder acessar minhas informações de sprint para melhor gerenciamento  | Importante |
|   01   | Haverá uma base de dados para avaliações | Eu como PBLTeX quero ter as avaliações armazenadas para não perder os dados de avaliações realizadas | Imprescindível |
|   01   | Haverá uma base de dados para login | Eu como PBLTeX quero ter uma tela de autenticação para conseguir entrar em determinados perfis | Imprescindível |
|   02   | Haverá uma diferenciação de times no cadastro | Eu como aluno quero ter minhas informações de grupo para melhor controle de qual é meu grupo e suas qualidades | Importante |
|   02   |Haverá uma diferenciação entre aluno e professor  | Eu como cliente quero que haja uma diferenciação entre aluno e orientador para melhor diferenciação de dados | Importante |
|   02   | Haverá uma tela de admin | Eu como PBLTeX quero que haja um perfil administrador para cadastrar ou retirar cadastro dos usuários | Imprescindível |
|   03   | Haverá uma tela de avaliação ao ScrumMaster | Eu como líder técnico quero poder avaliar meu aluno líder técnico para manter um bom rendimento de atividades | Importante |
|   03   | Haverá uma tela de avaliação ao PO | Eu como fake client quero avaliar meu aluno PO para manter bom rendimento e alterar pontos fracos | Imprescindível |
|   03  | Haverá um sistema de profiles | Eu como administrador quero atribuir um perfil específico a cada usuário cadastrado para que eu possa utilizar esse dado sistemicamente após sua autenticação | Imprescindível |
|   04   | Haverão telas de demonstração de pontuação | Eu como usuário quero que os dados sejam demonstrados de forma direta e prática para facilitação de entendimento |  Importante |
|   04  | Haverá uma visualização de avaliação geral | Eu como instrutor quero ter acesso a avaliação de meus alunos para saber qual seu rendimento na visão do time| Imprescindível |
|   04  | Haverá um dashboard ligado as informações de time, de sprint e de avaliações de usuário | Eu como aluno quero ter um dashboard para melhor facilidade de acompanhamento | Imprescindível |
<br/>

</details>

<br>

<h2>Hard Skills</h2>

<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Python</b></td> <td>Adquiri experiência com desenvolvimento de aplicações utilizando python e aprendendo a lógica.</td> </tr> <tr> <td align="center"><b>Lógica de Programação</b></td> <td> Consegui entender e compreender a lógica de programação para desenvolvimento de condições e aplicar lógica do negócio no código. </td> </tr> <tr> <td align="center"><b>Flask</b></td> <td>Conhecimento adquirido através do desenvolvimento de APIs RESTful e aplicações web com Flask.</td> </tr> <tr> <td align="center"><b>Git</b></td> <td>Versionamento de código, colaboração em equipe e uso de repositórios remotos (GitHub/GitLab).</td> </tr> <tr> <td align="center"><b>HTML/CSS/JavaScript</b></td> <td>Criação de interfaces responsivas e dinâmicas, com integração a APIs.</td> </tr> </table>

<h2>Soft Skills</h2>

<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Comunicação Efetiva</b></td> <td>Melhorei muito a comunicação, principalmente por fazer parte de um grupo grande, foi necessário aprender a lidar com diferentes tipos de ideias e formas de trabalhar</td> </tr> <tr> <td align="center"><b>Trabalho em Equipe</b></td> <td>Foi necessário atuar com colaboração ativa no projeto, respeitando prazos e contribuindo para a melhoria contínua.</td> </tr> <tr> <td align="center"><b>Resolução de Problemas</b></td> <td>Primeira vez enfrentando desafios sem saber como resolver e foi preciso pensar e estudar muito para propor soluções eficientes e escaláveis.</td> </tr> <tr> <td align="center"><b>Adaptabilidade</b></td> <td>Por ter pouco conhecimento em programação, precisei me adaptar muito a mudanças, começamos fazendo o projeto em tkinter o que atrapalhou muito o desenvolvimento, e após analisar junto ao grupo, modificamos e conseguimos chegar em um resultado bom.</td> </tr></table>
    
<h4>2ª API - 1º semestre 2023</h4> 
<p align="justify">O produto em parceria com a 2RP é um sistema que realiza o controle de horas excedentes de colaboradores da empresa.Anteriormente, a empresa enfrentava desafios na gestão de horas, dependendo de várias planilhas, o que limitava a disponibilidade, flexibilidade e controle necessários. Em resposta, desenvolvemos uma aplicação que centraliza o controle de horas excedentes, distinguindo entre horas extras e sobreavisos. Essa aplicação também oferece recursos de aprovação ou reprovação das horas pelo gestor da equipe e pelo departamento de Recursos Humanos.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/47537933-29eb-4be1-9125-8afe2555c88a" width="70%"></p>

    
[GIT](https://github.com/oJavaLi/doisrponto?tab=readme-ov-file)

<summary><b>Tecnologias Utilizadas</b></summary>
<br>

![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) 
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)

<b>Contribuições Pessoais</summary></b>
<br>
<p align="justify">Desempenhei o papel de Scrum Master, sendo responsável por facilitar a comunicação e coordenação entre a equipe e a empresa parceira, a 2RP. Durante o desenvolvimento do sistema de controle de horas excedentes, atuei na remoção de impedimentos para o time e garanti que os princípios ágeis fossem seguidos, promovendo um ambiente colaborativo e focado nos objetivos. Além disso, organizei as cerimônias do Scrum, como as reuniões diárias, revisões de sprint, e retrospectivas, assegurando que a equipe estivesse alinhada em relação aos requisitos do cliente e que o desenvolvimento fosse ágil e contínuo. 
Além disso, atuei na criação do Diagrama Entidade Relacionamento - DER, e na criação da interface de Apontamento de Horas Extras.</p>

<details><summary><b>Interface de Apontamento de Horas Extras</b></summary>

![image](https://github.com/user-attachments/assets/269aa6b3-a884-4697-baf0-b02ccebdb3ba)

<code>
    
    package com.ojavali.doisrponto.usuarios;

    import org.springframework.beans.BeanUtils;
    import org.springframework.beans.factory.annotation.Autowired;
    import org.springframework.http.HttpStatus;
    import org.springframework.http.ResponseEntity;
    import org.springframework.validation.annotation.Validated;
    import org.springframework.web.bind.annotation.*;
    
    import java.util.List;
    import java.util.Optional;
    
    @RestController
    @RequestMapping("/api/users")
    public class UserController {

    @Autowired
    private UserRepository userRepository; 

    // Criação de usuário
    @PostMapping("/cadastrarUsuario")
    public ResponseEntity<User> cadastrarUsuario(@RequestBody @Validated User user) {
        return ResponseEntity.status(HttpStatus.CREATED).body(userRepository.save(user));
    }

    // Obter todos os usuários
    @GetMapping("/usuarios")
    public ResponseEntity<List<User>> getAllUsers() {
        return ResponseEntity.status(HttpStatus.OK).body(userRepository.findAll());
    }

    // Obter um usuário com base no ID
    @GetMapping("/usuarios/{id}")
    public ResponseEntity<Object> getUsuario(@PathVariable(value = "id") Long id) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            return ResponseEntity.status(HttpStatus.OK).body(user);
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }

    // Atualizar dados de um usuário
    @PutMapping("/usuarios/{id}")
    public ResponseEntity<Object> updateUsuario(@PathVariable(value = "id") Long id, @RequestBody User updatedUser) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            BeanUtils.copyProperties(updatedUser, user, "id"); 
            userRepository.save(user);
            return ResponseEntity.status(HttpStatus.OK).body(user);
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }

    // Deletar um usuário
    @DeleteMapping("/usuarios/{id}")
    public ResponseEntity<Object> deleteUsuario(@PathVariable(value = "id") Long id) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            userRepository.delete(user);
            return ResponseEntity.status(HttpStatus.OK).body("Usuário deletado com sucesso!");
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }
            
</code>
</details>

<details><summary><b>Diagrama Entidade Relacionamento - DER</b></summary>

  ![image](https://github.com/user-attachments/assets/8ec5ae62-b894-400d-b076-75e22fce3c1c)

</details>


<details><Summary><b>Definição do backlog do produto.</b></Summary>

|           Task             | Importância|
|:---------------------------------:|:----------:|
|Como um colaborador gostaria de ter um sistema onde consiga ser capaz de lançar todas as informações sobre horas excedentes trabalhadas, para poder ser pago.|1|
|Como colaborador eu quero ser capaz de diferenciar horas extra de sobreaviso para controlar melhor meu tempo de trabalho e ter pagamento adequado.|2|
|Como um RH, eu quero ser capaz de visualizar os apontamentos submetidos por cada funcionário, para que eu possa revisar a carga trabalhada para submeter a pagamento.|3|
|Como RH, eu quero ser capaz de aprovar ou rejeitar as horas trabalhadas garantir não ter qualquer erro ou inconsistência no lançamento e fazer pagamento correto aos colaboradores.|4|
|Como RH, eu gostaria de ter a permissão de criar e gerenciar contas de um usuário com diferentes níveis de acesso, para poder cadastrar os funcionários em segurança no meu sistema.|5|
|Como um gestor, eu quero ser capaz de visualizar os apontamentos submetidos pelo meu CR, para que eu possa revisar a carga trabalhada para submeter a pagamento.|6|
|Como gestor, eu quero ser capaz de aprovar ou rejeitar as horas trabalhadas garantir não ter qualquer erro ou inconsistência no lançamento e fazer pagamento correto aos colaboradores.|7|
|Como um colaborador, eu quero ser capaz de visualizar informações sobre as minhas próprias horas extras executadas no dashboard, para ter maior controle das horas aprovadas/ reprovadas e pagamento adequado.|8|
|Como RH, eu quero ser capaz de acessar um dashboard em tempo real que me permita monitorar as horas extras executadas pelos colaboradores, para acompanhar horas trabalhadas de acordo com as necessidades do CR|9|

</details>

<h2>Hard Skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Java</b></td> <td>Desenvolvimento de aplicações utilizando Java para backend.</td> </tr> <tr> <td align="center"><b>Java Spring Framework</b></td> <td>Criação de APIs RESTful, gerenciamento de dependências e injeção de dependências com Spring Boot.</td> </tr> <tr> <td align="center"><b>Banco de Dados Relacionais (PostgreSQL)</b></td> <td>Modelagem, consultas SQL básicas.</td> </tr> <tr> <td align="center"><b>Git</b></td> <td>Controle de versão, colaboração em equipe e uso de repositórios remotos.</td> </tr> <tr> <td align="center"><b>RESTful APIs</b></td> <td>Desenvolvimento de serviços web seguindo boas práticas de arquitetura REST.</td> </tr> <tr> <td align="center"><b>HTML/CSS/JavaScript</b></td> <td>Criação de interfaces web responsivas e interativas.</td> </tr> <tr> <td align="center"><b>Diagrama DER</b></td> <td>Modelagem de banco de dados e relacionamento entre entidades.</td> </tr> </table>
<h2>Soft Skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Trabalho em Equipe</b></td> <td>Colaboração ativa em projetos e respeito às opiniões dos colegas.</td> </tr> <tr> <td align="center"><b>Resolução de Problemas</b></td> <td>Habilidade para identificar desafios e propor soluções eficazes, principalmente com um produto real, tentando entender a real entrega de valor.</td> </tr> <tr> <td align="center"><b>Gestão do Tempo</b></td> <td>Planejamento eficiente para cumprir prazos e aumentar produtividade, com mais pressão pois tinha um cliente real.</td> </tr> <tr> <td align="center"><b>Aprendizado Contínuo</b></td> <td>Busca constante por atualização e aprimoramento profissional, através de um projeto real.</td> </tr> <tr> <td align="center"><b>Resiliência</b></td> <td>Lidar com os desafios propostos e persistir até encontrar uma solução.</td> </tr> </table>

<h4>3ª API - 2º semestre 2023</h4> 
<p align="justify">O produto 2Rponto é um sistema que realiza o controle de horas excedentes de colaboradores da empresa 2RP Net. A empresa parceira é conhecida por disponibilizar soluções para análise de informações em tempo real para tomada de decisões de negócios que precisam atender requisitos de tempo extremamente rigorosos. As soluções inovadoras e customizadas a diferenciam no mercado, assim como os serviços, permitem o crescimento de negócio e de seus resultados.</p>

<p align="center"><img src="https://github.com/Cauana/bertoti/assets/77700346/2c90ccaa-860e-44a9-afa8-b276b372905e" width="70%"></p>

<p align="justify">Anteriormente, a empresa enfrentava desafios na gestão de horas, dependendo de várias planilhas, o que limitava a disponibilidade, flexibilidade e controle necessários. Em resposta, desenvolvemos uma aplicação que centraliza o controle de horas excedentes, distinguindo entre horas extras e sobreavisos. Essa aplicação também oferece recursos de aprovação ou reprovação das horas pelo gestor da equipe e pelo departamento de Recursos Humanos. Além disso, inclui painéis de controle para os colaboradores visualizarem suas horas aprovadas ou reprovadas, enquanto gestores e RH podem monitorar as pendências de aprovação de seus respectivos usuários. </p>
    
[GIT](https://github.com/oJavaLi/doisrponto?tab=readme-ov-file)

<summary><b>Tecnologias Utilizadas</b></summary>
<br>

![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) 
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)


<b>Contribuições Pessoais</summary></b>
<br>
<p align="justify">Desempenhei o papel de Product Owner, realizando o levantamente dos requisitos para construção do backlog do produto, garantindo uma compreensão do time sobre as necessidades do cliente e das regras de negócio. Fui responsável pela estruturação de classes, desenvolvi a aplicação cliente-servidor para apontamentos de sobreavisos e cadastro de usuários, além de realizar correções ao banco de dados. Sendo as atividades desempenhadas:</p>
  
 

<details><Summary><b>Controller de Usuário.</b></Summary>
<pre><code>
package com.ojavali.doisrponto.usuarios;

import org.springframework.beans.BeanUtils;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.validation.annotation.Validated;
import org.springframework.web.bind.annotation.*;

import java.util.List;
import java.util.Optional;

@RestController
@RequestMapping("/api/users")
public class UserController {

    @Autowired
    private UserRepository userRepository; 

    // Criação de usuário
    @PostMapping("/cadastrarUsuario")
    public ResponseEntity<User> cadastrarUsuario(@RequestBody @Validated User user) {
        return ResponseEntity.status(HttpStatus.CREATED).body(userRepository.save(user));
    }

    // Obter todos os usuários
    @GetMapping("/usuarios")
    public ResponseEntity<List<User>> getAllUsers() {
        return ResponseEntity.status(HttpStatus.OK).body(userRepository.findAll());
    }

    // Obter um usuário com base no ID
    @GetMapping("/usuarios/{id}")
    public ResponseEntity<Object> getUsuario(@PathVariable(value = "id") Long id) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            return ResponseEntity.status(HttpStatus.OK).body(user);
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }

    // Atualizar dados de um usuário
    @PutMapping("/usuarios/{id}")
    public ResponseEntity<Object> updateUsuario(@PathVariable(value = "id") Long id, @RequestBody User updatedUser) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            BeanUtils.copyProperties(updatedUser, user, "id"); 
            userRepository.save(user);
            return ResponseEntity.status(HttpStatus.OK).body(user);
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }

    // Deletar um usuário
    @DeleteMapping("/usuarios/{id}")
    public ResponseEntity<Object> deleteUsuario(@PathVariable(value = "id") Long id) {
        Optional<User> userOptional = userRepository.findById(id);

        if (userOptional.isPresent()) {
            User user = userOptional.get();
            userRepository.delete(user);
            return ResponseEntity.status(HttpStatus.OK).body("Usuário deletado com sucesso!");
        } else {
            return ResponseEntity.status(HttpStatus.NOT_FOUND).body("Usuário não encontrado");
        }
    }
}

</pre></code>
</details>

<details><Summary><b>Formulário de Sobreavisos.</b></Summary>
<pre><code>
    
const formulario = document.querySelector("sobre-aviso-form");
const botao = document.querySelector("submit");
const entrada = document.querySelector(".entrada");
const saida = document.querySelector(".saida");
const cliente = document.querySelector(".cliente");
const projeto = document.querySelector(".projeto");
const cr = document.querySelector(".cr");
const justificativa = document.querySelector(".justificativa");
const matricula = 1;

function getQueryParameter(name) {
    const urlSearchParams = new URLSearchParams(window.location.search);
    return urlSearchParams.get(name);
}

const username = getQueryParameter('username');
const categoria = getQueryParameter('categoria');

const usernameDisplay = document.getElementById('usernameDisplay');

usernameDisplay.textContent = `Matrícula: ${username}`; // Exemplo de mensagem de boas-vindas
function cadastrar(){
    fetch("http://localhost:1234/cadastrarApontamentos",
        {
            headers: {
                'Accept':'application/json',
                'Content-Type':'application/json'
            },
            method:"POST",
            body: JSON.stringify({
                categoria: categoria,
                data_hora_inicio:  entrada.value,
                data_hora_fim: saida.value,
                justificativa: justificativa.value,
                usuarioMatricula:  username,
                centroResultadosId: cr.value

            })
        })
        .then(function (res){
            // Verifica se a resposta da requisição foi bem-sucedida
            if (res.ok) {
                // Redireciona para a outra página HTML após o cadastro bem-sucedido
                window.location.href = `listarApontamentos.html?username=${username}`;
            } else {
                console.log("Erro ao cadastrar");
            }
        })
        .catch(function(res) {console.log(res)})
}
formulario.addEventListener('submit', function(event){
    event.preventDefault();
    cadastrar();
});
document.getElementById("submit2").addEventListener("click", function () {
    // Volte para a página anterior no histórico de navegação
    window.location.href = `listarApontamentos.html?username=${username}`;
});

document.addEventListener('DOMContentLoaded', function () {
    // Execute este código após a página ser completamente carregada

    // Obtém a referência ao elemento <select> com id="cr"
    const crSelect = document.getElementById('cr');

    // Faça uma solicitação AJAX (ou fetch) para buscar os IDs da URL
    fetch('/CR')
        .then(response => {
            if (!response.ok) {
                throw new Error('Erro na solicitação.');
            }
            return response.json();
        })
        .then(data => {
            // Preencha as opções do <select> com as propriedades "id" dos objetos
            data.forEach(obj => {
                const option = document.createElement('option');
                option.value = obj.id.toString(); // Acesse a propriedade "id" do objeto e converta para string
                option.textContent = obj.id.toString(); // Acesse a propriedade "id" do objeto e converta para string
                crSelect.appendChild(option);
            });
        })
        .catch(error => {
            console.error('Erro:', error);
        });
});

document.addEventListener('DOMContentLoaded', function () {

    function fetchApontamentosAndPopulateTable() {
        const token = sessionStorage.getItem("token");
        if (!token) {
            window.location.href = "/index.html";
        }
        // Execute este código após a página ser completamente carregada
        const crSelect = document.getElementById('cr');
        const clienteInput = document.getElementById('cliente');
        const projetoInput = document.getElementById('projeto');

        crSelect.addEventListener('change', function () {
        const crValue = this.value; 

            if (!crValue) {
                clienteInput.value = ''; // Limpa o campo "Cliente"
                projetoInput.value = ''; // Limpa o campo "Projeto"
                return;
            }

            fetch("/CR/" + crValue)
                .then(response => {
                    if (!response.ok) {
                        throw new Error('Erro na solicitação.');
                    }
                    return response.json();
                })
                .then(data => {
                    // Preencha os campos "cliente" e "projeto" com os dados do JSON
                    clienteInput.value = data.nome_cliente;
                    projetoInput.value = data.nome_projeto;
                })
                .catch(error => {
                    console.error('Erro:', error);
                });
        });
    }
    fetchApontamentosAndPopulateTable();

});

</pre></code>
</details>

<details>
  <summary><b>Conexão entre o backend e o front-end para cadastro de apontamentos</b></summary>
  <pre><code>
const formulario = document.querySelector("form");
const botao = document.querySelector("button");
const UserNome = document.querySelector(".name");
const UserMatricula = document.querySelector(".matricula");
const UserEmail = document.querySelector(".email");
const UserSenha = document.querySelector(".password");
const UserCategoria = document.querySelector(".role");

function cadastrar() {
    fetch("http://localhost:1234/cadastrarApontamento", {
        headers: {
            'Accept': 'application/json',
            'Content-Type': 'application/json'
        },
        method: "POST",
        body: JSON.stringify({
            nome: UserNome.value,
            matricula: UserMatricula.value,
            email: UserEmail.value,
            senha: UserSenha.value,
            categoria: UserCategoria.value
        })
    })
    .then(function (res) { console.log(res) })
    .catch(function (res) { console.log(res) })
};

formulario.addEventListener('submit', function (event) {
    event.preventDefault();
    cadastrar();
});
  </code></pre>
</details>


<details><Summary><b>Definição do backlog do produto.</b></Summary>

 | Rank|           Task             |Prioridade|Sprint|
|:---------------------------------:|:----------:|:----------:|:----------:|
|1|Como RH, eu gostaria de ter a permissão de criar e gerenciar contas de um usuário com diferentes níveis de acesso, para poder cadastrar os funcionários em segurança no meu sistema.|Média|1|
|2|Como um colaborador gostaria de ter um sistema onde consiga ser capaz de lançar todas as informações sobre horas excedentes trabalhadas, para poder ser pago.|Alta|1|
|3|Como colaborador eu quero ser capaz de diferenciar horas extra de sobreaviso para controlar melhor meu tempo de trabalho e ter pagamento adequado.|Alta|2|
|4|Como um RH, eu quero ser capaz de visualizar os apontamentos submetidos por cada funcionário, para que eu possa revisar a carga trabalhada para submeter a pagamento.|Média|2|
|5|Como RH, eu quero ser capaz de aprovar ou rejeitar as horas trabalhadas garantir não ter qualquer erro ou inconsistência no lançamento e fazer pagamento correto aos colaboradores.|Alta|2|
|6|Como um gestor, eu quero ser capaz de visualizar os apontamentos submetidos pelo meu CR, para que eu possa revisar a carga trabalhada para submeter a pagamento.|Média|3|
|7|Como gestor, eu quero ser capaz de aprovar ou rejeitar as horas trabalhadas garantir não ter qualquer erro ou inconsistência no lançamento e fazer pagamento correto aos colaboradores.|Alta|3|
|8|Como um colaborador, eu quero ser capaz de visualizar informações sobre as minhas próprias horas extras executadas no dashboard, para ter maior controle das horas aprovadas/ reprovadas e pagamento adequado.|Baixa|4|
|9|Como RH, eu quero ser capaz de acessar um dashboard em tempo real que me permita monitorar as horas extras executadas pelos colaboradores, para acompanhar horas trabalhadas de acordo com as necessidades do CR|Baixa|4|
 
</details>
<br>

<h2>Hard Skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Java</b></td> <td>Desenvolvimento de aplicações utilizando Java para backend.</td> </tr> <tr> <td align="center"><b>Java Spring Framework</b></td> <td>Criação de APIs RESTful, gerenciamento de dependências e injeção de dependências com Spring Boot.</td> </tr> <tr> <td align="center"><b>Banco de Dados Relacionais (PostgreSQL)</b></td> <td>Modelagem, consultas SQL básicas.</td> </tr> <tr> <td align="center"><b>Git</b></td> <td>Controle de versão, colaboração em equipe e uso de repositórios remotos.</td> </tr> <tr> <td align="center"><b>RESTful APIs</b></td> <td>Desenvolvimento de serviços web seguindo boas práticas de arquitetura REST.</td> </tr> <tr> <td align="center"><b>Gestão de Backlog</b></td> <td>Criação, priorização e refinamento do backlog do produto, garantindo que os itens estejam bem definidos e alinhados com a estratégia de negócios.</td> </tr> <tr> <td align="center"><b>Definição de Requisitos</b></td> <td>Transformação das necessidades do negócio em requisitos claros e detalhados para a equipe de desenvolvimento.</td> </tr> </table>
<h2>Soft Skills</h2>

<table align="center" border="1" cellpadding="10" width="100%"> <tr> <th align="center" width="30%"><b>Habilidade</b></th> <th align="center" width="70%"><b>Descrição</b></th> </tr> <tr> <td align="center"><b>Comunicação Efetiva</b></td> <td>Capacidade de articular ideias com clareza para equipes técnicas, stakeholders e clientes.</td> </tr> <tr> <td align="center"><b>Negociação</b></td> <td>Habilidade para equilibrar interesses de diferentes partes e garantir que as prioridades certas sejam atendidas.</td> </tr> <tr> <td align="center"><b>Tomada de Decisão</b></td> <td>Aptidão para tomar decisões rápidas e bem fundamentadas, alinhadas à visão do produto.</td> </tr> <tr> <td align="center"><b>Visão Estratégica</b></td> <td>Capacidade de entender o mercado, concorrência e objetivos da empresa para guiar o desenvolvimento do produto.</td> </tr> <tr> <td align="center"><b>Empatia</b></td> <td>Compreensão das necessidades dos usuários finais e stakeholders para criar um produto que realmente agregue valor.</td> </tr> <tr> <td align="center"><b>Trabalho em Equipe</b></td> <td>Colaboração eficaz com desenvolvedores, designers e demais áreas da empresa.</td> </tr> <tr> <td align="center"><b>Resolução de Problemas</b></td> <td>Capacidade de identificar desafios e propor soluções inovadoras para superar obstáculos.</td> </tr> </table>

<h4>4ª API - 1º Semestre 2024</h4> 
<p align="justify">A Oracle Partner Tracker é uma plataforma inteligente de gerenciamento e análise de dados, capaz de interpretar, organizar e representar os dados do sistema OPN da empresa parceira Oracle. Entre os objetivos principais do projeto, se encontram a modernização do acompanhamento das empresas parceiras Oracle, assim como a visualização de dados de forma inteligente de Tracks e Expertises de cada empresa parceira, para facilitar a identificação de melhorias e de conclusões estratégicas.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/c6aad513-edad-42ed-bcfd-45cb2d8e1e72" width="70%"></p>

    
[GIT](https://github.com/oJavaLi/doisrponto?tab=readme-ov-file)

<summary><b>Tecnologias Utilizadas</b></summary>
<br> 

![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) 
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D) 
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white) 

</ul>
<b>Contribuições Pessoais</b>
</summary><br>
<p align="justify">Desempenhei o papel de Desenvolvedora, criando endpoints REST para fornecer informações sobre workload, além de desenvolver CRUD para o cadastro de novas Workloads, ou seja, cargas de trabalho que os parceiros podem obter. Também trabalhei na implementação de lógicas de negócios para garantir a correta manipulação das informações e na integração com o banco de dados.</p>
 

<details><Summary><b>Cadastro de Workload</b></Summary>
<p align="center"><img src="https://github.com/user-attachments/assets/a9969e5f-c1b3-4a1f-9be7-ddfa8d33d17f" width="70%"></p>
<pre><code>
 @PostMapping
    @Operation(summary = "Insert Workload", description = "Insert a new Workload")
    @ApiResponses( value = {
        @ApiResponse(
            responseCode = "201",
            description = "Workload inserted",
            content = @Content(
                schema = @Schema(implementation = WorkloadDTO.class)
            )
        ),
        @ApiResponse(
            responseCode = "400",
            description = "Workload already exists"
        )
    })
    public ResponseEntity<WorkloadDTO> insertWorkload(@RequestBody WorkloadDTO workloadDTO){
        
        workloadDTO = workloadService.insertWorkload(workloadDTO).get();
        if (workloadDTO == null){
            return new ResponseEntity<>(HttpStatus.BAD_REQUEST);
        }
        URI uri = ServletUriComponentsBuilder.fromCurrentRequest().path("/{id}")
                .buildAndExpand(workloadDTO.getId()).toUri();
        return ResponseEntity.created(uri).body(workloadDTO);
    }

</pre></code>

<pre><code>


package Oracle.Partner.Tracker.entities;

import Oracle.Partner.Tracker.dto.WorkloadDTO;
import Oracle.Partner.Tracker.entities.relations.WorkloadExpertise;
import Oracle.Partner.Tracker.utils.IngestionOperation;
import Oracle.Partner.Tracker.utils.Status;
import jakarta.persistence.*;
import java.time.LocalDateTime;
import java.util.ArrayList;
import java.util.List;

import lombok.AllArgsConstructor;
import lombok.Data;
import lombok.EqualsAndHashCode;
import lombok.NoArgsConstructor;

@Entity
@Data
@NoArgsConstructor
@AllArgsConstructor
@EqualsAndHashCode
@Table(name = "workload")
public class Workload {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    private String description;
    @Enumerated(EnumType.STRING)
    @Column(name = "ingestion_operation")
    private IngestionOperation ingestionOperation;
    @Enumerated(EnumType.STRING)
    private Status status;
    @Column(name = "create_at")
    private LocalDateTime createAt;
    @Column(name = "update_at")
    private LocalDateTime updateAt;
    @OneToMany(fetch = FetchType.LAZY)
    private List<WorkloadExpertise> workloadExpertises = new ArrayList<>();
    
    public Workload(WorkloadDTO workloadDTO) {
        this.name = workloadDTO.getName();
        this.description = workloadDTO.getDescription();
        this.ingestionOperation = workloadDTO.getIngestionOperation();
        this.status = workloadDTO.getStatus();
        this.createAt = workloadDTO.getCreateAt();
        this.updateAt = workloadDTO.getUpdateAt();
    }

    public void addWorkloadExpertise(WorkloadExpertise workloadExpertise){
        workloadExpertise.setWorkload(this);
        this.workloadExpertises.add(workloadExpertise);
    }
    
</code></pre>

<code><pre>

    public Optional<WorkloadDTO> insertWorkload(WorkloadDTO workloadDTO){
            Optional<WorkloadDTO> optionalWorkload= this.findWorkloadByName(workloadDTO.getName());
            if (optionalWorkload.isPresent()){
                return Optional.empty();
            }
            if (workloadDTO.getName() == null || workloadDTO.getName().isBlank()){
                throw new RuntimeException("O nome da Workload é obrigatório");
            }

        Workload workload = new Workload();
        copyDTOtoEntity(workloadDTO, workload);

        workload = workloadRepository.save(workload);

        return Optional.of(new WorkloadDTO(workload));

    }
</pre></code>

<pre><code>

package Oracle.Partner.Tracker.repositories;

import Oracle.Partner.Tracker.entities.Workload;

import org.springframework.data.jpa.repository.JpaRepository;

public interface WorkloadRepository extends JpaRepository <Workload,Long>{
    Workload findByName(String name);
}
    
</code></pre>
</details>


<details><Summary><b>Definição do backlog do produto.</b></Summary>



<table>
    <thead>
        <tr>
            <th>US</th>
            <th>Como Um</th>
            <th>Eu Preciso</th>
            <th>Para</th>
            <th>Prioridade</th>
            <th>Sprint</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Administrador</td>
            <td>Acessar um dashboard que apresente informações gerais sobre o sistema e os parceiros.</td>
            <td>Ter uma visão abrangente do contexto.</td>
            <td>Imprescindível</td>
            <td>1</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Administrador</td>
            <td>Importar um arquivo CSV com dados relevantes, e tê-lo tratado e incorporado na plataforma.</td>
            <td>Adicionar e atualizar os dados do sistema.</td>
            <td>Imprescindível</td>
            <td>1</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Administrador</td>
            <td>Utilizar filtros no dashboard, para visualização específicas de dados, como durante um período de tempo ou uma quantidade específica.</td>
            <td>Facilitar a análise de dados.</td>
            <td>Importante</td>
            <td>1</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Administrador</td>
            <td>Visualizar as OPN Tracks mais utilizadas em um campo dedicado no dashboard.</td>
            <td>Entender as áreas de maior interesse e atividade.</td>
            <td>Importante</td>
            <td>1</td>
        </tr>
        <tr>
            <td>5</td>
            <td>Administrador</td>
            <td>Visualizar quanto cada OPN Track representa do total de parceiros Oracle.</td>
            <td>Entender a popularidade das tracks.</td>
            <td>Desejável</td>
            <td>2</td>
        </tr>
        <tr>
            <td>6</td>
            <td>Administrador</td>
            <td>Visualizar a porcentagem da expertise total de cada parceiro Oracle.</td>
            <td>Entender a distribuição de habilidades dentro da plataforma.</td>
            <td>Desejável</td>
            <td>2</td>
        </tr>
    </tbody>
</table>

<br>
</details>

<br>
  <h2>Hard skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Descrição</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Construção de APIs RESTful</b></td> 
    <td>Desenvolvimento de APIs utilizando <b>Spring Boot</b>, seguindo padrões RESTful para facilitar a comunicação entre sistemas e garantir escalabilidade.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Implementação de CRUDs</b></td> 
    <td>Criação de operações de <b>CRUD</b> com <b>Spring Boot</b> e <b>JPA/Hibernate</b>, garantindo persistência de dados eficiente e segura.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Documentação de Endpoints</b></td> 
    <td>Uso de <b>Swagger/OpenAPI</b> para documentação clara e interativa de APIs, facilitando a integração com outros sistemas e desenvolvedores.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Otimização de Consultas SQL</b></td> 
    <td>Aplicação de boas práticas para <b>otimizar consultas</b> no banco de dados, reduzindo tempo de resposta e melhorando a performance das aplicações.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Interfaces Dinâmicas com Vue.js</b></td> 
    <td>Desenvolvimento de <b>interfaces interativas</b> e dinâmicas utilizando <b>Vue.js</b>, garantindo melhor experiência do usuário e integração eficiente com APIs.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Design Patterns e Boas Práticas</b></td> 
    <td>Aplicação de <b>padrões de projeto (Design Patterns)</b> e boas práticas no desenvolvimento para garantir código limpo, modular e reutilizável.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Uso de Lombok</b></td> 
    <td>Utilização do <b>Lombok</b> para reduzir código boilerplate em classes Java, tornando o desenvolvimento mais produtivo e organizado.</td> 
  </tr> 
</table>



<h2>Soft skills</h2>
<br>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Descrição</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Resolução de Problemas</b></td> 
    <td>Capacidade de identificar, analisar e solucionar problemas de software de forma eficiente, garantindo a estabilidade e desempenho da aplicação.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Diagnóstico de Erros</b></td> 
    <td>Uso de <b>logs do Spring Boot</b> para identificar e corrigir erros, analisando mensagens de erro e rastreando a origem dos problemas.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Debugging</b></td> 
    <td>Utilização das ferramentas de <b>debugging</b> no <b>IntelliJ</b> e <b>VS Code</b> para inspecionar variáveis, analisar a execução do código e corrigir falhas.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Gestão de Tempo e Organização</b></td> 
    <td>Planejamento eficaz das tarefas, priorizando demandas e garantindo a entrega dentro dos prazos estabelecidos.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Planejamento de Tarefas</b></td> 
    <td>Organização das atividades dentro dos <b>sprints</b>, garantindo alinhamento com a equipe e cumprimento dos objetivos do projeto.</td> 
  </tr> 
</table>


<h4>5ª API - 2º Semestre 2024</h4> 
<p align="justify">O problema apresentado pela empresa Pro4Tech está relacionado à eficiência e à eficácia no processo de recrutamento e seleção de pessoal. Atualmente, a empresa busca otimizar a maneira como os dados de recrutamento são coletados, visualizados e analisados. A "dor" central do cliente inclui a necessidade de centralizar e visualizar dados dispersos, permitir uma tomada de decisão estratégica, gerar relatórios personalizados e automatizar processos manuais, além de possibilitar a integração de dados de diferentes fontes.

O projeto de DataViz do ByteLabs é uma plataforma focada na análise de dados de recrutamento e seleção. Tem como objetivo oferecer insights valiosos como:

- Métricas de eficiência no recrutamento (ex. tempo médio de contratação, quantidade de contratações por processo seletivo).

- Identificação de padrões e tendências para otimizar o processo de seleção.

- Personalização de relatórios conforme as necessidades específicas dos gestores.

- A plataforma é voltada para gerentes de RH e analistas.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/c941a1f0-442e-4978-9dd7-6b577989e0ca" width="70%"></p>

    
[GIT](https://github.com/bytelabss/ByteLabss-API5sem)

<summary><b>Tecnologias Utilizadas</b></summary>
<br> 

![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white) 
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D) 
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white) 
<img src="https://img.shields.io/badge/spark-%2523ED8B00.svg?style=for-the-badge&logo=apache%20spark&color=white" alt="Apache Spark">
<img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">

</ul>
<b>Contribuições Pessoais</b>
</summary><br>
<p align="justify">Atuei como Desenvolvedora no projeto, implementando filtros para visualização de dados do processo seletivo para facilitar a visualização dos candidatos vinculados a cada processo. Desenvolvi endpoints dedicados para retornar informações sobre candidatos e processos seletivos, otimizando a navegação e análise dos dados. Além disso, fui responsável por implementar a Integração Contínua (CI) na equipe, automatizando os testes e o processo de build, o que contribuiu para maior agilidade e confiabilidade nas entregas.</p>
 

<details><Summary><b>Filtro por nome do processo seletivo para visualizar candidatos daquele processo</b></Summary>
    
![image](https://github.com/user-attachments/assets/b85ffa11-5249-409c-b051-dbf36dfb20c9)

![image](https://github.com/user-attachments/assets/c732b264-65cb-4582-b333-211b796117b2)

![image](https://github.com/user-attachments/assets/d5806e09-9617-4a22-8d4e-cfa0c876e3a6)

</details>

<details><Summary><b>Lista candidatos por determinado processo seletivo</b></Summary>
    
![image](https://github.com/user-attachments/assets/7d4ad903-951f-48e7-80a9-cd1474a868b8)
![image](https://github.com/user-attachments/assets/82a76a94-eef6-4fa7-851d-0d7bf79331ac)
![image](https://github.com/user-attachments/assets/20552e7e-5b96-447a-85b9-41a9d5889e9c)
![image](https://github.com/user-attachments/assets/ed1635e1-154b-4fd8-9ebc-9e6ba1585b5e)



</details>

<details><Summary><b>Integração Contínua (CI)</b></Summary>
    
<p align="justify">Fui responsável pela implementação da Integração Contínua (CI) da equipe, estruturando todo o fluxo de automação com base nas branches do projeto: BYTE, DEV, TESTE e MAIN. Configurei pipelines para execução de testes e validação de código a cada push em branch de feature (CI FEATURE ON PUSH), além de garantir validações automáticas durante os merges entre ambientes: da feature para DEV, de DEV para TESTE e de TESTE para MAIN. Essa organização permitiu uma maior segurança nas entregas, identificação precoce de falhas e uma padronização no processo de desenvolvimento e deploy, otimizando o fluxo de trabalho do time.</p>

![CI-Byte](https://github.com/user-attachments/assets/7cc35d80-b9be-47a4-8703-d4ffae78f374)

</details>


<details><Summary><b>Definição do backlog do produto.</b></Summary>

<body>
        <div align="center">
                <table>
                        <thead>
                                <th>Ranking</th>
                                <th>Requisito <b> funcional</b></th>
                                <th>User Story</th>
                                <th>Sprint</th>
                        </thead>
                        <tbody>
                                <tr>
                                        <td>US01</td>
                                        <td>1</td>
                                        <td align="justify">Eu, como gerente de RH, quero visualizar o tempo médio de contratações realizadas para cada processo seletivo em um período determinado, para poder avaliar a eficiência dos processos de recrutamento e identificar áreas de melhoria</td>
                                        <td>1</td>
                                </tr>
                                <tr>
                                        <td>US02</td>
                                        <td>1</td>
                                        <td align="justify">Eu, como analista de RH, quero visualizar o tempo médio de contratações realizadas para cada vaga em um período determinado, para que eu possa entender o desempenho das vagas individuais e melhorar a gestão de vagas futuras</td>
                                        <td>1</td>
                                </tr>
                                <tr>
                                        <td>US03</td>
                                        <td>1</td>
                                        <td align="justify">Eu, como gerente de RH, quero visualizar a quantidade de contratações realizadas por cada processo seletivo em um período específico, para que eu possa monitorar o progresso e a eficiência dos processos seletivos</td>
                                        <td>1</td>
                                </tr>
                                <tr>
                                        <td>US04</td>
                                        <td>1</td>
                                        <td align="justify">Eu, como analista de RH, quero visualizar a quantidade de contratações realizadas por cada participante de RH, em um período específico, para que eu possa avaliar a produtividade e desempenho individual dos recrutadores</td>
                                        <td>1</td>
                                </tr>
                                <tr>
                                        <td>US05</td>
                                        <td>7</td>
                                        <td align="justify">Eu, como gerente de RH, quero um processo de ETL que extraia, transforme e carregue os dados de processos seletivos, vagas, participantes de RH, contratações e tempos envolvidos, para que eu possa consolidar essas informações em um data warehouse e realizar análises mais eficazes para melhorar as decisões de recrutamento</td>
                                        <td>1</td>
                                </tr>
                                <tr>
                                        <td>US06</td>
                                        <td>3</td>
                                        <td align="justify">Eu, como analista de RH, quero poder gerar relatórios manualmente, em PDF e em Excel, para que eu possa estudar períodos específicos dos processos seletivos e tomar novas decisões de forma embasada</td>
                                        <td>2</td>
                                </tr>
                                <tr>
                                        <td>US07</td>
                                        <td>3</td>
                                        <td align="justify">Eu, como analista de RH, quero poder receber relatórios automáticos sazonais, em PDF e em Excel, para que eu possa estudar períodos específicos dos processos seletivos e tomar novas decisões de forma embasada</td>
                                        <td>2</td>
                                </tr>
                                <tr>
                                        <td>US08</td>
                                        <td>1</td>
                                        <td align="justify">Eu, como analista de RH, quero visualizar a pontuação de cada candidato por critério de avaliação, para cada vaga, para que eu possa avaliar objetivamente o desempenho dos candidatos e tomar decisões mais informadas no processo de contratação</td>
                                        <td>2</td>
                                </tr>
                                <tr>
                                        <td>US09</td>
                                        <td>5</td>
                                        <td align="justify">Eu, como analista de RH, quero receber alarmes na tela sempre que um dashboard padrão sair do ideal, para que eu possa fazer manobras estratégicas quando necessário</td>
                                        <td>3</td>
                                </tr>
                                <tr>
                                        <td>US10</td>
                                        <td>5</td>
                                        <td align="justify">Eu, como gerente de RH, quero receber alarmes na tela sempre que um dashboard padrão sair do ideal, para que eu possa fazer manobras estratégicas quando necessário</td>
                                        <td>3</td>
                                </tr>
                                <tr>
                                        <td>US11</td>
                                        <td>2</td>
                                        <td align="justify">Eu, como gerente de RH, quero poder criar e salvar consultas personalizadas na base de dados, para poder facilitar meu acesso</td>
                                        <td>3</td>
                                </tr>
                                <tr>
                                        <td>US12</td>
                                        <td>6</td>
                                        <td align="justify">Eu, como analista de RH, quero poder compartilhar minhas consultas personalizadas, para poder auxiliar outros usuários em suas atividades</td>
                                        <td>4</td>
                                </tr>
                                <tr>
                                        <td>US13</td>
                                        <td>6</td>
                                        <td align="justify">Eu, como gerente de RH, quero poder compartilhar minhas consultas personalizadas, para poder auxiliar outros em suas atividades</td>
                                        <td>4</td>
                                </tr>
                                <tr>
                                        <td>US14</td>
                                        <td>4</td>
                                        <td align="justify">Eu, como gerente de RH, quero poder cadastrar os novos membros de minha equipe, para que eles possam acessar o sistema</td>
                                        <td>4</td>
                                </tr>
                        </tbody>
                </table>
        </div>
</body>



<table>
    <thead>
        <tr>
            <th>US</th>
            <th>Como Um</th>
            <th>Eu Preciso</th>
            <th>Para</th>
            <th>Prioridade</th>
            <th>Sprint</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Administrador</td>
            <td>Acessar um dashboard que apresente informações gerais sobre o sistema e os parceiros.</td>
            <td>Ter uma visão abrangente do contexto.</td>
            <td>Imprescindível</td>
            <td>1</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Administrador</td>
            <td>Importar um arquivo CSV com dados relevantes, e tê-lo tratado e incorporado na plataforma.</td>
            <td>Adicionar e atualizar os dados do sistema.</td>
            <td>Imprescindível</td>
            <td>1</td>
        </tr>
        <tr>
            <td>3</td>
            <td>Administrador</td>
            <td>Utilizar filtros no dashboard, para visualização específicas de dados, como durante um período de tempo ou uma quantidade específica.</td>
            <td>Facilitar a análise de dados.</td>
            <td>Importante</td>
            <td>1</td>
        </tr>
        <tr>
            <td>4</td>
            <td>Administrador</td>
            <td>Visualizar as OPN Tracks mais utilizadas em um campo dedicado no dashboard.</td>
            <td>Entender as áreas de maior interesse e atividade.</td>
            <td>Importante</td>
            <td>1</td>
        </tr>
        <tr>
            <td>5</td>
            <td>Administrador</td>
            <td>Visualizar quanto cada OPN Track representa do total de parceiros Oracle.</td>
            <td>Entender a popularidade das tracks.</td>
            <td>Desejável</td>
            <td>2</td>
        </tr>
        <tr>
            <td>6</td>
            <td>Administrador</td>
            <td>Visualizar a porcentagem da expertise total de cada parceiro Oracle.</td>
            <td>Entender a distribuição de habilidades dentro da plataforma.</td>
            <td>Desejável</td>
            <td>2</td>
        </tr>
    </tbody>
</table>

<br>
</details>

<br>
  <h2>Hard skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Descrição</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Construção de APIs RESTful</b></td> 
    <td>Desenvolvimento de APIs utilizando <b>Spring Boot</b>, seguindo padrões RESTful para facilitar a comunicação entre sistemas e garantir escalabilidade.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Implementação de CRUDs</b></td> 
    <td>Criação de operações de <b>CRUD</b> com <b>Spring Boot</b> e <b>JPA/Hibernate</b>, garantindo persistência de dados eficiente e segura.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Documentação de Endpoints</b></td> 
    <td>Uso de <b>Swagger/OpenAPI</b> para documentação clara e interativa de APIs, facilitando a integração com outros sistemas e desenvolvedores.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Otimização de Consultas SQL</b></td> 
    <td>Aplicação de boas práticas para <b>otimizar consultas</b> no banco de dados, reduzindo tempo de resposta e melhorando a performance das aplicações.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Interfaces Dinâmicas com Vue.js</b></td> 
    <td>Desenvolvimento de <b>interfaces interativas</b> e dinâmicas utilizando <b>Vue.js</b>, garantindo melhor experiência do usuário e integração eficiente com APIs.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Design Patterns e Boas Práticas</b></td> 
    <td>Aplicação de <b>padrões de projeto (Design Patterns)</b> e boas práticas no desenvolvimento para garantir código limpo, modular e reutilizável.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Uso de Lombok</b></td> 
    <td>Utilização do <b>Lombok</b> para reduzir código boilerplate em classes Java, tornando o desenvolvimento mais produtivo e organizado.</td> 
  </tr> 
</table>



<h2>Soft skills</h2>
<br>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Descrição</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Resolução de Problemas</b></td> 
    <td>Capacidade de identificar, analisar e solucionar problemas de software de forma eficiente, garantindo a estabilidade e desempenho da aplicação.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Diagnóstico de Erros</b></td> 
    <td>Uso de <b>logs do Spring Boot</b> para identificar e corrigir erros, analisando mensagens de erro e rastreando a origem dos problemas.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Debugging</b></td> 
    <td>Utilização das ferramentas de <b>debugging</b> no <b>IntelliJ</b> e <b>VS Code</b> para inspecionar variáveis, analisar a execução do código e corrigir falhas.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Gestão de Tempo e Organização</b></td> 
    <td>Planejamento eficaz das tarefas, priorizando demandas e garantindo a entrega dentro dos prazos estabelecidos.</td> 
  </tr> 
  <tr> 
    <td align="center"><b>Planejamento de Tarefas</b></td> 
    <td>Organização das atividades dentro dos <b>sprints</b>, garantindo alinhamento com a equipe e cumprimento dos objetivos do projeto.</td> 
  </tr> 
</table>



