### Mostly out of the scope of interview
### Two commonly used patterns in interviews: Singleton Class & Factory Method

## Singleton class:
- ensures a class has only one instance and ensures access to the instance through application. Ex: Resturant.
```
Public class Restaurant{
    private static Restaurant _instance = null;
    protected Restaurant() {...}
    public static Restaurant getInstance() {
        if (_instance == null){
            _instance = new Restaurant();
        }
    }
}
```
However many people dislike it. Interfere with unit testing

## Factory Method:
Offers an interface for creating an instance of a class, with subclasses deciding which class to instantiate.\
You can:
- Implement this with the creator class being abstract and not providing an implementation for the factory method.
- Or, have the creator class be a concrete class that provides an omplementation for the factory method. In this case, factory method would take a parameter representing which class to instantiate
```
Public class CardGame{
    public static CardGame createCardGame(GameType type){
        if (type == GameType.Poker){
            return new PokerGame();
        }
        else if (type == GameType.BlackJack){
            return new BlackJackGame();
        }
        return null;
    }
}