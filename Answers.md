## Answers to Question 1 and 2

### 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

The relationship between the Product and Product_category entities is a one-to-many relationship. This means that one product can belong to only one category, but one category can have multiple products. In terms of database design, this relationship is typically represented by a foreign key column in the Product table that references the primary key column in the Product_Category table. In Java with Hibernate ORM, the relationship between the Product and Product_Category entities is typically represented using annotations such as @ManyToOne and @OneToMany. To be more specific the Product entity contains a @ManyToOne annotation referring to the Product_Category entity, indicating that each product belongs to a single category. In the same way, the Product_Category entity contain a @OneToMany annotation, specifying that each category can have multiple associated products. These annotations establish the one-to-many relationship between the entities.

### 2. How could you ensure that each product in the "Product" table has a valid category assigned to it?

To ensure that each product in the Product table has a valid category to it, we can use database constraints like foreign key constraint between the category_id column in the Product table and the primary key column in the Product_Category table. In Java with Hibernate ORM, we can use the @JoinColumn annotation in the Product entity to specify the foreign key column that maps to the primary key column in the Product_Categry entity. Additionally we can use validation annotations such as @NutNull or attribute nullable=false along with the @JoinColumn to ensure that the associated category is not null when saving a Product entity.

