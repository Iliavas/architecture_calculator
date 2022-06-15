# Как использовать
### Создать Calculation
```graphql
mutation create {
  createOrUpdateIndicator(calculationData: {
    fields: [
      {
        id: 2,
        fieldId: "QXZhaWxhYmxlRmllbGROYW1lOjYyOWRkMWI0NTA2MjI4Yjg5ODA4Mzk1ZQ==",
        function: "SUM",
        countIf: {
          value: 1,
          field: "QXZhaWxhYmxlRmllbGROYW1lOjYyOWRkMWI0NTA2MjI4Yjg5ODA4Mzk1ZQ==",
          operator: "gt"
        }
      }
    ],
    expressions: [
      {
        id: 3,
        elements: [
          {
            content: 2,
            type: FIELD
          }
        ],
        function: SUM
      },
      {
        id: 1,
        elements: [
          {
            content: 2,
            type: FIELD
          },
          {
            content: 3,
            type: FIELD
          },
          {
            content: 5,
            type:LITERAL
          }
        ],
        function: SUM
      }
    ],
    executeId: 1,
  }, indicatorData:{
    name: "name"
  }) {
    indicator {
      id,
      newCalculation{
        id
      }
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
