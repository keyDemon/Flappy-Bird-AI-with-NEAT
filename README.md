# Flappy Bird AI using NEAT

This project demonstrates the use of the NEAT (NeuroEvolution of Augmenting Topologies) algorithm to train a neural network to play the Flappy Bird game. The neural network controls the bird, which learns to navigate through the pipes by evolving over generations.

## Requirements

- Python 3.x
- Pygame
- NEAT-Python

## Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/yourusername/flappy-bird-neat.git
   cd flappy-bird-neat
   ```

2. **Install dependencies:**

   Ensure you have `pip` installed. Then, run:

   ```sh
   pip install pygame neat-python
   ```

3. **Add the required images:**

   Ensure the following images are in a directory named `imgs` in the same directory as the script:

   - `bird1.png`
   - `bird2.png`
   - `bird3.png`
   - `pipe.png`
   - `base.png`
   - `bg.png`

## Running the Program

1. **Configure NEAT:**

   Make sure the NEAT configuration file `config-feedforward.txt` is present in the same directory. If not, create it and add the necessary configurations.

2. **Execute the script:**

   Run the main script:

   ```sh
   python flappy_bird.py
   ```

## File Structure

- `flappy_bird.py`: Main script that runs the Flappy Bird game and applies the NEAT algorithm to train the AI.
- `config-feedforward.txt`: Configuration file for NEAT.

## How it Works

- **Bird Class:** Manages the bird's position, movement, and drawing on the screen.
- **Pipe Class:** Handles the generation and movement of pipes, including collision detection with the bird.
- **Base Class:** Manages the moving base at the bottom of the screen.
- **NEAT Integration:** The `main` function sets up the NEAT algorithm, initializes the population, and evolves the neural network over generations to improve the bird's performance.

## Game Mechanics

- The bird continuously falls due to gravity and can jump when the neural network decides to do so.
- Pipes move from right to left, and the bird must navigate through the gaps.
- The bird earns points by passing through the pipes, and the NEAT algorithm rewards higher fitness to birds that survive longer and score higher.

## NEAT Configuration

The `config-feedforward.txt` file contains various settings for the NEAT algorithm, such as population size, mutation rates, and network structure. Adjust these settings to fine-tune the training process.

## References

- [NEAT-Python Documentation](https://neat-python.readthedocs.io/en/latest/)
- [Pygame Documentation](https://www.pygame.org/docs/)
