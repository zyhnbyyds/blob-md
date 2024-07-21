### 🌟 Nuxt CLI Tool for Server API Generation

This is a Node CLI tool designed for Nuxt 3 to streamline the creation of server API files. Using Mongoose models, you can easily generate the necessary API files for your node server. Future updates will include support for additional database models.

---

## 📜 Commands

### 1. `g` [generate]
Generate server API files using Mongoose models.

- **Options:**
  - `-g` : Generate GET API files. (Includes list and detail)
  - `-p` : Generate POST API files.
  - `-u` : Generate PUT API files.
  - `-d` : Generate DELETE API files.
  - `-a` : Generate all API files.
  - `-n` : The name of the API files. (Required)
  - `-p` : The path of the API files. (Required)
  - `-m` : The model for the API files. (If not provided, only API files are generated without operational code)
    - **Note:** Model must be a Mongoose model and include a key field (e.g., `id`).
  - `-k` : The key field of the model. (Default: `id`).
  - `-t` : Unit test generation. use vitest.

### 2. `h` [help]
Display help information.

---

## 📖 Usage Guide

### Installing the CLI Tool

```bash
npm install -g your-cli-tool
```

### Generating API Files

#### Basic Command Structure

```bash
nc g -n <api-name> -p <api-path> [options]
```

#### Example Commands

1. **Generate GET API Files:**
    ```bash
    nc g -g -n user -p ./server/api/user -m User -k _id
    ```
    This command will generate the necessary GET API files for the `User` model, including list and detail views.

2. **Generate POST API Files:**
    ```bash
    nc g -p -n user -p ./server/api/user -m User
    ```
    This will create the POST API files for the `User` model.

3. **Generate All API Files:**
    ```bash
    nc g -a -n user -p ./server/api/user -m User -k _id
    ```
    This command generates all API files (GET, POST, PUT, DELETE) for the `User` model.

### Help Command

To view all available commands and options:

```bash
nc h
```

---

## 🔧 Additional Notes

- Ensure that the `-m` option points to a valid Mongoose model.
- The `-k` option is crucial for identifying the unique field in your model. By default, it is set to `id`, but you can specify a different key if necessary.

---

### 🌐 Future Updates

- Support for additional database models beyond Mongoose.
- Enhanced CLI features and options for more flexible API generation.

---

Stay tuned for updates and improvements! Happy coding! 💻✨
