# extension-python
*Repository by Joalor64GH*

*Originally by magnumsrt*

Original Repository - `https://github.com/magnumsrt/MagEngine-Public`

## Instructions
### 1. Installation:
You can either install it througfh haxelib:
```yml
haxelib install extension-python
```
Or you can install it through Git for the latest updates:
```yml
haxelib git extension-python https://github.com/Joalor64GH/extension-python.git
```

### 2. Editing `Project.xml`
First of all, add this in `Project.xml`:

```xml
<haxelib name="extension-python" />
```

Then, if you have a custom defines section, add:

```xml
<define name="PYTHON_ALLOWED"/>
```

Then, before:

```xml
<assets path="assets/songs"         library="songs"         exclude="*.ogg" if="web"/>
<assets path="assets/songs"         library="songs"         exclude="*.mp3" unless="web"/>
```

Add:

```xml
<assets path="dlls/"                rename=''               if="PYTHON_ALLOWED" />
```

Alternatively, if you followed the steps for MP4 Video support, replace:

```xml
<assets path="dlls/"                rename=''               if="VIDEOS_ALLOWED" />
```

With:

```xml
<assets path="dlls/"                rename=''               if="VIDEOS_ALLOWED || PYTHON_ALLOWED" />
```

# Credits
* [Joalor64GH (me)](https://github.com/Joalor64GH) - Creator of repository.
* [magnumsrt](https://github.com/magnumsrt) - Creator of Python Support and Mag Engine.
* [PolybiusProxy](https://github.com/polybiusproxy) - Inspiring me to do this.
