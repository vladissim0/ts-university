# University Management System (TypeScript)

Practice project (session 09): OOP architecture in TypeScript.

## Concepts demonstrated
| Concept | Where |
| --- | --- |
| Abstract class + inheritance (IS-A) | `Person` → `Student`, `Teacher` → `Professor`, `AssociateProfessor` |
| Encapsulation + validation | `Person.email` getter/setter, private `Student._grades` |
| Aggregation (weak HAS-A) | `Course` → `Teacher`, `AcademicGroup` → `Student` |
| Composition (strong HAS-A) | `Faculty` creates and removes its `AcademicGroup`s |
| Interfaces + generics | `Identifiable`, `IRepository<T, ID>`, `InMemoryRepository<T>` |

## Run
```bash
npm install
npm run dev      # runs src/main.ts with tsx
# or
npm start        # compiles to dist/ and runs with node
```

## Structure
```
src/
  basic-contracts.ts   interfaces and types
  person-hierarchy.ts  Person, Student, Teacher, Professor, AssociateProfessor
  learning-units.ts    Course, AcademicGroup
  faculty.ts           Faculty (composition)
  repository.ts        IRepository, InMemoryRepository (with findWhere)
  main.ts              demo scenario
```
