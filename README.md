# TypeScript Programming Notes

These notes help to aid my short term memory.

## Types, Interfaces, Unions, Enums, Classes!

### Types
- a type is low level
- types are closed 
- types cannot be augmented
- types can be composed into a new type

#### Extending types
- https://blog.logrocket.com/extending-object-like-types-interfaces-typescript

```typescript
type ToDoListItem = {
  title: string;
  completedDate: Date | null;
}
type ToDoList = {
  todos: ToDoListItem[];
}
type CalendarEvent = {
  title: string;
  start: Date;
  end: Date;
}
type Calendar = {
  events: CalendarEvent[];
}
type AppState = ToDoList & Calendar & {
  modified: Date;
}
```

### Interfaces
- an interface is high level
- interfaces are open
- interfaces can be augmented
- interfaces can be merged and remain the same interface
- interfaces can implement multiple interfaces

### Unions
- A simple union:
```typescript
type Union = "X" | "Y" | "Z";
```

- A union type describes a value that can be one of several types. We use the vertical bar ( | ) to separate each type, so number | string | boolean is the type of a value that can be a number , a string , or a boolean.
  - https://www.typescriptlang.org/docs/handbook/unions-and-intersections.html

### Enums

- https://www.typescriptlang.org/docs/handbook/enums.html

```typescript
enum Direction {
  Up = 1,
  Down,
  Left,
  Right,
}
```

### Classes
- classes are high level
- a class can implement interfaces

## Resources

### TypeScript Programming Language
- https://www.typescriptlang.org/
- https://www.typescriptlang.org/docs/

#### The TypeScript Handbook
- https://www.typescriptlang.org/docs/handbook/intro.html

#### The TypeScript Online Playground
- https://www.typescriptlang.org/play

#### Unions and Intersection Types
- https://www.typescriptlang.org/docs/handbook/unions-and-intersections.html
- https://www.typescriptlang.org/docs/handbook/2/types-from-types.html

#### Type vs Interface in TypeScript
- https://blog.bitsrc.io/type-vs-interface-in-typescript-cf3c00bc04ae

#### Exploring the satisfies operator in TypeScript
- https://dev.to/logrocket/exploring-the-satisfies-operator-in-typescript-22ab

#### Extending object-like types with interfaces in TypeScript
- https://blog.logrocket.com/extending-object-like-types-interfaces-typescript

