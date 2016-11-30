# In-Memory-FS Demo

In this example I will show you the usage of an in memory java solution that is available 
as Open Source Project.
[JIMFS on Github]( https://github.com/google/jimfs)

## OS dependen behavior
You could define the OS depended behavior during the time 
you are creating the builder for the FS.

```java
  Configuration.unix()
  Configuration.osX()
  Configuration.windows()
  Configuration.forCurrentPlatform()
```

With the builder you could manage the params like 
maximal size, available roots and much more.

After you created the configuration, the method build() will create the instance of the configuration.
With this you are able to create instances of the filesystem: 

```final FileSystem fs = Jimfs.newFileSystem(configuration)```

