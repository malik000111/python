def find_cargo():
    cargo_weight = 713
    boxes = [[2, 200], [3, 300], [7, 213]]  # [distance, weight]
    while True:
        for i in range(3):
            distance = int(input("Enter distance for box {}: ".format(i + 1)))
            boxes[i][0] = distance

        total_weight = sum(box[1] for box in boxes)

        if total_weight == cargo_weight:
            print("All cargo found!")
            break
        else:
            print("Incorrect distances. Try again.")

            # Move boxes randomly
            for i in range(3):
                boxes[i][1] = 0


find_cargo()
