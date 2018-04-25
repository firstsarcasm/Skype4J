# Skype4J

Here is an example of using this API to log into your Skype account.

```java
Skype skype = new SkypeBuilder(username, password).withAllResources().build();
skype.login();
skype.getEventDispatcher().registerListener(new Listener() {
  @EventHandler
  public void onMessage(MessageReceivedEvent e) {
    System.out.println("Got message: " + e.getMessage().getContent());
  }
});
skype.subscribe();
// Do stuff
skype.logout();
```

If you want to use a guest account, you can do that too

```java
Skype skype = new SkypeBuilder("Skype4JGuest").withChat("19:42abed183a95456ea1de9e2f7356163c@thread.skype").withAllResources().build();
skype.login();
skype.getEventDispatcher().registerListener(new Listener() {
  @EventHandler
  public void onMessage(MessageReceivedEvent e) {
    System.out.println("Got message: " + e.getMessage().getContent());
  }
});
skype.subscribe();
// Do stuff
skype.logout();
```

For more examples, please consult the [wiki](https://github.com/samczsun/Skype4J/wiki)

## JavaDocs

JavaDocs can be found [here](https://samczsun.github.io/Skype4J/)

## Licensing

This project is licensed under the Apache 2.0 license

## Contributing

If you want to help out, thanks a lot! However, there are a few legalities to work out first.

Any contributions you wish to make must be accompanied by a Contributer License Agreement ("CLA").
This simply gives myself, or whoever is maintaining the project, the right to redistribute your contributions.

The CLA can be found in the root directory of the project, in the file called "CLA". Please read it carefully.

You only need to submit your CLA once, so if you've already signed a CLA there's no need to do it again.