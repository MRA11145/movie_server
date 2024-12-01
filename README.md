# Movie Server API

A simple RESTful API for managing movies and their directors, built with Go.

---

## Data Models

### Movie
```go
type Movie struct {
    ID       string   `json:"id"`
    Isbn     string   `json:"isbn"`
    Title    string   `json:"title"`
    Director Director `json:"director"`
}

type Director struct {
    FirstName string `json:"firstname"`
    LastName  string `json:"lastname"`
}
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/movies` | Get all movies |
| GET | `/movies/{id}` | Get a specific movie by ID |
| POST | `/movies` | Create a new movie |
| PUT | `/movies/{id}` | Update a movie by ID |
| DELETE | `/movies/{id}` | Delete a movie by ID |