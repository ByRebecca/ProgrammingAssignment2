# ProgrammingAssignment2


    ## Créer une matrice sépciale qui peut calculer l'inverse. 
    makeCacheMatrix <- function( m = matrix() ) {

	  ## Proprité de l'inverse
    i <- NULL

    ## La méthode pour faire la martrice
    set <- function( matrix ) {
            m <<- matrix
            i <<- NULL
    }

    
    get <- function() {
    	## Return the matrix
    	m
    }

    ## Comment avoir l'inverse de la matrice
    setInverse <- function(inverse) {
        i <<- inverse
    }


    ##Calculer l'inverse de la matrice spéciale renvoyée par "makeCacheMatrix"
    ## au-dessus de. Si l'inverse a déjà été calculé (et que la matrice n'a pas
    ## modifié), alors le "cachesolve" devrait récupérer l'inverse du cache.
    cacheSolve <- fonction(x, ...) {

    ## Avoir une matrice qui matrice qui est l'inverse de 'x'
    m <- x$getInverse()

    
    if( !is.null(m) ) {
            message("getting cached data")
            return(m)
    }

    
    data <- x$get()

    
    m <- solve(data) %*% data

    
    x$setInverse(m)

    ## Avoir la matrice m 
    m
    }
