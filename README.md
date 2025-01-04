# Assignment-2-Lexical-Scoping
Peer-graded Assignment: Programming Assignment 2: Lexical Scoping

Instructions

This programming assignment requires you to write an R function that can cache potentially time-consuming computations. For example, calculating the mean of a numeric vector is typically a fast operation. However, for a very long vector, it may take too long to compute the mean, especially if it has to be computed repeatedly (e.g., in a loop). If the contents of a vector are not changing, it makes sense to cache the value of the mean so that when it is needed again, it can be looked up in the cache rather than recomputed. This programming assignment will take advantage of the scoping rules of the R language and how they can be manipulated to preserve state inside an R object.

Assignment: Caching the Inverse of a Matrix

Matrix inversion is usually a costly computation, and there may be some benefit to caching the inverse of a matrix rather than computing it repeatedly. The assignment is to write a pair of functions that cache the inverse of a matrix:

makeCacheMatrix: This function creates a special "matrix" object that can cache its inverse.

cacheSolve: This function computes the inverse of the special "matrix" returned by makeCacheMatrix. If the inverse has already been calculated (and the matrix has not changed), then cacheSolve should retrieve the inverse from the cache.

Computing the inverse of a square matrix can be done with the solve function in R. For example, if X is a square invertible matrix, then solve(X) returns its inverse.

For this assignment, the matrix supplied is always invertible.
