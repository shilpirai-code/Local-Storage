# Local-Storage

In an Angular application, there are multiple ways to store information for various purposes

The choice of storage mechanism depends on factors such as the 
1. lifetime of the data
2. the need for persistence 
3. security considerations

Below are some common approaches to store information in an Angular app:

**1. Component State (In-Memory Storage)**  
**Description:** Each Angular component can store information in its internal state (class properties). This storage is short-lived and specific to the lifecycle of the component.  
**Use Case:** Ideal for temporary data that only needs to be available while the user is interacting with the current view or component.

**2. Service-Level State (Singleton Service)**  
**Description:** By creating a service with a shared state, you can maintain data across multiple components in your Angular application. Services are often singleton instances, meaning the same instance is available to all components that inject the service.  
**Use Case:** Useful for sharing data between components, managing application-wide state, or caching data during the session.

**3. Local Storage**  
**Description:** Local storage is a browser feature that allows you to store data as key-value pairs in the browser. Data stored in local storage persists across browser sessions (until manually cleared).  
**Use Case:** Ideal for storing non-sensitive information that needs to persist across page reloads or browser restarts, such as user preferences or settings.  

Here, we are going to talk about local storage. It can be useful for storing information you want to be available on the same browser. To do so we will follow the below steps:
1. Create a Service (Optional but Recommended)
2. Implement Local Storage Logic in the Service
3. Inject the Service into the components
