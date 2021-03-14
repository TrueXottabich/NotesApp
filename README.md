# NotesApp

# AddNote

Used to add and save new note in app.

**URL** : `/notes/`

**Method** : `POST`

**Auth required** : NO

**Data constraints**

```json
{
    "title": "note title, can be missed",
    "content": "note text"
}
```

**Data example**

```json
{
    "content" : "testContent1"
}
```

```json
{
    "title" : "testTitle1",
    "content" : "testContent1"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "id": 2,
    "title": "testTitle1",
    "content": "testContent1"
}
```


# GetAllNotes

Used to get all notes.

**URL** : `/notes/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "id": 1,
        "title": "newTitle1",
        "content": "newContent1"
    },
    {
        "id": 2,
        "title": "testConten",
        "content": "testContent1"
    },
    {
        "id": 3,
        "title": "testConten",
        "content": "testContent1"
    }
]
```


# GetNoteById

Used to get note by Id.

**URL** : `/notes/{id}`

**Method** : `GET`

**Auth required** : NO

**Data constraints**

PathParam {id} integer.

**Data example**

/notes/3


## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "id": 2,
    "title": "testTitle1",
    "content": "testContent1"
}
```



# Update Note

Used to update existing note in app.

**URL** : `/notes/{id}`

**Method** : `PUT`

**Auth required** : NO

**Data constraints**

PathParam {id} integer.

```json
{
    "title": "note title, can be missed",
    "content": "note text"
}
```

**Data example**

/notes/1

```json
{
    "title" : "newTitle1",
    "content" : "newContent1"
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
    "id": 1,
    "title": "newTitle1",
    "content": "newContent1"
}
```


# GetNoteByText

Used to get note by text.

**URL** : `/notes?query=text`

**Method** : `GET`

**Auth required** : NO

**Data constraints**

text is String parameter

**Data example**

/notes?query=title


## Success Response

**Code** : `200 OK`

**Content example**

```json
[
    {
        "id": 1,
        "title": "newTitle1",
        "content": "newContent1"
    },
    {
        "id": 2,
        "title": "testTitle1",
        "content": "testContent1"
    },
    {
        "id": 3,
        "title": "testTitle1",
        "content": "testContent1"
    }
]
```
