# Как использовать
### Создать Calculation
```graphql
mutation createCalculation($planIndicatorId: ID){
  newCreateCalculation(
    planIndicatorId: $planIndicatorId,
    calculateData: {
      expressions: [
        {
          id: 1,
          function: SUM,
          elements: [
            {
              type: FIELD,
              content: 2
            }
          ]
        }
      ],
      fields: [
        {
          id: 2,
          fieldId: "QXZhaWxhYmxlRmllbGROYW1lOjYyOWRkMWI0NTA2MjI4Yjg5ODA4Mzk1ZQ==",
          function: "SUM"
        }
      ],
      executeId: 1,
    },
    filterFields: [],
    expressionType: BARE
  ) {
    calculation{
      id,
      expressions
    }
  }
}
```
### Исполнить Calculation

```graphql
mutation calculate{
  calculate(calculateDataId: "Q2FsY3VsYXRpb25EYXRhVHlwZToyOQ==") {
    response
  }
}
```
