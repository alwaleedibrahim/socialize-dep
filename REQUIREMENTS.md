# Requirements

## Roles
```
Users {
    Signup
    Login
    Update profile
    Create groups and become thier admin
}

Groups:
Admin {
    Accept join requests
    Add admin
    delete posts
}

Members {
    Send join requests to groups
    Show posts
    Add posts
    Delete own posts
    Edit own posts
    upvote posts
    downvote posts
    add comments
}
```

## db tables
```
user
    email (unique)
    displayname
    password
    profile picture
    bio

group
    id (unique)
    name
    members [ref:user.email]
    admins [ref:user.email]
    posts [
        id (unique)
        content
        time
        votes
        group(ref:group.id)
        user(ref:user.email)
        comments [
            user(ref:user.email)
            content
            time
        ]
    ]

```
routes
- signup
- login
- update profile
- create group
- add admin
- 
- 

file structure

index.js
models/
    dbconnection/
        dbconnection.js
    user

