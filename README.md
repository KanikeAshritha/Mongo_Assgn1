# Mongo_Assgn1
<pre>
db.todo_table.insertOne({task : "Play",
status:"Not done"})
{
  acknowledged: true,
  insertedId: ObjectId('6836e42631485535101b391b')
}
db.todo_table.insertMany([
  {task : 'dance',status: "Not done"},
  {task : 'sing',status :" Not done"},
  {task : 'Study',status : "Done"}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e49431485535101b391c'),
    '1': ObjectId('6836e49431485535101b391d'),
    '2': ObjectId('6836e49431485535101b391e')
  }
}
db.todo_table.updateMany({status : "Done"},
                         {$set : {status:true})
SyntaxError: Unexpected token, expected "," (2:46)

[0m [90m 1 |[39m db[33m.[39mtodo_table[33m.[39mupdateMany({status [33m:[39m [32m"Done"[39m}[33m,[39m
[31m[1m>[22m[39m[90m 2 |[39m                          {$set [33m:[39m {status[33m:[39m[36mtrue[39m})
 [90m   |[39m                                               [31m[1m^[22m[39m[0m
db.todo_table.updateMany({status : "Done"},
                         {$set : {status:true}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : "Not Done"},
                         {$set : {status:false})
SyntaxError: Unexpected token, expected "," (2:47)

[0m [90m 1 |[39m db[33m.[39mtodo_table[33m.[39mupdateMany({status [33m:[39m [32m"Not Done"[39m}[33m,[39m
[31m[1m>[22m[39m[90m 2 |[39m                          {$set [33m:[39m {status[33m:[39m[36mfalse[39m})
 [90m   |[39m                                                [31m[1m^[22m[39m[0m
db.todo_table.updateMany({status : "Not Done"},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : 'Not Done'},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: 'Not done'
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : 'Not done'},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 2,
  modifiedCount: 2,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: ' Not done'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
db.todo_table.updateMany({status : ' Not done'},
                         {$set : {status:false}})
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
db.todo_table.insertMany([
  {task : 'shopping',status: true},
  {task : 'go for a walk',status :false},
  {task : 'chill with friends',status : true}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e5c231485535101b391f'),
    '1': ObjectId('6836e5c231485535101b3920'),
    '2': ObjectId('6836e5c231485535101b3921')
  }
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true
}
db.todo_table.insertMany([
  {task : 'Eat',status: false},
  {task : 'Sleep',status :true},
  {task : 'Talk to parents',status : true}
])
{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId('6836e6b131485535101b3922'),
    '1': ObjectId('6836e6b131485535101b3923'),
    '2': ObjectId('6836e6b131485535101b3924')
  }
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true
}
db.todo_table.updateMany(
  { status: { $exists: false } },
  { $set: { status: false } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.insertOne([
  {task : 'Clockout'}
])
{
  acknowledged: true,
  insertedId: ObjectId('6836e8fe31485535101b3925')
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6836e8fe31485535101b3925')
}
db.todo_table.updateOne([
  {_id : '6836e8fe31485535101b3925'},
  {$set : {status : True}}
])
ReferenceError: True is not defined
db.todo_table.updateOne([
  {_id : '6836e8fe31485535101b3925'},
  {$set : {status : true}}
])
MongoInvalidArgumentError: Update document requires atomic operators
db.todo_table.updateOne([
  {_id : ObjectId('6836e8fe31485535101b3925')},
  {$set : {status : true}}
])
MongoInvalidArgumentError: Update document requires atomic operators
db.todo_table.updateOne(
  {_id : ObjectId('6836e8fe31485535101b3925')},
  {$set : {status : true}}
)
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6836e8fe31485535101b3925'),
  status: true
}
db.todo_table.updateMany(
  { status: { $exists: true } },
  { $push: { updateAt: new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.todo_table.updateMany(
  { status: { $exists: true } },
  { $push: { createdAt: new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.runCommand({
  collMod: "todo_table",
  validator: {
    $jsonSchema: {
      bsonType: "object",
      properties: {
        priority: {
          enum: ["low", "medium", "high"]
        }
      }}}})
{ ok: 1 }
db.todo_table.updateMany(
  { name: { $exists: true } },
  { $set: { priority : "medium" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.updateMany(
   { name: { $exists: true } },
  { $set: { priority : "medium" } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6836e8fe31485535101b3925'),
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ]
}
db.todo_table.updateMany(
  { priority: { $exists: false } },  
  { $set: { priority: "low" } }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.todo_table.updateMany(
  { task : 'Clock in'},  
  { $set: { priority: "low" } }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 0,
  modifiedCount: 0,
  upsertedCount: 0
}
db.todo_table.updateMany(
  { task : 'Clock in',status : 'false'}      
);
MongoInvalidArgumentError: Update document requires atomic operators
db.todo_table.insertOne(
  { task : 'Clock in',status : 'false'}      
);
{
  acknowledged: true,
  insertedId: ObjectId('6836ef5131485535101b3926')
}
db.todo_table.updateOne(
  { task : 'Clock in'},  
  { $set: { status: true ,updatedAt : new Date()} }       
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 1,
  modifiedCount: 1,
  upsertedCount: 0
}
db.todo_table.find()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6836e8fe31485535101b3925'),
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836ef5131485535101b3926'),
  task: 'Clock in',
  status: true,
  updatedAt: 2025-05-28T11:12:14.430Z
}
db.todo_table.countDocuments()
12
db.todo_table.find().sort()
{
  _id: ObjectId('6836e42631485535101b391b'),
  task: 'Play',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391c'),
  task: 'dance',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391d'),
  task: 'sing',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e49431485535101b391e'),
  task: 'Study',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b391f'),
  task: 'shopping',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b3920'),
  task: 'go for a walk',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e5c231485535101b3921'),
  task: 'chill with friends',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3922'),
  task: 'Eat',
  status: false,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3923'),
  task: 'Sleep',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836e6b131485535101b3924'),
  task: 'Talk to parents',
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  '0': {
    task: 'Clockout'
  },
  _id: ObjectId('6836e8fe31485535101b3925'),
  status: true,
  updateAt: [
    2025-05-28T10:51:15.761Z
  ],
  createdAt: [
    2025-05-28T10:51:24.829Z
  ],
  priority: 'low'
}
{
  _id: ObjectId('6836ef5131485535101b3926'),
  task: 'Clock in',
  status: true,
  updatedAt: 2025-05-28T11:12:14.430Z
}
db.todo_table.updateMany(
  { task: { $exists: true } },
  { $set: { dueDate : new Date() } }
);
{
  acknowledged: true,
  insertedId: null,
  matchedCount: 11,
  modifiedCount: 11,
  upsertedCount: 0
}
db.todo_table.find(
  {dueDate : {$eq : new Date()}}
);
db.todo_table.find(
  {dueDate : {$eq : new Date(28)}}
);
todo
Selection deleted
</pre>
