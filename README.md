# The-Best-Text-Editor

## Description

This is THE best Text Editor, it is a simple text editor that allows you to type out your notes or texts and install them using webpack and node.js.

[Visit My Live Site on Heroku](https://dry-caverns-84097.herokuapp.com/)

![Screenshot](/Assets/Screenshot%202023-05-26%20111037.png)

## Table of Contents

- [Usage](#usage)
- [Code Snippets](#code-snippets)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Usage

1. Clone the repository or download the source code files.
2. Make sure you have Node.js and npm installed on your machine.
3. You can run the program locally by running the following commands:

```bash
npm build
npm start
```

4. The program should now be running on `http://localhost:3000`.
5. If you want to just visit the live site click this link: [Visit My Live Site on Heroku](https://dry-caverns-84097.herokuapp.com/)

## Code Snippets

This is my put and get methods that I used to save the data to the database in my database.js:

```javascript
// put method that accepts some content and adds it to the database
export const putDb = async (content) => {
  const db = await openDB("jate", 1);
  const tx = db.transaction("jate", "readwrite");
  const store = tx.objectStore("jate");
  await store.put({ content });
  await tx.done;
};

// get method that gets all the content from the database
export const getDb = async () => {
  const db = await openDB("jate", 1);
  const tx = db.transaction("jate", "readonly");
  const store = tx.objectStore("jate");
  return store.getAll();
};
```

## Technologies Used

The following technologies and tools were used to create this application:

- Node.js
- Express.js
- JavaScript
- Webpack
- inject manifest
- Babel

## My links

### \* [Portfolio](https://bryannguyen9.github.io/Bryan-Nguyen-Portfolio/)

### \* [LinkedIn](https://linkedin.com/in/bryannguyen9)

### \* [Github](https://github.com/bryannguyen9)

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, please feel free to open an issue or submit a pull request.

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is licensed under the MIT License. For more information, please see the [LICENSE](./LICENSE) file.
