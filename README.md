
<h1>Portfólio das APIs - Cauana Dias Costa</h1>

<h4>Introdução</h4>

<p align="justify">Trabalho de Graduação na modalidade Portfólio das Aprendizagens a partir de Projeto Integrador (APIs), apresentado na Faculdade de Tecnologia de São José dos Campos - curso: Banco de Dados.</p>

<h4>Sobre mim</h4>

<p align="center"><img src="https://github.com/Cauana/bertoti/assets/77700346/fa566986-fa26-4d55-9d05-57cb6117387c" width="30%"></p>

<p align="justify">Bacharel em Administração Pública pela Universidade Estadual Paulista (UNESP) e regularmente matriculada no 6º semestre do curso tecnólogo em Banco de Dados pela Faculdade de Tecnologia de São José dos Campos (FATEC).</p>

<p align="justify">Possuo experiência na área de Tecnologia, tive a oportunidade de realizar meu estágio na General Electric (GE Taubaté) por um ano, onde trabalhei com o desenvolvimento de um projeto de melhoria das traduções técnicas com termos de Engenharia utilizando VBA e Python. Além disso, atuei realizando tratamento de dados, dashboards para entendimento de listas de documentos e principalmente desenvolvimento de automações de processos.</p>

<p align="justify">Atualmente sou Assessora de Tecnologia do Banco do Brasil (BB), onde atuo como desenvolvedora Backend Java, em microsserviços que envolvem mensageria e APIs que recebem, processam e enviam transações.</p>

<p align="center">• <a href="https://www.github.com/Cauana">LinkedIn</a> • <a href="https://www.linkedin.com/in/cauanadias/">GitHub</a> •</p>

<h4>Meus Projetos</h4>

<h4>1ª API - 2º semestre 2022</h4> 
<p align="justify"> Os professores da FATEC, precisavam de uma forma prática de avaliar e visualizar o desempenho dos alunos em equipes Scrum durante as sprints. Ele queria centralizar as notas de autoavaliação, avaliação entre pares e avaliação do próprio professor, com base na Escala Likert, para todos os grupos da sala em um único sistema. A solução desenvolvida, chamada "Agile Assessment" foi um sistema que realiza a avaliação 360° entre os membros de uma equipe scrum, sendo uma avaliação de seus pares de equipe, a si mesmo e de professores, utilizando a Escala Likert como parâmetro.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/5063a5ed-99b7-4fff-ba57-8ea1fe8242ba" width="70%"></p>

    
<a href="https://github.com/Pythonators/API_semestre1_pythonators?tab=readme-ov-file">GitHub do projeto</a>

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

<table align="center" border="1" cellpadding="10" width="70%">
  <tr>
    <th align="center" width="30%"><b>Habilidade</b></th>
    <th align="center" width="70%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Python</b></td>
    <td><img src="https://geps.dev/progress/80" alt="80%"></td>
  </tr>
  <tr>
    <td align="center"><b>Lógica de Programação</b></td>
    <td><img src="https://geps.dev/progress/80" alt="80%"></td>
  </tr>
  <tr>
    <td align="center"><b>Flask</b></td>
    <td><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
  <tr>
    <td align="center"><b>Git</b></td>
    <td><img src="https://geps.dev/progress/50" alt="50%"></td>
  </tr>
  <tr>
    <td align="center"><b>HTML/CSS/JavaScript</b></td>
    <td><img src="https://geps.dev/progress/50" alt="50%"></td>
  </tr>
</table>

<h2>Soft Skills</h2>

<table align="center" border="1" cellpadding="10" width="60%">
  <tr>
    <th align="center"><b>Habilidade</b></th>
    <th align="center"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Comunicação Efetiva</b></td>
    <td><img src="https://geps.dev/progress/90" alt="90%"></td>
  </tr>
  <tr>
    <td align="center"><b>Trabalho em Equipe</b></td>
    <td><img src="https://geps.dev/progress/95" alt="95%"><td>
  </tr>
  <tr>
    <td align="center"><b>Resolução de Problemas</b></td>
    <td><img src="https://geps.dev/progress/60" alt="60%"></td>
  </tr>
  <tr>
    <td align="center"><b>Adaptabilidade</b></td>
    <td><img src="https://geps.dev/progress/85" alt="85%"></td>
  </tr>
</table>

<p>
  Participar de um grupo muito grande, com 10 pessoas, foi um desafio que exigiu o desenvolvimento de várias soft skills. Desde o início, precisei aprender não só a programar, mas também a entender como funciona uma metodologia ágil, como o Scrum, algo totalmente novo para mim. A comunicação se tornou essencial para alinhar ideias, distribuir tarefas e resolver conflitos naturais de um time grande. O trabalho em equipe foi constante, principalmente para manter a organização e cumprir os prazos definidos. Na prática, enfrentamos um grande problema técnico: começamos o projeto utilizando Tkinter, mas percebemos que seria inviável desenvolver todas as funcionalidades necessárias com essa tecnologia. Isso exigiu que todo o grupo se adaptasse rapidamente, tomasse decisões assertivas e migrasse para uma nova stack, o que, apesar das dificuldades, resultou em um projeto mais robusto e funcional. Todo esse processo fortaleceu muito minha capacidade de resolver problemas e me adaptar a mudanças.
</p>

    
<h4>2ª API - 1º semestre 2023</h4> 
<p align="justify">O produto em parceria com a 2RP é um sistema que realiza o controle de horas excedentes de colaboradores da empresa.Anteriormente, a empresa enfrentava desafios na gestão de horas, dependendo de várias planilhas, o que limitava a disponibilidade, flexibilidade e controle necessários. Em resposta, desenvolvemos uma aplicação que centraliza o controle de horas excedentes, distinguindo entre horas extras e sobreavisos. Essa aplicação também oferece recursos de aprovação ou reprovação das horas pelo gestor da equipe e pelo departamento de Recursos Humanos.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/47537933-29eb-4be1-9125-8afe2555c88a" width="70%"></p>


<a href="https://github.com/oJavaLi/API-2-Semestre">GitHub do projeto</a>

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

<table align="center" border="1" cellpadding="10" width="50%">
  <tr>
    <th align="center" width="70%"><b>Habilidade</b></th>
    <th align="center" width="30%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Java</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
  <tr>
    <td align="center"><b>Java Spring Framework</b></td>
    <td align="center"><img src="https://geps.dev/progress/65" alt="65%"></td>
  </tr>
  <tr>
    <td align="center"><b>Banco de Dados Relacionais (PostgreSQL)</b></td>
    <td align="center"><img src="https://geps.dev/progress/60" alt="60%"></td>
  </tr>
  <tr>
    <td align="center"><b>Git</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td>
  </tr>
  <tr>
    <td align="center"><b>RESTful APIs</b></td>
    <td align="center"><img src="https://geps.dev/progress/65" alt="65%"></td>
  </tr>
  <tr>
    <td align="center"><b>HTML/CSS/JavaScript</b></td>
    <td align="center"><img src="https://geps.dev/progress/55" alt="55%"></td>
  </tr>
  <tr>
    <td align="center"><b>Diagrama DER</b></td>
    <td align="center"><img src="https://geps.dev/progress/60" alt="60%"></td>
  </tr>
</table>

<h2>Soft Skills</h2>

<table align="center" border="1" cellpadding="10" width="50%">
  <tr>
    <th align="center" width="70%"><b>Habilidade</b></th>
    <th align="center" width="30%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Trabalho em Equipe</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td>
  </tr>
  <tr>
    <td align="center"><b>Resolução de Problemas</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
  <tr>
    <td align="center"><b>Gestão do Tempo</b></td>
    <td align="center"><img src="https://geps.dev/progress/65" alt="65%"></td>
  </tr>
    <tr>
    <td align="center"><b>Comunicação</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td>
  </tr>
<tr>
    <td align="center"><b>Resiliência</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
</table>

<p>
  Esse projeto marcou meu primeiro contato direto com <b>Java</b> e <b>Spring</b>. Apesar de já conhecer o grupo, tudo era novo para mim, desde a linguagem até o backend profissional.
  Trabalhamos com um <b>cliente real</b>, o que aumentou a responsabilidade sobre entregas e qualidade. Atuei pela primeira vez como <b>Scrum Master</b>, organizando o time e acompanhando o progresso.
</p>
<p>
  Também participei da criação do <b>Diagrama DER</b>, aprendendo modelagem de dados e sua importância no desenvolvimento.
  Fazer <b>apresentações externas</b> para clientes foi essencial para meu crescimento, melhorando minha comunicação.
</p>


<h4>3ª API - 2º semestre 2023</h4> 
<p align="justify">O produto 2Rponto é um sistema que realiza o controle de horas excedentes de colaboradores da empresa 2RP Net. A empresa parceira é conhecida por disponibilizar soluções para análise de informações em tempo real para tomada de decisões de negócios que precisam atender requisitos de tempo extremamente rigorosos. As soluções inovadoras e customizadas a diferenciam no mercado, assim como os serviços, permitem o crescimento de negócio e de seus resultados.</p>

<p align="center"><img src="https://github.com/Cauana/bertoti/assets/77700346/2c90ccaa-860e-44a9-afa8-b276b372905e" width="70%"></p>

<p align="justify">Anteriormente, a empresa enfrentava desafios na gestão de horas, dependendo de várias planilhas, o que limitava a disponibilidade, flexibilidade e controle necessários. Em resposta, desenvolvemos uma aplicação que centraliza o controle de horas excedentes, distinguindo entre horas extras e sobreavisos. Essa aplicação também oferece recursos de aprovação ou reprovação das horas pelo gestor da equipe e pelo departamento de Recursos Humanos. Além disso, inclui painéis de controle para os colaboradores visualizarem suas horas aprovadas ou reprovadas, enquanto gestores e RH podem monitorar as pendências de aprovação de seus respectivos usuários. </p>
    
<a href="https://github.com/oJavaLi/doisrponto?tab=readme-ov-file">GitHub do projeto</a>

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

<table align="center" border="1" cellpadding="10" width="50%">
  <tr>
    <th align="center" width="70%"><b>Habilidade</b></th>
    <th align="center" width="30%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Java</b></td>
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%"></td>
  </tr>
  <tr>
    <td align="center"><b>Java Spring Framework</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td>
  </tr>
  <tr>
    <td align="center"><b>Banco de Dados Relacionais (PostgreSQL)</b></td>
    <td align="center"><img src="https://geps.dev/progress/60" alt="60%"></td>
  </tr>
  <tr>
    <td align="center"><b>Git</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
  <tr>
    <td align="center"><b>RESTful APIs</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td>
  </tr>
  <tr>
    <td align="center"><b>Gestão de Backlog</b></td>
    <td align="center"><img src="https://geps.dev/progress/65" alt="65%"></td>
  </tr>
  <tr>
    <td align="center"><b>Definição de Requisitos</b></td>
    <td align="center"><img src="https://geps.dev/progress/60" alt="60%"></td>
  </tr>
</table>

<h2>Soft Skills</h2>

<table align="center" border="1" cellpadding="10" width="50%">
  <tr>
    <th align="center" width="70%"><b>Habilidade</b></th>
    <th align="center" width="30%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Comunicação Efetiva</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td>
  </tr>
  <tr>
    <td align="center"><b>Negociação</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td>
  </tr>
  <tr>
    <td align="center"><b>Tomada de Decisão</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
  <tr>
    <td align="center"><b>Visão Estratégica</b></td>
    <td align="center"><img src="https://geps.dev/progress/65" alt="65%"></td>
  </tr>
  <tr>
    <td align="center"><b>Empatia</b></td>
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%"></td>
  </tr>
  <tr>
    <td align="center"><b>Trabalho em Equipe</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td>
  </tr>
  <tr>
    <td align="center"><b>Resolução de Problemas</b></td>
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td>
  </tr>
</table>

<p>
  No meio do projeto, assumi o papel de <b>Product Owner</b> após a saída do anterior. Foi um desafio grande me adaptar e compreender rapidamente as responsabilidades, buscando sempre apoiar o time para manter o foco e garantir as entregas.
</p>

<h4>4ª API - 1º Semestre 2024</h4> 
<p align="justify">A Oracle Partner Tracker é uma plataforma inteligente de gerenciamento e análise de dados, capaz de interpretar, organizar e representar os dados do sistema OPN da empresa parceira Oracle. Entre os objetivos principais do projeto, se encontram a modernização do acompanhamento das empresas parceiras Oracle, assim como a visualização de dados de forma inteligente de Tracks e Expertises de cada empresa parceira, para facilitar a identificação de melhorias e de conclusões estratégicas.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/c6aad513-edad-42ed-bcfd-45cb2d8e1e72" width="70%"></p>

    
<a href="https://github.com/codecatss/API-BD4">GitHub do projeto</a>

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

<h2>Hard skills</h2>
<table align="center" border="1" cellpadding="10" width="100%">
  <tr>
    <th align="center" width="30%"><b>Habilidade</b></th>
    <th align="center" width="70%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Construção de APIs RESTful</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/85" alt="85%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Implementação de CRUDs</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/80" alt="80%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Documentação de Endpoints</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/75" alt="75%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Otimização de Consultas SQL</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/70" alt="70%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Interfaces Dinâmicas com Vue.js</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/50" alt="50%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Design Patterns e Boas Práticas</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/75" alt="75%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Uso de Lombok</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/70" alt="70%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Debugging</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/80" alt="80%">
    </td>
  </tr>
</table>

<h2>Soft skills</h2>
<br>
<table align="center" border="1" cellpadding="10" width="100%">
  <tr>
    <th align="center" width="30%"><b>Habilidade</b></th>
    <th align="center" width="70%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Resolução de Problemas</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/85" alt="85%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Diagnóstico de Erros</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/75" alt="75%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Gestão de Tempo e Organização</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/80" alt="80%">
    </td>
  </tr>
  <tr>
    <td align="center"><b>Planejamento</b></td>
    <td align="center">
      <img src="https://geps.dev/progress/80" alt="80%">
    </td>
  </tr>
</table>

<p style="max-width:600px; margin: 20px auto;">
  Esse projeto apresentou uma pressão técnica maior devido à sua complexidade, o que foi um desafio para mim, especialmente por não ter experiência prévia com <b>Vue.js</b>. 
  Foi um processo de aprendizado intenso para lidar com o frontend e integrar com o backend. 
  O uso constante de <b>debugging</b> e análise de logs foi fundamental para superar obstáculos e garantir a qualidade da entrega.
</p>


<h4>5ª API - 2º Semestre 2024</h4> 
<p align="justify">O problema apresentado pela empresa Pro4Tech está relacionado à eficiência e à eficácia no processo de recrutamento e seleção de pessoal. Atualmente, a empresa busca otimizar a maneira como os dados de recrutamento são coletados, visualizados e analisados. A "dor" central do cliente inclui a necessidade de centralizar e visualizar dados dispersos, permitir uma tomada de decisão estratégica, gerar relatórios personalizados e automatizar processos manuais, além de possibilitar a integração de dados de diferentes fontes.

O projeto de DataViz do ByteLabs é uma plataforma focada na análise de dados de recrutamento e seleção. Tem como objetivo oferecer insights valiosos como:

- Métricas de eficiência no recrutamento (ex. tempo médio de contratação, quantidade de contratações por processo seletivo).

- Identificação de padrões e tendências para otimizar o processo de seleção.

- Personalização de relatórios conforme as necessidades específicas dos gestores.

- A plataforma é voltada para gerentes de RH e analistas.</p>

<p align="center"><img src="https://github.com/user-attachments/assets/c941a1f0-442e-4978-9dd7-6b577989e0ca" width="70%"></p>

    
<a href="https://github.com/bytelabss/ByteLabss-API5sem">GitHub do projeto</a>

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

<h2>Hard skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Nível</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Desenvolvimento de APIs RESTful</b></td> 
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Integração com Frontend Vue.js</b></td> 
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Documentação com Swagger</b></td> 
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Integração Contínua (CI)</b></td> 
    <td align="center"><img src="https://geps.dev/progress/70" alt="90%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Conceitos de DevOps</b></td> 
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td> 
  </tr>
  <tr> 
    <td align="center"><b>Modelagem de Dados Analíticos</b></td> 
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>SQL e Spark para ETL</b></td> 
    <td align="center"><img src="https://geps.dev/progress/70" alt="70%"></td> 
  </tr>
</table>

<h2>Soft skills</h2>
<table align="center" border="1" cellpadding="10" width="100%"> 
  <tr> 
    <th align="center" width="30%"><b>Habilidade</b></th> 
    <th align="center" width="70%"><b>Nível</b></th> 
  </tr> 
  <tr> 
    <td align="center"><b>Resolução de Problemas</b></td> 
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Diagnóstico e Depuração</b></td> 
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Colaboração em Equipe</b></td> 
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Gestão Ágil de Tarefas</b></td> 
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%"></td> 
  </tr> 
  <tr> 
    <td align="center"><b>Responsabilidade Técnica</b></td> 
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%"></td> 
  </tr> 
</table>

<p>Foi desafiador entender e implementar práticas de DevOps, além de cumprir requisitos mais complexos dentro do projeto, como a prática de integração continua. Outro desafio importante foi o uso de Data Warehouse e processos ETL para integrar e analisar os dados de forma eficaz. A integração do time facilitou a resolução de problemas de forma mais eficaz utilizando conceitos ágeis adquiridos anteriormente.</p>


<h4>6ª API - 1º Semestre 2025</h4> 
<p align="justify">O problema apresentado pela empresa Kersys foi relacionado ao meio ambiente e o processo de reflorestamento de uma área. Assim, atuamos como facilitadores no processo de reflorestamento, desde a visualização da área do projeto em um mapa, até nas próprias estratégias de reflorestamento e no acompanhamento do processo como um todo.

A solução proposta pela equipe é desenvolver uma plataforma web, que permite o cadastro de uma área geográfica, e a partir dela, fazer um cruzamento com nossa base de dados e nossos modelos de inteligência artificial. O resultado desse cruzamento será um acompanhamento em tempo real e estratégias personalizadas para garantir a minimização de riscos e a maior taxa de sucesso possível para o projeto de reflorestamento. Além de insights valiosos como:

Métricas de saúde florestal da área. (ex. oxigenação, hidratação e tempo de vida do plantio).

Identificação de riscos e cuidados a ser tomados a partir de dados geográficos e climáticos da área.

Indicação de espécies de plantas para o plantio, baseados na época do ano e na longevidade desejada.

Geração de relatórios para acompanhamento retroativo do processo de reflorestamento.

<p align="center"><img src="https://github.com/user-attachments/assets/017d32d7-4dab-4618-9ef5-a9102f8d9c6f" width="70%"></p>

<a href="https://github.com/bytelabss/ByteLabs-API6Sem">GitHub do projeto</a>

<summary><b>Tecnologias Utilizadas</b></summary>
<br> 

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) 
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white) 
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white) 
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) 
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
 ![Jira](https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white) 
 ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) 
 ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) 
 ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)

</ul>
<b>Contribuições Pessoais</b>
</summary><br>
<p align="justify">Atuei como Product Owner (P.O.) e Desenvolvedora no projeto, mantendo contato direto com o cliente para entender suas necessidades e organizar o backlog da equipe, seguindo o processo definido pelo D.O.R (Definition of Ready) acordado coletivamente. Além disso, colaborei com a equipe para assegurar a correta implementação dos princípios da LGPD no sistema. Também participei do desenvolvimento de funcionalidades de inteligência artificial, como predições das melhores espécies para plantio em áreas específicas, considerando suas características e particularidades.</p>
 

<details><Summary>Definition of Ready (D.O.R)</Summary> 

Critérios gerais:
- A user story foi detalhada e compreendida por todos os envolvidos.
- Os critérios de aceitação estão claramente definidos.
- O backlog contém todas as informações necessárias.
- O design básico da interface com a ideia principal.
- O ambiente de desenvolvimento está preparado para implementação.


</details>

<details><Summary>Backlog do Produto</Summary>

<body>
        <div align="center">
                <table>
                        <thead>
                                <th>ID</th>
                                <th>Requisito <b> funcional</b></th>
                                <th>User Story</th>
                                <th>Sprint</th>
                                <th>Jira Link</th>
                        </thead>
                        <tbody>
                                <tr>
                                        <td>US01</td>
                                        <td align="center">2</td>
                                        <td align="justify">Como engenheiro ambiental, quero cadastrar, editar e visualizar novas áreas reflorestadas com informações detalhadas, para que o sistema possa monitorá-las corretamente.</td>
                                        <td align="center">1</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-1">LABS-1</a></td>
                                </tr>
                                <tr>
                                        <td>US02</td>
                                        <td align="center">2</td>
                                        <td align="justify">Como produtor, quero visualizar minhas áreas de plantio atualizadas em um mapa interativo, para acompanhar a distribuição geográfica e evolução.</td>
                                        <td align="center">1</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-3">LABS-3</a></td>
                                </tr>
                                <tr>
                                        <td>US03</td>
                                        <td align="center">-</td>
                                        <td align="justify">Como administrador, quero definir permissões de acesso para diferentes usuários (engenheiro ambiental e produtores), para garantir segurança e conformidade com a LGPD.</td>
                                        <td align="center">2</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-4">LABS-4</a></td>
                                </tr>
                                <tr>
                                        <td>US04</td>
                                        <td align="center">3</td>
                                        <td align="justify">Como engenheiro ambiental, quero ter acesso a uma base de dados confiável sobre reflorestamento do Brasil com dados sobre características do solo e da área, para compreender as necessidades e possibilidades de um terreno para reflorestamento.</td>
                                        <td align="center">1</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-2">LABS-2</a></td>
                                </tr>
                                <tr>
                                        <td>US05</td>
                                        <td align="center">-</td>
                                        <td align="justify">Como um engenheiro ambiental, quero que as ações do sistema estejam em conformidade com a LGPD.</td>
                                        <td align="center">-</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-26">LABS-26</a></td>
                                </tr>
                                <tr>
                                        <td>US06</td>
                                        <td align="center">1</td>
                                        <td align="justify">Como um engenheiro ambiental, quero receber recomendações sobre as melhores espécies para cada área, considerando as condições climáticas e características do solo, para garantir um reflorestamento eficiente.</td>
                                        <td align="center">2</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-31">LABS-31</a></td>
                                </tr>
                                <tr>
                                        <td>US07</td>
                                        <td align="center">4</td>
                                        <td align="justify">Como um engenheiro ambiental, quero identificar áreas sob risco de condições ambientais adversas, para tomar medidas preventivas.</td>
                                        <td align="center">3</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-32">LABS-32</a></td>
                                </tr>
                                <tr>
                                        <td>US08</td>
                                        <td align="center">1</td>
                                        <td align="justify">Como um produtor, quero visualizar diferentes estratégias de plantio, para avaliar seus impactos antes de implementar mudanças.</td>
                                        <td align="center">2</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-33">LABS-33</a></td>
                                </tr>
                                <tr>
                                        <td>US09</td>
                                        <td align="center">4</td>
                                        <td align="justify">Como um analista ambiental, quero visualizar indicadores-chave de reflorestamento de áreas sob riscos, para facilitar a tomada de decisão.</td>
                                        <td align="center">3</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-35">LABS-35</a></td>
                                </tr>
                                <tr>
                                        <td>US10</td>
                                        <td align="center">4</td>
                                        <td align="justify">Como um analista ambiental, quero gerar relatórios sobre o reflorestamento.</td>
                                        <td align="center">3</td>
                                        <td align="center"><a href="https://bytelabss.atlassian.net/browse/LABS-36">LABS-36</a></td>
                                </tr>
                        </tbody>
                </table>
        </div>
</body>
</details>

<details><Summary><b>Modelo de Classificação Área - Melhor tipo de espécie</b></Summary>

<code><pre>
from flask import Blueprint, request, jsonify
from marshmallow import ValidationError
from ..database import Session
import pandas as pd
import numpy as np
import os
from sklearn.impute import SimpleImputer
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.cluster import KMeans
import joblib

bp = Blueprint("models", __name__)

@bp.route('/treinar', methods=['POST'])
def treinar_kmeans():
    try:
        os.makedirs('models', exist_ok=True)

        df = pd.read_csv("dataforest/data/dados_amostragem.csv")

        X = df[["temperatura", "precipitacao", "altitude", "declividade", "exposicao",
                "distancia_vertical_drenagem", "densidade_drenagem", "cobertura_arborea"]]

        imputer = SimpleImputer(strategy="mean")
        X_imputed = pd.DataFrame(imputer.fit_transform(X), columns=X.columns)

        scaler = StandardScaler()
        X_scaled = scaler.fit_transform(X_imputed)

        inertia = []
        for i in range(1, 11):
            kmeans = KMeans(n_clusters=i, random_state=42)
            kmeans.fit(X_scaled)
            inertia.append(kmeans.inertia_)

        kmeans = KMeans(n_clusters=4, random_state=42)
        kmeans.fit(X_scaled)

        df['cluster'] = kmeans.labels_

        centroids = kmeans.cluster_centers_

        joblib.dump(kmeans, 'models/modelo_kmeans.pkl')
        joblib.dump(scaler, 'models/scaler.pkl')
        joblib.dump(imputer, 'models/imputer.pkl')
        joblib.dump(centroids, 'models/centroids.pkl')

        print("✅ Modelos salvos com sucesso!")

        df_especies = pd.read_csv("dataforest/data/areasxespecies.csv")

        X = df_especies.drop("target", axis=1)

        X_imputado = imputer.transform(X) 

        X_normalizado = scaler.transform(X_imputado)  

        clusters = kmeans.predict(X_normalizado)

        df_especies["cluster"] = clusters

        encoder = LabelEncoder()
        df_especies["target_encoded"] = encoder.fit_transform(df_especies["target"])
        joblib.dump(encoder, 'models/encoder.pkl')

        cluster_species = {}
        for cluster in df_especies['cluster'].unique():
            species_in_cluster = df_especies[df_especies['cluster'] == cluster]
            most_common_species = species_in_cluster['target_encoded'].mode()[0]
            species_name = encoder.inverse_transform([most_common_species])[0]
            cluster_species[int(cluster)] = species_name
        
        df_especies.to_csv("models/df_especies_clusters.csv", index=False)

        return jsonify({
            "mensagem": "Modelo treinado com sucesso!",
            "clusters": cluster_species
        })

    except Exception as e:
        return jsonify({"erro": str(e)}), 500
    

@bp.route('/classificar', methods=['POST'])
def classificar_area():
    try:

        kmeans = joblib.load('models/modelo_kmeans.pkl')
        scaler = joblib.load('models/scaler.pkl')
        imputer = joblib.load('models/imputer.pkl')
        encoder = joblib.load('models/encoder.pkl')


        df_especies = pd.read_csv("models/df_especies_clusters.csv")
        
        # Aqui é importante adicionar a regra que classifica todas as áreas já cadastradas após implementação da Lari
        # A ideia é - a lari coloca no banco a area já com essas caracteristicas do modelo
        # E depois a gente roda o classificador para todas essas áreas
        # Retorna essa recomendação na página 

        nova_area = request.get_json()  

        nova_area_df = pd.DataFrame([nova_area])

        X_imputed = imputer.transform(nova_area_df)

        X_normalizado = scaler.transform(X_imputed)

        cluster = kmeans.predict(X_normalizado)[0]

        species = df_especies[df_especies['cluster'] == cluster]['target'].mode()[0]

        cluster = int(cluster) 
        response = {
            "cluster": cluster,
            "species": species,
            "mensagem": "Área classificada com sucesso!"
        }

        return jsonify(response)

    except Exception as e:
        return jsonify({"erro": str(e)}), 500

</pre></code>
</details>


<h2>Hard Skills</h2>
<table align="center" border="1" cellpadding="10" width="100%">
  <tr>
    <th align="center" width="60%"><b>Habilidade</b></th>
    <th align="center" width="40%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Desenvolvimento de APIs RESTful (Python Flask)</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Integração com Frontend React + TypeScript</b></td>
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Implementação de Modelos de IA (scikit-learn, pandas)</b></td>
    <td align="center"><img src="https://geps.dev/progress/75" alt="75%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Modelagem e Manipulação de Dados (MongoDB / Postgres)</b></td>
    <td align="center"><img src="https://geps.dev/progress/80" alt="80%" width="150"></td>
  </tr>
  <tr>
    <td align="center"><b>Boas Práticas de LGPD em Desenvolvimento</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Gestão de Produto (Backlog, D.O.R, Jira)</b></td>
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Versionamento de Código (Git e GitHub)</b></td>
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%" width="100"></td>
  </tr>
</table>

<h2>Soft Skills</h2>
<table align="center" border="1" cellpadding="10" width="100%">
  <tr>
    <th align="center" width="60%"><b>Habilidade</b></th>
    <th align="center" width="40%"><b>Nível</b></th>
  </tr>
  <tr>
    <td align="center"><b>Visão de Produto e Foco no Cliente</b></td>
    <td align="center"><img src="https://geps.dev/progress/95" alt="95%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Tomada de Decisão Estratégica</b></td>
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Gestão Ágil de Projetos (Scrum, D.O.R)</b></td>
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Resolução de Problemas Complexos</b></td>
    <td align="center"><img src="https://geps.dev/progress/85" alt="85%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Comunicação com Stakeholders e Equipe</b></td>
    <td align="center"><img src="https://geps.dev/progress/95" alt="95%" width="100"></td>
  </tr>
  <tr>
    <td align="center"><b>Trabalho em Equipe e Colaboração</b></td>
    <td align="center"><img src="https://geps.dev/progress/90" alt="90%" width="100"></td>
  </tr>
</table>

<p>O maior desafio do projeto foi alinhar a visão do produto com as reais necessidades do cliente e dos agricultores, enquanto gerenciávamos a complexidade técnica de implementar modelos de inteligência artificial que realmente gerassem valor. A aplicação correta dos princípios da LGPD também foi um ponto crítico, garantindo a segurança dos dados sensíveis dos usuários. Este projeto foi uma oportunidade de crescimento tanto nas habilidades técnicas quanto nas competências de gestão de produto e liderança ágil.</p>
