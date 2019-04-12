# dursin/mammalian

A collection of metadata for living species of the class Mammalia in North America.

## Species Collection

The default export of the package is an array of `Species` objects with the following structure:

```
    interface Image {
        source: string;
        width: number;
        height: number;
    }

    type ConservationStatus = "EX" | "EW" | "CR" | "EN" | "VU" | "NT" | "LC";

    interface Species {
        title: string;
        description: string;
        thumbnail: Image;
        image: Image;
        desktop_url: string;
        mobile_url: string;
        extract: string;
        conservation_status: ConservationStatus;
    }
```

Where conservation status is as defined by the [Wikipedia page on Conservation Status](https://en.wikipedia.org/wiki/Conservation_status)

For example:

```
    {
        title: "American black bear",
        thumbnail: {
            source: "https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/01_Schwarzb%C3%A4r.jpg/236px-01_Schwarzb%C3%A4r.jpg",
            width: 236,
            height: 320
        },
        image: {
            source: "https://upload.wikimedia.org/wikipedia/commons/0/08/01_Schwarzb%C3%A4r.jpg",
            width: 427,
            height: 578
        },
        description: "species of bear",
        desktop_url: "https://en.wikipedia.org/wiki/American_black_bear",
        mobile_url: "https://en.m.wikipedia.org/wiki/American_black_bear",
        extract: "The American black bear is a medium-sized bear native to North America. It is the continent's smallest and most widely distributed bear species. American black bears are omnivores, with their diets varying greatly depending on season and location. They typically live in largely forested areas, but do leave forests in search of food. Sometimes they become attracted to human communities because of the immediate availability of food. The American black bear is the world's most common bear species.",
        conservation_status: "LC"
    }
```

## Contributing

Any enhancement made to the `species.json` file must be scripted in the `index.js` file under the `generate` directory.
