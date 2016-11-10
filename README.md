# NSQ
NSQL Discipliona

# Exercicio 1
use aula2

db.Alunos.insert({ "name":"Briner Nunes", "birthday":ISODate("1988-11-07T2:00:00Z"), informations:{ cursadas:"IEL", cursando:"NSQ"} })

db.Alunos.insert({ "name":"Briner Nunes", "birthday":ISODate("1988-11-07T2:00:00Z"), informations:{ cursadas:"NSQ", cursando:"LKL"} })

db.Alunos.insert({ "name":"Eduardo MElo", "birthday":ISODate("1987-04-22T2:00:00Z"), informations:{ cursadas:"IEL", cursando:"NSQ",cursando:"IBD"} })

db.Alunos.insert({ "name":"Leonardo Quintao", "birthday":ISODate("1986-11-27T2:00:00Z"), informations:{ cursadas:"IEL",cursadas:"HJO", cursando:"NSQ",cursando:"IBD"} })

db.Alunos.find({},{birthday:1, _id: 0}).sort({birthday: 1})

db.Alunos.update({"name":"Briner Nunes",}, { $set:{"nota": 5} })

db.Alunos.remove({"name":"Eduardo MElo"})
