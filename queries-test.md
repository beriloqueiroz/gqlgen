***
mutation createCourse {
  createCourse(input: {
    name: "arduino 2",
    description: "curso 2",
    categoryId : "f2041bc8-f4ee-4c76-abce-4254f6881f63"
  }) {
    id
  }
}

mutation createCategory {
  createCategory(input: {
    name: "eletronica 2",
    description: "categoria 2",
  }) {
    id
  }
}

query listCategories {
 categories{
    id
    name
    description
    courses {
   id
      description
      name
      category{
        id
        name
      }
    }
  }
}

query listCourses {
 courses{
    id
    name
    description
    category {
      id
      name
    }
  }
}
***
