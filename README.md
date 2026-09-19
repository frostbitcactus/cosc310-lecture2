# COSC 310 - Lecture 2 Exercises

Python & Git exercises: menu filtering, a `Cart` class, and business rule
enforcement (`OutOfStockError`, quantity validation), backed by pytest tests.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Run

```bash
python3 exercise1.py
python3 exercise2.py
python3 exercise3.py
pytest -v
```

## Business rules and where they are enforced

- Quantity must be at least 1 - enforced in `Cart.add_item` (`exercise3.py`),
  raises `ValueError`.
- Unavailable items cannot be added to the cart - enforced in
  `Cart.add_item` (`exercise3.py`), raises `OutOfStockError`.
- Removing an item not in the cart is rejected - enforced in
  `Cart.remove_item` (`exercise3.py`), raises `KeyError`.
