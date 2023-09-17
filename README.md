# BetterCanvasAPIDocs
This is meant to give an easier-to-read, and more detailed tutorial and documentation to use the Canvas LMS API for Python.


## Basic Setup

```
    import canvasapi

    TOKEN = <INSERT_TOKEN_HERE>
    BASE_URL = "https://<YOUR_SCHOOL_BASE_URL>"

    ##   A NOTE ON THE BASE_URL
    ## This may not function the same for everyone,
    ## however in my instance, this URL was 
    ## "osu.instructure.com"

    canvas_api = canvasapi.Canvas(BASE_URL,TOKEN)
```

To the owner of the API key, you will use the following function:

```
result = canvas_api.get_user('self')
```

The rest of this documentation and the tutorial will follow from this result variable.

From this point, to get the courses that a user is in, you will use `result.get_courses()`, which will return a `PaginatedList` object of all of the courses, which can be iterated through using a for loop, such as this example:

```
for course in result.get_courses():
    print(course.name)
```

### This will be continued soon.