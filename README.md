# graphql-x-nodejs
simple graphql + nodejs
```
node server.js
```
server running : 
```
localhost:4000/graphql
```

```
{
    message
}
```

```
node server2.js
```
server running : 
```
localhost:4000/graphql
```

```
query getCourseWithFragments($courseID1: Int!, $courseID2: Int!) {
  course1: course(id: $courseID1) {
    ...courseFields
  }
  course2: course(id: $courseID2) {
    ...courseFields
  }
}

fragment courseFields on Course {
  title
  author
  description
  topic
  url
}

```


```
{ 
  "courseID1":1,
    "courseID2":2
}
```

