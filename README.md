# LIA

For this assignment, you must develop a web application named [Cellaret]
that allows users to manage their beverage alcohol collection.

[Cellaret]: https://en.wikipedia.org/wiki/Cellarette

## Planning

The project is divided into three milestones. Milestone 1, due at the
end of the week, covers the initial setup. Milestone 2 and 3, each
lasting two weeks, focus on implementing features.

GitHub must be used to store code and for project planning.
[Click here to create your repository.][Classroom] For every feature you
work on, a corresponding issue of type "feature" must be created, and
each feature should be divided into sub-issues of type "task". Issues
related to code must be closed by the associated commit or pull request.

We strongly discourage assigning features or tasks to specific team
members in advance. The whole team should focus on one feature at a
time, and tackle tasks in the order in which they appear in the
milestone.

Daily meetings are scheduled to discuss your work. Your attendance to
these meetings is mandatory.

[Classroom]: https://classroom.github.com/a/HXv5qEHP

### Milestone 1

> Due: January 9

Your task for milestone 1 is to analyse requirements, do research, and
prepare for milestone 2 and 3. Here are the deliverables:

- Entity-relationship model
- Technology stack (Wordpress and UI frameworks are prohibited)
- Installation guide
- Models API documentation
- Continuous integration setup (linter, formatter, test runner)
- Personas (at least one)
- Color palette (including contrast ratios)
- Typography system (including size, leading, margins, and font for body
  text, small text, and three levels of headings)
- Mockups (at least one page)
- Feature backlog for milestone 2

These must be accessible from your repository's README.

#### Assessment criteria

- Planning
  - requirements are met
  - features are prioritized by effort and user needs
  - features are accurately divided into tasks
  - backlog is realistic and achievable within the time frame

- Design
  - personas are well-detailed and relevant to the application
  - colors are harmonious and conform to the [WCAG 2.1 Level AA][webaim]
  - typography is legible and effectively communicates hierarchy
  - visual guidelines are applied consistently
  - design decisions are informed by personas
  - each page has a clear, visually reinforced goal

- Code
  - entities, relationships and cardinalities match the requirements
  - documentation is clear and complete

- Teamwork
  - continuous integration is properly configured and runs on every
    commit
  - workload is evenly distributed

[webaim]: https://webaim.org/resources/contrastchecker/

### Milestone 2 and 3

> Due: January 23, February 6

Your task for milestone 2 and 3 is to work on features. Only completed
features will be assessed. Given the allotted time, you may not be able
to implement all of the features listed below. It is your responsibility
to prioritize features according to the value they add to the
application.

Milestone 3 will conclude with a formal presentation in front of the
class. As part of this presentation, you must submit a slide deck that
highlights the various stages of the development process, including
challenges encountered and lessons learned.

#### Assessment criteria

Same as for milestone 1, plus:

- Code
  - program flow is decomposed into manageable, logical pieces
  - data structures are appropriate
  - common code is unified, not duplicated
  - appropriate algorithms are used, and coded cleanly
  - interfaces are used correctly
  - code is formatted consistently and lint-free
  - code is well-tested
  - project is well-structured
  - markup is semantic
  - website is [accessible]
  - no global variables are used
  - constants are used instead of hard-coded values
  - complex or meaningful expressions are named
  - naming is consistent and descriptive
  - inline comments are only used to explain reasoning
  - mockups are faithfully implemented and adapted when necessary

- Teamwork
  - commits contain related changes
  - commit messages are consistent and informative
  - changes are merged using pull requests
  - pull requests are reviewed before being merged
  - review comments help the author improve their code

[accessible]: https://developer.mozilla.org/en-US/docs/Web/Accessibility

## Features

Cellaret is a web application that allows users to manage their beverage
alcohol collection. Users can browse products from the SAQ catalog, and
create lists of bottles, known as "cellars". You will find below the
list of features to implement.

> [!NOTE]
> A "product" is a beverage from the SAQ catalog, while a "bottle" is an
> instance of a product stored in a cellar. There is only one Menaud Dry
> Gin product, for example, but users can have multiple bottles of it in
> their cellars.

### Visitors can...

- view the website on desktop and mobile devices
- view the product catalog
- view detailed information about a product
- search the catalog by product name
- sort the catalog or search results by price (lowest to highest,
  highest to lowest) or name (a to z, z to a)
- filter the catalog or search results by category, taste tag, country,
  region, price, degree of alcohol, producer, size, vintage and grape
  variety
- create and sign into an account
- view the website in French and English

### Users can...

- manage their account
- create and delete cellars
- add a description to a cellar
- add and remove bottles from a cellar
- add bottles from a private import to a cellar
- move bottles from one cellar to another
- search, sort and filter bottles using the criteria listed above
- sort bottles by quantity
- filter bottles by cellar
- leave notes on bottles
- report product catalog errors
- buy a recurring sommelier subscription

### Subscribers can...

- manage their subscription
- chat live with a professional sommelier
- view past conversations

### Administrators can...

- synchronize products with the SAQ catalog
- edit products
- generate statistics about users, cellars and products
- manage user accounts
- post articles about beverages (pairings, recipes, trends, etc.)

## SAQ catalog

The SAQ catalog is available through a [GraphQL] API, which you can
explore using Apollo's [Studio Explorer]. Here is the endpoint's URL:

```
https://catalog-service.adobe.io/graphql
```

And the headers:

```
x-api-key:7a7d7422bd784f2481a047e03a73feaf
magento-customer-group:b6589fc6ab0dc82cf12099d1c2d40ab994e8410c
magento-environment-id:2ce24571-9db9-4786-84a9-5f129257ccbb
magento-store-code:main_website_store
magento-store-view-code:fr
magento-website-code:base
```

[GraphQL]: https://graphql.org/learn/queries/
[Studio Explorer]: https://studio.apollographql.com/sandbox/explorer/
