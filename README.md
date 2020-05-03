# Awtrix2-Docker
Official Docker Container for [Awtrix2](https://blueforcer.de/2019/01/04/awtrix-2-0/) Host in collaboration with Blueforcer.

The Container is based on the anapsix/alpine-java:8_JDK image.

It has an autoupdate feature witch will get the latest Host from the Awtrix Site on a restart from the Container.

# Getting Started

```bash
docker run --name AwTriX2 -p 7000:7000 -p 7001:7001 --restart always -e TZ=Europe/Berlin whyet/awtrix2:latest-arm
```

# For persistent Data add:

```bash
-v pwd:/data
```

# Set Language

If you want AWTRIX to automatically display some apps like **DayOfTheWeek** in your local language/format (e.g. "Sonntag" instead of "Sunday") you can specify this with an eviroment variable.

```bash
-e JAVA_TOOL_OPTIONS="-Duser.language=de -Duser.country=DE"
```

Where `de` is your two-letter language code. (see [ISO 639-2](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes))  
And `DE` is your two-letter country code. (see [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2))