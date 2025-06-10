# Hand Gesture-Controlled Tic-Tac-Toe

A Python-based Tic-Tac-Toe game controlled using hand gestures, built with OpenCV and MediaPipe. Players use their index finger to select a cell on a 3x3 grid and close their hand to confirm a move, all via webcam. The game features real-time hand tracking, a simple UI, and classic Tic-Tac-Toe logic.

Features





Gesture Controls: Point with your index finger to select a cell; close your hand to place an 'X' or 'O'.



Real-Time Interaction: Uses webcam input for seamless gesture detection.



Cross-Environment Support: Compatible with standard Python, Jupyter notebooks, and Pyodide (browser-based).



Smooth Gameplay: Runs at ~30 FPS with asyncio for responsive performance.

Requirements





Python 3.8+



Libraries: opencv-python, mediapipe, numpy, nest_asyncio



Webcam for gesture input

Installation





Clone the repository:

git clone <repository-url>
cd <repository-folder>



Install dependencies:

pip install opencv-python mediapipe numpy nest_asyncio



Run the game:

python tictactoe_gesture.py

Or, in a Jupyter notebook, copy and run the code in a cell.

How to Play





Launch the script to open a webcam window showing a 3x3 Tic-Tac-Toe grid.



Select a Cell: Point with your index finger to highlight a cell (green outline).



Confirm Move: Close your hand (all fingers down except thumb) to place your 'X' or 'O'.



Gameplay: Players alternate turns. The game ends with a winner or draw, displayed on-screen.



Quit: Press 'q' to exit.

Technical Details





Hand Tracking: MediaPipe detects hand landmarks; the index finger tip selects cells, and a closed hand confirms moves.



Game Logic: Checks rows, columns, and diagonals for wins or draws.



Rendering: OpenCV draws the grid and game state at 640x480 resolution.



Asyncio: Ensures smooth performance and compatibility with Jupyter and Pyodide via nest_asyncio.



No File I/O: Pyodide-compatible for browser execution.

Troubleshooting





Webcam Error: If "Error: Could not open webcam" appears, ensure your webcam is connected and not in use by another application. Try changing cv2.VideoCapture(0) to cv2.VideoCapture(1).



Performance: Adjust asyncio.sleep(0.03) for different FPS if needed.



Dependencies: Ensure all libraries are installed with compatible versions.

Future Improvements





Add sound effects for moves and game outcomes.



Support multiple gesture types for different actions.



Enhance UI with customizable grid sizes or themes.

License

MIT License. See LICENSE for details.

Acknowledgments





Built with OpenCV and MediaPipe for computer vision.



Inspired by the potential of gesture-based interfaces in gaming.

Feel free to contribute or share feedback! 🚀
