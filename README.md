# mongodb-query

mongo
use academic

db.createCollection("departement")
db.createCollection("student")
show collections

db.getCollectionInfos({name: departement})

db.departement.insert({
  code: "XI911",
  name: "Science Skill",
  major: "Phd"
})

db.departement.insert({
  code: "XII922",
  name: "Biology Skill",
  major: "Phd"
})

db.departement.insert({
  code: "XI933",
  name: "Math Skill",
  major: "NOOB"
})

db.departement.insert({
  code: "BI944",
  name: "Computer Skill",
  major: "PRO AS FUCK"
})

db.departement.insert({
  code: "CI922",
  name: "Jumping skill",
  major: "Not good"
})

db.student.insert({
  studentId: "1",
  name: "Adam",
  address: "Bangka 2",
  departement: ObjectId("58b644f033716d9ca4ad8912")
})

db.student.insert({
  studentId: "1",
  name: "Citra",
  address: "Pondok Indah",
  departement: ObjectId("58b6467d33716d9ca4ad8914")
})


db.student.insert({
  studentId: "1",
  name: "Akbar",
  address: "Blok S",
  departement: ObjectId("58b6467d33716d9ca4ad8916")
})

db.student.insert({
  studentId: "3",
  name: "Devi",
  address: "Pondok Pinang",
  departement: ObjectId("58b6467d33716d9ca4ad8914")
})


db.student.insert({
  studentId: "4",
  name: "Indah",
  address: "Pejaten",
  departement: ObjectId("58b6467d33716d9ca4ad8916")
})

db.student.find({}, {_id: 0, name: 1, address: 1})

db.student.find({studentId: "3"}, {_id: 0, name: 1, address: 1, studentId: 1})

db.student.find({}, {name: 1}).sort({"name":-1})
db.student.find({}, {name: 1}).sort({"name":1})

db.departement.find({}, {name: 1}).sort({"name":-1})
db.departement.find({}, {name: 1}).sort({"name":1})

db.student.find({name: "Adam"})
