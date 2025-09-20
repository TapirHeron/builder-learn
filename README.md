<<<<<<< HEAD
A simple builder pattern demo

implements select delete insert update those DML

example
```
/**
*  select example
*
*/
  System.out.println(
                SQLQuery.selectBuilder()
                        .select("id", "name", "email")
                        .from("users")
                        .where(SQLQuery.whereBuilder()
                                .where("id = 1")
                                .where("name = 'John'")
                                .where("email = 'john@example.com'")
                                .build())
                        .build());


/**
*  update example
*
*/
        System.out.println(SQLQuery.updateBuilder()
                .update("users")
                .set(SQLQuery.setBuilder()
                        .set("name", "John Doe")
                        .set("email", "john@example.com")
                        .build())
                .where(SQLQuery.whereBuilder()
                        .where("id = 1")
                        .where("name = 'John'")
                        .build())
                .build());
/**
*  delete example
*
*/
        System.out.println(SQLQuery.deleteBuilder()
                .deleteFrom("users")
                .where(SQLQuery.whereBuilder()
                        .where("id = 1")
                        .where("name = 'John'")
                        .build())
                .build());

/**
*  insert example
*
*/
        System.out.println(SQLQuery.insertBuilder()
                .insertInto("users")
                .assign(SQLQuery.assginmentBuilder()
                        .assign("name", "John Doe")
                        .assign("email", "john@example.com")
                        .assign("password", "password")
                        .build())
                .build());

```
=======
# builder-learn
to learn builder pattern
>>>>>>> a24f9afd19d6b7c1b60d909e75c88c2de97cb2dd
