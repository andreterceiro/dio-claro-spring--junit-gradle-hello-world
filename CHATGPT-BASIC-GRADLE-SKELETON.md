To create a simple "Hello World" project using Gradle 4.4.1, follow these steps:

### Step 1: Install Gradle

Make sure you have Gradle installed. You can check this by running:

```bash
gradle -v
```

If you don't have Gradle installed, you can download it from the [Gradle website](https://gradle.org/releases/).

### Step 2: Create a New Project Directory

Create a new directory for your project:

```bash
mkdir HelloWorld
cd HelloWorld
```

### Step 3: Initialize the Gradle Project

Run the following command to create a basic Gradle project structure:

```bash
gradle init --type basic
```

This will create a few files and directories, including `build.gradle`.

### Step 4: Edit `build.gradle`

Open the `build.gradle` file and modify it to include the application plugin and specify the main class. Here’s an example:

```groovy
plugins {
    id 'application'
}

mainClassName = 'HelloWorld'

repositories {
    mavenCentral()
}

dependencies {
    // You can add dependencies here if needed
}
```

### Step 5: Create Source Directory and HelloWorld Class

Create the necessary directories and the HelloWorld class:

```bash
mkdir -p src/main/java
```

Now create a file named `HelloWorld.java` in `src/main/java`:

```java
// src/main/java/HelloWorld.java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Step 6: Build and Run the Project

To build the project, run:

```bash
gradle build
```

To run the application, use:

```bash
gradle run
```

### Step 7: Verify Output

You should see `Hello, World!` printed in the console.

### Summary

You now have a simple "Hello World" Gradle project using version 4.4.1. You can expand upon this structure to add more features or dependencies as needed! If you have any more questions or need further assistance, feel free to ask!