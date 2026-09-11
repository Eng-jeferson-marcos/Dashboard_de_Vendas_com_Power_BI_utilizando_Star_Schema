# Dashboard_de_Vendas_com_Power_BI_utilizando_Star_Schema
Atividade desenvolvida para o curso primeiros passos com Power BI da DIO, sob a supervisão da Juliana Mascarenhas

Realizei o Star Schema no DBdiagram.io web

Table Professor {
  idProfessor int [pk]
  Departamento_idDepartamento int [ref: > Departamento.idDepartamento]
}

Table Departamento {
  idDepartamento int [pk]
  Nome varchar(45)
  Campus varchar(45)
  idProfessor_coordenador int
}

Table Curso {
  idCurso int [pk]
  Departamento_idDepartamento int [ref: > Departamento.idDepartamento]
}

Table Disciplina {
  idDisciplina int [pk]
  Professor_idProfessor int [ref: > Professor.idProfessor]
}

Table Aluno {
  idAluno int [pk]
}

Table Matriculado {
  Aluno_idAluno int [ref: > Aluno.idAluno]
  Disciplina_idDisciplina int [ref: > Disciplina.idDisciplina]
}

Table Disciplina_Curso {
  Disciplina_idDisciplina int [ref: > Disciplina.idDisciplina]
  Curso_idCurso int [ref: > Curso.idCurso]
}

Table Pre_requisito {
  idPreRequisito int [pk]
}

Table Pre_requisito_Disciplina {
  Disciplina_idDisciplina int [ref: > Disciplina.idDisciplina]
  PreRequisito_idPreRequisito int [ref: > Pre_requisito.idPreRequisito]
}

<img width="1181" height="658" alt="image" src="https://github.com/user-attachments/assets/11ea1b9d-8f6f-4158-80c8-df62cfc2cd60" />
