# n8n with PostgreSQL

This project runs n8n with a PostgreSQL database using Docker.

## Prerequisites

- Docker
- Docker Compose

## Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository-url>
    cd <repository-folder>
    ```

2.  **Create a `.env` file:**

    Create a `.env` file by copying the example below and customize the values for your environment.

    ```env
    # PostgreSQL Credentials
    # Note: Do not use special characters in the password
    POSTGRES_DB=n8n
    POSTGRES_USER=n8n_user
    POSTGRES_PASSWORD=your_strong_password_here

    # n8n Domain
    N8N_HOST=n8n.your-domain.com

    # Timezone
    GENERIC_TIMEZONE=Europe/Berlin
    TZ=Europe/Berlin
    ```

3.  **Start the application:**

    Run the following command to start the n8n and PostgreSQL containers:

    ```bash
    docker-compose up -d
    ```

4.  **Access n8n:**

    Once the containers are running, you can access the n8n interface by navigating to `https://n8n.your-domain.com` in your web browser.

## Usage

-   **Stopping the application:**

    ```bash
    docker-compose down
    ```

-   **Viewing logs:**

    ```bash
    docker-compose logs -f
    ```

## Additional Resources

For more advanced configurations and troubleshooting, refer to the [official n8n documentation](https://docs.n8n.io/).
