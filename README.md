# RestFulApiNotes

## RESTful API

A RESTful API (Representational State Transfer) is an architectural style for designing networked applications. It's based on a few key principles:

- **Stateless Communication**: Each request from a client to the server must contain all the information necessary to understand the request. The server doesn't store any client state between requests.

- **Client-Server Architecture**: The client and server are separate entities, each with their own concerns. The client is responsible for the user interface and user experience, while the server is responsible for storing and managing data, as well as processing requests.

- **Uniform Interface**: The interface between the client and the server should be uniform, meaning that the same set of standardized methods (like GET, POST, PUT, DELETE) should be applicable to all resources. Additionally, resources should be uniquely identifiable through URIs.

- **Resource-Based**: RESTful APIs treat data as resources that can be accessed and manipulated using standard HTTP methods. Each resource is identified by a unique URI.

- **Representation**: Resources are represented in a format that is easily understood by the client, typically JSON or XML. Clients can request different representations of a resource (e.g., JSON, XML) using content negotiation.

- **Statelessness**: As mentioned earlier, RESTful APIs are stateless, meaning that each request from a client to the server must contain all the necessary information to understand the request, and the server doesn't store any client state between requests.

# BEST PRACTICES
1. **Use Descriptive and Meaningful Resource Names**: Instead of generic or ambiguous names, choose resource names that accurately represent the entities they represent.

     ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/ba9287db-1c27-440a-a2f3-2e2e40c94e1b)

2. **Use HTTP Methods Correctly**: Use the appropriate HTTP methods (GET, POST, PUT, DELETE, PATCH, etc.) for different operations.
     ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/b010305a-f3b8-4e77-b35b-82f67a17c437)

3. **Version Your APIs**: Use versioning to ensure backward compatibility and allow for future enhancements without breaking existing clients.
    ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/83d59f7d-3091-4d11-9d28-c030d04d667d)

4. **Use HTTP Status Codes Correctly**: Return the appropriate HTTP status codes to indicate the success or failure of an API request.
   
   ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/691bfe3a-dba1-408a-86f6-4cded8de4fa8)

5. **Pick Your JSON Field Naming Convention (and Stick to It)**: JSON standard doesn’t impose a field naming convention, but it’s a best practice to pick one and stick with it.
   
   ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/ca9e7408-6b30-4579-a1b4-88dd24160794)

6. **Use Consistent Error Messages**:
   - In most cases, HTTP status codes are not enough to explain what went wrong. To help your API consumers, include a structured JSON error message.
   - The response should include the following information:
     - Error code: A machine-readable error code that identifies the specific error condition.
     - Error message: A human-readable message that provides a detailed explanation of the error.
     - Error context: Additional information related to the error, such as the request ID, the request parameters that caused the error, or the field(s) in the request that caused the error.
     - Error links: URLs to resources or documentation that provide additional information about the error and how it can be resolved.
     - Timestamp: The time when the error occurred.
 7. **Use Query Parameters for Filtering, Sorting, and Searching**:Query parameters allow you to provide additional information in the URL of an HTTP request to control the response returned by the server.

    ![image](https://github.com/rahulbasutkar04/RestFulApiNotes/assets/115400916/ab3b7a8a-5edc-4d06-9857-7497aedf9f1c)

 8. **Implement Authentication and Authorization**:Secure your APIs by implementing proper authentication and authorization mechanisms.
     Authentication:
    - Use API keys, tokens, or OAuth 2.0 for authentication.
     Authorization:
    - Apply Role-Based Access Control (RBAC) for authorization.

 9. **Do Not Maintain State**:A REST API should not maintain a state on the server. That’s the responsibility of the client. This ensures the API is cacheable, scalable, and decoupled from the client.

10. **Document Your APIs**:Provide comprehensive documentation for your APIs, including endpoint details, request/response examples, and usage guidelines.
- Use Swagger/OpenAPI documentation or Markdown-based documentation (e.g., Swagger UI or Redoc).


## PUT VS PATCH

| Feature        | PUT                             | PATCH                                   |
|----------------|---------------------------------|-----------------------------------------|
| **Purpose**    | Updates a resource entirely     | Applies partial modifications to a resource |
| **Request Body** | Entire resource representation | Instructions for partial modifications  |
| **Idempotent** | Yes                             | Yes (if the same set of changes is applied repeatedly) |
| **Usage**      | Full updates                   | Partial updates                        |
| **Impact**     | Replaces entire resource        | Modifies specific parts of the resource |


for more : https://www.geeksforgeeks.org/what-is-the-difference-between-put-post-and-patch-in-restful-api/


