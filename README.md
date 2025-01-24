# PHP Development Environment for LeetCode Solutions via a `Dev Container`

Welcome to the repository for setting up a reusable PHP development environment tailored for solving [LeetCode problems](https://leetcode.com/problemset/). This guide walks you through creating a Docker-based dev container in Visual Studio Code with PHP and Test-Driven Development (TDD). Whether you're preparing for coding interviews or honing your PHP skills, this setup ensures a consistent and efficient development experience.

---

## Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [How to Use](#how-to-use)
- [Key Benefits](#key-benefits)
- [Resources](#resources)
- [License](#license)
- [Contributing](#contributing)

---

## 🚀 Features {#features}

- **Pre-configured PHP 8.3 environment**: Includes Composer and Xdebug for seamless development.
- **Effortless testing**: Set up for PHPUnit, perfect for TDD.
- **Cross-platform consistency**: Develop in the same environment across machines.

---

## 🛠️ Quick Start {#quick-start}

### Prerequisites

1. Install [Docker Desktop](https://www.docker.com/get-started/).
2. Install [Visual Studio Code](https://code.visualstudio.com/download).
3. Install the **Dev Containers** extension in VS Code:
   - Open the Extensions view (`Ctrl+Shift+X` or `Cmd+Shift+X` on macOS).
   - Search for "Remote - Containers" and install it or go to the [Visual Studio Code Dev Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) website.

---

### Setting Up the Dev Container

1. Clone this repository:

   ```bash
   git clone https://github.com/angellugo/leetcode-php-devcontainer.git
   cd leetcode-php-devcontainer
   ```

2. Open the project in VS Code:

   ```bash
   code .
   ```

3. Follow the prompts to reopen the folder in a container or use the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P` on macOS) to select:

   ```text
   Dev Containers: Reopen in Container
   ```

4. The container will build automatically, setting up PHP, Composer, and Xdebug so you can start solving LeetCode problems in PHP! 🎉

---

## ✅ How to Use {#how-to-use}

### 1. Writing Your Solution

1. Create a new directory for your LeetCode problem under `src/`:

   ```bash
   mkdir -p src/Problem0004
   ```

2. Add your solution file, e.g., `src/Problem0004/MedianOfTwoSortedArrays.php`:

   ```php
   <?php

   namespace LeetCode\Problem0004;

   class MedianOfTwoSortedArrays
   {
       public function findMedianSortedArrays(array $nums1, array $nums2): float
       {
           return 0.0; // Placeholder
       }
   }
   ```

### 2. Writing Tests

1. Create a test file under `tests/`:

   ```bash
   mkdir -p tests/Problem0004
   ```

2. Add your test case, e.g., `tests/Problem0004/MedianOfTwoSortedArraysTest.php`:

   ```php
   <?php

   namespace LeetCode\Problem0004;

   use PHPUnit\Framework\TestCase;

   class MedianOfTwoSortedArraysTest extends TestCase
   {
       public function testMedianOfTwoSortedArrays()
       {
           $solution = new MedianOfTwoSortedArrays();
           $this->assertEquals(2.0, $solution->findMedianSortedArrays([1, 3], [2]));
           $this->assertEquals(2.5, $solution->findMedianSortedArrays([1, 2], [3, 4]));
       }
   }
   ```

### 3. Running Tests

Run PHPUnit directly from the container:

```bash
vendor/bin/phpunit tests/Problem0004/MedianOfTwoSortedArraysTest.php
```

---

## 🌟 Key Benefits {#key-benefits}

- **Reusability**: Easily extend to solve more LeetCode problems.
- **Efficiency**: Focus on solving problems without worrying about environment setup.
- **Portability**: Develop consistently across different machines.

---

## 📚 Resources {#resources}

- [LeetCode](https://leetcode.com/)
- [PHP Documentation](https://www.php.net/)
- [PHPUnit Documentation](https://phpunit.de/)

---

## 📝 License {#license}

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing {#contributing}

Contributions are welcome! Feel free to open issues or submit pull requests to improve this setup.

---

Happy coding! 🎉
