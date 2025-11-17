## ১. Union এবং Intersection টাইপের ব্যবহার

TypeScript-এ Union টাইপ ব্যবহার করা হয় যখন কোনো ভ্যারিয়েবল একাধিক টাইপের হতে পারে। অন্যদিকে, Intersection টাইপ ব্যবহার করা হয় যখন আমরা একাধিক টাইপ একসাথে মিক্স করতে চাই।

**উদাহরণ:**

```typescript
// Union Type
let value: string | number;
value = "Hello";
value = 100;

// Intersection Type
type Person = { name: string };
type Contact = { phone: string };

type Employee = Person & Contact;

const employee: Employee = {
  name: "Najib",
  phone: "017XXXXXXXX"
};
```

এখানে `value` ভ্যারিয়েবলটি একবার string, আবার একবার number হতে পারে। আর `Employee` টাইপটি তৈরি হয়েছে দুটি টাইপ (`Person` এবং `Contact`) একত্র করে।



## ২. Enums এর ব্যবহার

Enum হলো TypeScript-এর একটি ফিচার যা কোনো নির্দিষ্ট মানের সেটকে একটি নাম দেওয়া সহজ করে। এটি কোডকে আরও পড়তে সহজ করে এবং ভুল কমায়।

### Numeric Enum উদাহরণ:

```typescript
enum Direction {
  Up = 1,
  Down,
  Left,
  Right
}

let move: Direction = Direction.Left;
```

### String Enum উদাহরণ:

```typescript
enum Status {
  Success = "SUCCESS",
  Fail = "FAIL",
  Pending = "PENDING"
}

let result: Status = Status.Success;
```

Numeric enum-এ মানগুলো সংখ্যা আকারে থাকে, আর string enum-এ মানগুলো স্ট্রিং আকারে থাকে।


