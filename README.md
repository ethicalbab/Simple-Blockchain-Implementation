# Simple Blockchain with Flask

This project is a simple implementation of a blockchain using Python and Flask. The blockchain allows you to mine new blocks, retrieve the entire chain, and validate the chain.

## Prerequisites

- Python 3.x
- Flask
- hashlib
- json

## Getting Started

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/blockchain-flask.git
    cd blockchain-flask
    ```

2. **Install dependencies:**

    ```bash
    pip install Flask
    ```

### Running the Application

1. **Start the Flask server:**

    ```bash
    python app.py
    ```

2. **Access the application:**

    Open your web browser and go to `http://127.0.0.1:5000`.

## API Endpoints

### Mine a New Block

- **URL:** `/mine_block`
- **Method:** `GET`
- **Description:** Mines a new block and adds it to the blockchain.

- **Sample Response:**

    ```json
    {
        "message": "A block is MINED",
        "index": 2,
        "timestamp": "2024-08-02 12:34:56.789123",
        "proof": 123456,
        "previous_hash": "abcd1234efgh5678ijkl91011mnop1213"
    }
    ```

### Get the Entire Blockchain

- **URL:** `/get_chain`
- **Method:** `GET`
- **Description:** Retrieves the entire blockchain.

- **Sample Response:**

    ```json
    {
        "chain": [
            {
                "index": 1,
                "timestamp": "2024-08-02 12:34:56.789123",
                "proof": 1,
                "previous_hash": "0"
            },
            {
                "index": 2,
                "timestamp": "2024-08-02 12:34:56.789123",
                "proof": 123456,
                "previous_hash": "abcd1234efgh5678ijkl91011mnop1213"
            }
        ],
        "length": 2
    }
    ```

### Check Blockchain Validity

- **URL:** `/valid`
- **Method:** `GET`
- **Description:** Checks if the blockchain is valid.

- **Sample Response:**

    ```json
    {
        "message": "The Blockchain is valid."
    }
    ```

## Project Structure

