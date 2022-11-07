The design for this SDK is fairly straigh forward.  There is a class for each type of API call:
	Books
	Movies
	Characters
	Quotes
	Chapters

All of the classes inherit from the BaseRequest class which provides the following public methods:
	GetAll
	GetById
Any class specific functions (i.e. Movie Quotes, Book Chapters, and Character Quotes) are implemented on a class specific basis.

The BaseRequest also allows for setting filters, sorting, and pagination by instantiating the following objects with the appropriate data
	Sorting
	Filters
	Pagination
and assigning the object to the BaseRequest property associated with it.

All of the communication with the REST API is performned through the QueryAPI method in the BaseRequest class.

There is also a sample client (LOTR-Client) and NUnit Test project (LOTRSdk-Tests) included in the GIT repo.

