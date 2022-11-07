# bret_cline-SDKThis is a basic SDK for the https://the-one-api.dev/documentation API.

The NuGet package for this SDK is located at https://www.nuget.org/packages/LOTRSdk/1.0.1 

The souce code for this SDK and associated projects is located at https://github.com/bretcline/bret_cline-SDK/tree/main/LOTR-SDK/LOTRSdk

The use of this SDK is fairly straight forwared but does require the use of an API Key from the-one-api.dev.

The package can be installed using NuGet using the Package Manager 
NuGet\Install-Package LOTRSdk -Version 1.0.1
or via the .NET CLI
dotnet add package LOTRSdk --version 1.0.1

The SDK can be tested using the NUnit Test project located at https://github.com/bretcline/bret_cline-SDK/tree/main/LOTRSdk-Tests

Some sample code is as follows:  

        var accessToken = "Your Access Token";

        var movies = new Movies(accessToken);
        var allmovies = movies.GetAll();

        foreach (var movie in allmovies)
        {
            Console.WriteLine(movie.Name);
        }
        var firstMovie = movies.GetByID(allmovies[2].Id);
        Console.WriteLine(firstMovie.Name);
        Console.WriteLine(firstMovie.AcademyAwardNominations);

As you can see it easily allows for getting a list of all movies, or a specifid movie based on the Id associated with the movie.

