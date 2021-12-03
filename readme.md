# QA Restore names ([uk](readme.uk.md), [ru](readme.ru.md))
The database failed. Some users lost values from the `firstName` field, but
`user` object has a `fullName` field, so we can restore `firstName`.

Write tests for `restoreNames` function, that takes an array of `users` and set
correct `firstName` to users who do not have it or is equal to `undefined`. You
should not return anything from the function.

Example:
```
const users = [
  {
    firstName: undefined,
    lastName: 'Holy',
    fullName: 'Jack Holy',
  },
  {
    lastName: 'Adams',
    fullName: 'Mike Adams',
  },
];

restoreNames(users);

// users === [
  {
    firstName: 'Jack',
    lastName: 'Holy',
    fullName: 'Jack Holy',
  },
  {
    firstName: 'Mike',
    lastName: 'Adams',
    fullName: 'Mike Adams',
  },
];
```
