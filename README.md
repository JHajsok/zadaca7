# zadaca7

## Kako pokrenuti?

Napravi novi folder i u njemu jos jedan folder `src` te unutar njega `git clone https://github.com/JHajsok/zadaca7.git`

Vrati se u root folder (znaci tam di je `src`) i napravi sljedece:
1. `rosdep install --from-paths src -y --ignore-src`
2. `colcon build`
3. `export TURTLEBOT3_MODEL=waffle`
4. `source install/setup.bash`

I sad dolazimo do pokretanja simulacije i bug algoritma --> 2 terminala (jedan u root folderu, drugi u `src/as_bugs`)  
U prvom terminalu: `ros2 launch as_bugs bug.launch.py`  
U drugom terminalu: `python3 bugx.py`  

U rviz2 treba zadati 2D Goal Pose i to je to

## Promjena labirinta

Unutar launch fajla (`src/launch/bug.launch.py`) promijeniti 28. liniju na kraju iz `cust2.world` u `cust1.world` ili `Arena_1.world`  
Nakon promjene obavezno `colcon build`

## Izlaz iz simulacije i/ili skripte

Samo Ctrl+C na terminal u kojem je sim/skripta

Ako bug dode do goala skripta se sama gasi
