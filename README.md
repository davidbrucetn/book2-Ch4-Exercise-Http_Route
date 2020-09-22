# book2-Ch4-Exercise-Http_Route
Bk 2, Ch4 HTTP Req &amp; Routing Exercise Q&amp;A

```
Exercise
Given the following Controller methods, what can you infer about the HTTP request that would be made to execute them?
WalkersController.cs
public ActionResult Details(int id)
{
    ...
}
It would use the GET verb/method with the Walker.Id as the Parameter.
DogsController.cs
public ActionResult Edit(int id)
{
    ...
}
This would be using either the GET verb/method with the Dog.Id parameter.
TacosController.cs
public ActionResult Details(int id)
{
    ...
}
This would be using the GET verb/method with the Taco Id as a parameter.
DogsController.cs
[HttpPost]
public ActionResult Create(Dog dog)
{
    ...
}
This would be using the POST verb/method with the form data as the body.
DogsController.cs
[HttpPost]
public ActionResult Edit(int id, Dog dog)
{
    ...
}
Since it has {HttpPost] annotation, it would be using the PUT verb/method with the form data to be used on the server side.
 
Given the following HTTP requests, what would the controller method look like that would handle them?
path: /owners/index
method: GET
OwnersController.cs
public IActionResult Index()
        {
		....
        }
 
 
path: /owners/details/96
method: GET
OwnersController.cs
public IActionResult Details(int id)
        {
		....
        }
 
 
 
path: /dogs/create
method: GET
DogsController.cs
 public ActionResult Create()
        {
            ...
        }
 
path: /dogs/create
method: POST
body: 
    Name: Delta
    Breed: Golden Retriever
    Notes: She will chase squirrels
DogsController.cs 
  [HttpPost]
         public ActionResult Create(Dog dog)
        {
...
        }
 
 
path: walkers/delete/6
method: POST
body:
    Id: 6
    Name: Mellesa
    NeighborhoodId: 5
WalkersController.cs
 	 [HttpPost]
        [ValidateAntiForgeryToken]
        public ActionResult Delete(int id, IFormCollection collection)
        {
        ...
        }
