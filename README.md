## Bookstore REST API

This is REST based API to list, add, update and delete books.
As it for beginners there will be no 3rd party packages, authentication and DB

### Demo

![Alt Bookstore API](https://raw.githubusercontent.com/akilans/golang-mini-projects/main/demos/golang-bookstore-api.gif)

### Build and run

```bash
go build
./bookstore
# Access localhost:8080

# Import Bookstore-REST-API.postman_collection.json if you are using postman
```

### URL and sample request

- Get all the books - http://localhost:8080
- Get book by id - http://localhost:8080/book?id=1
- Delete book by id - http://localhost:8080/delete?id=5
- Add books - http://localhost:8080/add
- Update book - http://localhost:8080/add

```
# There is a typo in book id 5. We will update in next step
# Method POST
    [
        {
        "id": "4",
        "title": "Atomic Habits",
        "author": "James Clear",
        "price": "300",
        "image_url": "https://prodimage.images-bn.com/pimages/9780735211292_p0_v5_s600x595.jpg"
    },
    {
        "id": "5",
        "title": "The 4-hour workweekk",
        "author": "Tim Ferrisss",
        "price": "4000",
        "image_url": "https://images-eu.ssl-images-amazon.com/images/I/51iGkLC6jhL._SY264_BO1,204,203,200_QL40_FMwebp_.jpg"
    }
]

```

- Update book by id - http://localhost:8080/update

```
# Method POST
{
    "id": "5",
    "title": "The 4-hour workweek",
    "author": "Tim Ferriss",
    "price": "400",
    "image_url": "https://images-eu.ssl-images-amazon.com/images/I/51iGkLC6jhL._SY264_BO1,204,203,200_QL40_FMwebp_.jpg"
}

```

