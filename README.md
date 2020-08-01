jQuery Resource
===

Provides a base class to handle REST resources for jQuery.ajax

## Table of Contents

- [jQuery Resource](#jquery-resource)
  - [Table of Contents](#table-of-contents)
  - [Install](#install)
    - [CDN](#cdn)
  - [Usage](#usage)
    - [post()](#post)
    - [add()](#add)
    - [create()](#create)
    - [get()](#get)
    - [find()](#find)
    - [patch()](#patch)
    - [update()](#update)
    - [put()](#put)
    - [replace()](#replace)
    - [delete()](#delete)
  - [License](#license)

## Install

### CDN

```html
<script src="https://cdn.jsdelivr.net/npm/jquery-resource@1.0.0-beta.2/dist/jquery.resource.min.js"></script>
```

## Usage

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// POST /api/users
userResource.post({
  email: 'george.bluth@reqres.in',
  first_name: 'George',
  last_name: 'Bluth'
});

// GET /api/users/1
userResource.get(1);

// PATCH /api/users/1
userResource.patch(1, {
  email: 'emma.wong@reqres.in',
  first_name: 'Emma',
  last_name: 'Wong'
});

// DELETE /api/users/1
userResource.delete(1);
```

### post()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// POST /api/users
userResource.post({
  email: 'george.bluth@reqres.in',
  first_name: 'George',
  last_name: 'Bluth'
}).done(function () {
  console.log('POST /api/users');
});
```

### add()

Alias of `post()` method.

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// POST /api/users
userResource.add({
  email: 'george.bluth@reqres.in',
  first_name: 'George',
  last_name: 'Bluth'
}).done(function () {
  console.log('POST /api/users');
});
```

### create()

Alias of `post()` method.

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// POST /api/users
userResource.create({
  email: 'george.bluth@reqres.in',
  first_name: 'George',
  last_name: 'Bluth'
}).done(function () {
  console.log('POST /api/users');
});
```

### get()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// GET /api/users/1
userResource.get(1).done(function () {
  console.log('GET /api/users/1');
});
```

### find()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// GET /api/users?first_name=George
userResource.find({
  first_name: 'George'
}).done(function () {
  console.log('GET /api/users?first_name=George');
});
```

### patch()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// PATCH /api/users/1
userResource.patch(1, {
  email: 'emma.wong@reqres.in',
  first_name: 'Emma',
  last_name: 'Wong'
}).done(function () {
  console.log('PATCH /api/users/1');
});
```

### update()

Alias of `patch()` method.

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// PATCH /api/users/1
userResource.update(1, {
  email: 'emma.wong@reqres.in',
  first_name: 'Emma',
  last_name: 'Wong'
}).done(function () {
  console.log('PATCH /api/users/1');
});
```

### put()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// PUT /api/users/1
userResource.put(1, {
  email: 'emma.wong@reqres.in',
  first_name: 'Emma',
  last_name: 'Wong'
}).done(function () {
  console.log('PUT /api/users/1');
});
```

### replace()

Alias of `put()` method.

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// PUT /api/users/1
userResource.replace(1, {
  email: 'emma.wong@reqres.in',
  first_name: 'Emma',
  last_name: 'Wong'
}).done(function () {
  console.log('PUT /api/users/1');
});
```

### delete()

```javascript
var userResource = new $.resource({
  endpoint: 'https://reqres.in/api/users'
});

// DELETE /api/users/1
userResource.delete(1).done(function () {
  console.log('DELETE /api/users/1');
});
```

## License

[MIT](./LICENSE)
