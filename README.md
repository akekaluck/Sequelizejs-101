# Sequelizejs-101
Note for Sequelizejs

How to use condition for association tables?
Company.find({
  include: {all: true},
  where: { ‘$employee.name$’: ‘Mr. A’ }
})
