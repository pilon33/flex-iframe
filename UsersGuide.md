
---

## Import Flex-IFrame swc in your project ##

There are several ways to get the Flex-Iframe swc.

### Directly downloading Flex-IFrame swc ###
You can find the last version of the library at the [downloads](http://code.google.com/p/flex-iframe/downloads/list) page.

If you use Flex/Flash builder, just drop it in the project `libs` directory.


### Using Maven ###
Flex-IFrame artifacts are deployed in [Maven Central repository](http://repo1.maven.org/maven2/com/google/code/flex-iframe/). All you have to do is to add a dependency:
```
<dependency>
  <groupId>com.google.code.flex-iframe</groupId>
  <artifactId>flex-iframe</artifactId>
  <version>1.4.5</version>
</dependency>
```

### Building Flex-IFrame from the sources ###

If you just cannot wait for a release, you can follow the [developer's guide](DevelopersGuide.md) instructions.



---

## Use Flex-IFrame in your project ##

### Change the wmode ###

**Important !** To use flex-iframe, you must add the parameter `wmode="opaque"` to the embed in your HTML template. For more information about this, read the [FAQ](FAQ.md).


### Create an IFrame ###

Here is an example of use in MXML:

```
<mx:Application
    xmlns:mx="http://www.adobe.com/2006/mxml"
    xmlns:flexiframe="http://code.google.com/p/flex-iframe/">

    <flexiframe:IFrame id="googleIFrame"
                       label="Google"
                       source="http://www.google.com"
                       width="80%"
                       height="80%"/>

<mx:Application>
```

You can create IFrames in ActionScript too by importing the IFrame class:
```
import com.google.code.flexiframe.IFrame;
```

You can find several example sources [here](http://code.google.com/p/flex-iframe/source/browse/#svn/trunk/examples), and with their builds [here](http://repo1.maven.org/maven2/com/google/code/flex-iframe/examples/).