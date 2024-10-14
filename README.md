# Delivery1.py
def calculate_delivery_fee(area_code, weight):
    if area_code == 1:  # Local delivery
        if weight < 5:
            return 12.00
        elif 5 <= weight <= 20:
            return 16.50
        else:
            return 22.00
    elif area_code == 2:  # Long distance delivery
        if weight < 5:
            return 35.00
        else:
            return 47.95
    else:
        return None

def main():
    area_code = int(input("Enter delivery area code (1 for local, 2 for long distance): "))
    weight = float(input("Enter weight of the item (in pounds): "))
    
    fee = calculate_delivery_fee(area_code, weight)
    
    if fee is not None:
        print(f"The delivery fee is: ${fee:.2f}")
    else:
        print("Invalid area code.")

if __name__ == "__main__":
    main()
