# Express_GraphQL_MongoDB_Simple_Example

Simple Example for GraphQL - MongoDB local connection

connection : http://localhost:4000/graphql

Query Examples

Simple Query for users
query {
  users {
    id
    email
  }
}

Simple Query for posts
query {
  posts {
    id
    title
    content
    author {
      email
    }
  }
}

Mutation for Post
mutation($title: String!, $content:String!, $author:String!){
  createPost(title:$title, content:$content, author:$author){
    title
    content
    author{
      email
    }
  }
}

input args for Post
{
  "title": "test post for presentation",
  "content": "express graphql mongodb simple example",
  "author": "628dbfb841b9c97fe2995062"
}


Mutation for User
mutation($email: String!, $pwd:String!){
  createUser(email:$email, pwd:$pwd){
    id
    email
    pwd
  }
}