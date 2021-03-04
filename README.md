# React-Google-Books

## Table of Contents

- [Description](#description)

- [Deployed Link](#deployed-link)

- [TechnonlogyUse](#Technonlogy-Use)

- [License](#license)

- [Authors](#Authors)

- [Acknowledgments](#Acknowledgments)

## Description

This Google Books Search App to allow Users to search and save books. When a user search a book in the search bar and the books are generated, including an image of the cover page, title author, a description of the book. If the user clicks the save button then the book will be saved to their profile. The user also can see a list of their saved books.

## Video

![Video](./client/public/Books.gif)

## Deployed Link

- [Heroku Deploy](https://react-googlebooksapi-search.herokuapp.com/)

## Technonlogy Use

- React
- Bootstrap
- JavaScript
- CSS
- Express
- Axios
- Mongoose
- JSX

## Code Snippet

       module.exports = {
    create: function(req, res) {
        console.log("req.body ======>", req.body);
        db.Book.create(req.body)
        .then(dbModel => res.json(dbModel))
        .catch(err => res.status(422).json(err));
    },
    findAll: function(req, res) {
        console.log("req.query ==========>", req.query)
        db.Book.find(req.query)
        .then(dbModel => res.json(dbModel))
        .catch(err => res.status(422).json(err));
    },
    remove: function(req, res) {
        db.Book.findById({ _id: req.params.id })
        .then(dbModel => dbModel.remove())
        .then(dbModel => res.json(dbModel))
        .catch(err => res.status(422).json(err));
    }

     };

## License

![badge](https://shields.io/badge/license-MIT-green)

## Authors

1.  Abuye Mamuye

- [GitHub](https://github.com/AbuyeM1)

- [LinkedIn](https://www.linkedin.com/in/abuye-mamuye-5a49921b0/)

2.  William Bryan

- [GitHub](https://github.com/WeiLiBryan)

- [LinkedIn](https://www.linkedin.com/in/william-bryan-72730019a/)

3.  Spencer Christy

- [GitHub](https://github.com/spenrad)

- [LinkedIn](https://www.linkedin.com/in/spencer-christy/)

## Acknowledgments

- Jerome Chenette (Instructor)
- Manuel Nunes (TA)
- Mahisha Manikandan (TA)
- UC Berkeley Coding Bootcamp
