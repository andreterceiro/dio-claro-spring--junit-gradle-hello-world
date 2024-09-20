Creating a basic "Hello World" project with Gradle is straightforward. Here’s a step-by-step guide:

### Step 1: Install Gradle
Make sure you have Gradle installed. You can download it from the [official website](https://gradle.org/install/).

### Step 2: Create Project Directory
Open a terminal and create a new directory for your project:

```bash
mkdir HelloWorld
cd HelloWorld
```

### Step 3: Initialize the Gradle Project
Run the following command to generate a basic Gradle project structure:

```bash
gradle init
```

You’ll be prompted to select the type of project. Choose "application" and then follow the prompts to set the project details (like language, build type, etc.).

### Step 4: Modify the Project Structure
After initialization, you should have a structure like this:

```
HelloWorld
├── build.gradle
├── gradle
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── settings.gradle
└── src
    └── main
        └── java
            └── <your-package>
                └── App.java
```

### Step 5: Edit `App.java`
Navigate to `src/main/java/<your-package>/` and open `App.java`. Replace the contents with the following code:

```java
package <your-package>;

public class App {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

Make sure to replace `<your-package>` with your chosen package name (e.g., `com.example.helloworld`).

### Step 6: Configure `build.gradle`
Open `build.gradle` and ensure it looks something like this:

```groovy
plugins {
    id 'application'
}

application {
    mainClass = '<your-package>.App'
}

repositories {
    mavenCentral()
}

dependencies {
    // Add your dependencies here
}
```

### Step 7: Build and Run the Project
To build the project, run:

```bash
gradle build
```

To run your application, use:

```bash
gradle run
```

### Step 8: Output
You should see the output:

```
Hello, World!
```

### Summary
You now have a basic "Hello World" project set up with Gradle! You can expand this project by adding more classes or dependencies as needed.