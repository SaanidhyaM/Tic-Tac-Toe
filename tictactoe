# Tic Tac Toe

# Create the grid
grid = [' ' for _ in range(9)]

# Define winning combinations
winning_combinations = [
    [0, 1, 2], [3, 4, 5], [6, 7, 8],  # rows
    [0, 3, 6], [1, 4, 7], [2, 5, 8],  # columns
    [0, 4, 8], [2, 4, 6]  # diagonals
]

print('-------------')
for i in range(3):
    print(f'| {i*3+1} | {i*3+2} | {i*3+3} |')
    print('-------------')
print("Use the numbers in the grid as reference to enter your move.\n")

# Function to print the grid
def print_grid():
    print('-------------')
    for i in range(3):
        print(f'| {grid[i * 3]} | {grid[i * 3 + 1]} | {grid[i * 3 + 2]} |')
        print('-------------')

# Function to check if a player has won
def check_win(player):
    for combo in winning_combinations:
        if all(grid[i] == player for i in combo):
            return True
    return False

# Function to play the game
def play_game():
    current_player = 'X'
    while True:
        print_grid()
        position = int(input(f"Player {current_player}, enter a position (1-9): ")) - 1
        if position < 0 or position >= 9 or grid[position] != ' ':
            print('Invalid move. Try again.')
            continue
        grid[position] = current_player
        if check_win(current_player):
            print_grid()
            print(f"Player {current_player} wins!")
            break
        if ' ' not in grid:
            print_grid()
            print("It's a tie!")
            break
        current_player = 'O' if current_player == 'X' else 'X'

# Start the game
play_game()
