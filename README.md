# Sequelizejs-101
My note and troubleshoot for Sequelizejs

## Where conditions for association tables.
```
Company.find({
  include: {all: true},
  ...
  where: { ‘$employee.name$’: ‘Mr. A’ }
  ...
})
```

## To implement paging API use `findAndCountAll`
### If count rows is incorrect when use `findAndCountAll` function,  try to set `distinct: true`
```
Company.findAndCountAll({
    distinct:true,
    ...
    include: [{all:true}]
  }).then(function(results) {
    ...
  });
```

## Query data for `Page = 2` and `Total rows per page = 10`
```
Company.find({
    ...
    limit: 10
    ...
    offset: 1
  })
```

## Link to sequelize cli commands
https://github.com/sequelize/cli
