# Pathway translations

This repository contains translations that are used by the Projects Admin back end and Projects website front end

If you add a Pathway to the Projects Admin, it normally has a title and description, which will be used on the Projects website.

However, if you add data in the relevant translation file here to match the slug for the Pathway, the system will use those translations instead of the defaults.

You can also add translations for metadata - title & description and for the new Pathway designs, you can add 'header' data to populate the sections in the Pathway page's header.

# NB

YAML should ideally be linted because if invalid syntax is pushed to the gh-pages branch it can cause server errors on Projects Admin!!

# Examples

Here is a simple example with just title, description and meta data:

```yaml
scratch-intro:
    title: "Introduction to Scratch: sprites, scripts, and loops"
    description: In this introduction to coding in Scratch for beginners, you will learn how to add code, costumes, and sounds to sprites as you make animations, a game, an app, and a book.
    meta_title: Project path | Intro to Scratch programming for kids
    meta_description: Introduction to Scratch programming for kids, teenagers and young adults. Learn how to make animations, a game, an app, and a book.
```

This is an example with the header populated:

```yaml
scratch-intro:
    title: "Introduction to Scratch: sprites, scripts, and loops"
    description: In this introduction to coding in Scratch for beginners, you will learn how to add code, costumes, and sounds to sprites as you make animations, a game, an app, and a book.
    meta_title: Project path | Intro to Scratch programming for kids
    meta_description: Introduction to Scratch programming for kids, teenagers and young adults. Learn how to make animations, a game, an app, and a book.
    header:
      - title: "What will I create?"
        content: |
          Through this path you will create an interactive project, games, a simulation, and a piece of digital art.
          By the end of this path you will have used your new skills to become a digital artist with your own unique, inspirational piece of art that can be scaled using repeated patterns.
      - title: "What do I need to know?"
        content: |
          - Basic typing and computer navigation skills
          - "Experience coding in Scratch. If you are unfamiliar with Scratch you could try our Scratch paths, [Introduction to Scratch](https://projects.raspberrypi.org/en/pathways/scratch-intro), [More Scratch](https://projects.raspberrypi.org/en/pathways/more-scratch), and [Further Scratch](https://projects.raspberrypi.org/en/pathways/further-scratch)."
      - title: "What do I need?"
        content: |
           - Access to a web browser capable of running [trinket.io](https://trinket.io).
      - title: "Facilitator information"
        content: |
          ##321…Make!
          This path is made up of three different types of project in a 3-2-1 structure:

          - 3 Explore projects to introduce creators to a set of skills, and provide step-by-step instructions to help them develop initial confidence.
          - 2 Design projects to allow creators to practise the skills they learned in the previous Explore projects, and to express themselves creatively whilst growing independence.
          - 1 Invent project where creators meet a project brief for a particular audience using their skills.

          ##Reflection
          Each project contains a reflection step. Reflecting is an important part of learning, because it helps make new connections in your brain. Creators answer three questions to reflect on what they’ve learned.

          After each question, they press ‘Check my answer’. If an answer is incorrect, useful feedback will guide them towards the correct answer. There is no limit to the amount of times they can attempt each question.

          ##Saving projects in Trinket
          If creators have a Trinket account, they can remix the starter projects to save a copy to their My Trinkets library.

          If they don’t have a Trinket account, they can still come back to their project in the future by using the same computer and using the starter project link.

          ##Inspiring the community
          Creators are encouraged to inspire others in the Raspberry Pi Foundation community by sharing their projects with us via the [project submissions form](https://form.raspberrypi.org/f/community-project-submissions). Projects will be anonymously shared to our Community Galleries.
```

the `header` is a [yaml array of objects](https://www.w3schools.io/file/yaml-arrays/#yaml-arrays-of-objects) which contains `title` and `content` keys.

The values for the `content` can be written with simple [markdown](https://daringfireball.net/projects/markdown/) to add 

- headers
```
##Saving projects in Trinket
```

- links 
```
[trinket.io](https://trinket.io)
```

- lists
```
- Basic typing and computer navigation skills
- "Experience coding in Scratch. If you are unfamiliar with Scratch you can..."
```

Multiline content can be added using the '|' character and ensuring indentation follows the YAML syntax:

```
        content: |
          Through this path you will create an interactive project, games, a simulation, and a piece of digital art.
          By the end of this path you will have used your new skills to become a digital artist with your own unique, inspirational piece of art that can be scaled using repeated patterns.
```

