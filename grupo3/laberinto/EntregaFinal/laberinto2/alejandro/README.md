Skip to content
Search or jump to…
Pull requests
Issues
Codespaces
Marketplace
Explore

@JaimeTruman
JaimeTruman
/
IdSw2-22-23
Public
forked from mmasias/IdSw2-22-23
Cannot fork because you own this repository and are not a member of any organizations.
Code
Pull requests
Actions
Projects
Security
Insights
Settings
IdSw2-22-23/grupo3/laberinto/readme.md
@Marfdev
Marfdev plantuml code into readme
Latest commit 9529a5d last week
History
1 contributor
100 lines (88 sloc)  2.42 KB

![Alt text](./Diagrama.png "Optional Title")

```
@startuml
class World
class Main
class User
class Position
class Pared
class Suelo
class AguaTurbulenta
class Montana
class CespedMedio
class Agua
class Arena
class CespedAlto
class CespedBajo
abstract class Entity
abstract class Block
enum PlayerSprite { 
DEFAULT
ALT
}
enum BlockSprite {
DAY
NIGHT
}
Main : World world
Main : Scanner scanner
Main -- World
World : final int[][] INTMAP
World : private static int rows
World : private static int columns
World : private static Block[][] map
World : private User user
World : private static final Map<Integer, Block> BLOCKMAPPER
World : public static Block[][] getMap()
World : public static int getRows()
World : public static int getColumns()
World : public static Block getBlock(Position position)
World : public void printWorld(Scanner scanner)
World - User
Entity : protected Position position
Entity : protected PlayerSprite sprite
Entity : protected boolean canBeMounted
Entity : protected boolean isBeingRidden
Entity : public abstract String getSprite();
Entity : public abstract void setSprite(String sprite)
Entity : public Position getPosition()
Entity : protected void setPosition(double x, double y)
Entity : protected void setPosition(Position position)
Entity : protected abstract void move(String direccion)
Entity --> User
Entity --> Caballo
Entity --> Barca
Entity --> Alfombra
Entity - Position
User : public boolean isMounted
User : public Entity mount
User : public void toggleMount(Entity entityToMount)
Position : public Position(double x, double y)
Position : public double getX()
Position : public double getY()
Position : public void setX(double x)
Position : public void setY(double y)
Position : private double x
Position : private double y
Block : protected BlockSprite sprite
Block : protected double speed
Block : protected Integer id
Block : protected List<Entity> transitList
Block : public double getSpeed() 
Block : public abstract String getSprite()
Block : public abstract void setSprite(String sprite)
Block : public abstract boolean canStep(User user)
Block : public Integer getId() 
Block : public List<Entity> getTransitList() 
Block --> Pared
Block --> Suelo
Block --> AguaTurbulenta
Block --> Montana
Block --> CespedMedio
Block --> Agua
Block --> Arena
Block --> CespedAlto
Block --> CespedBajo
World -- Block
@enduml
```
Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
IdSw2-22-23/readme.md at feature/restructuracion · JaimeTruman/IdSw2-22-23 