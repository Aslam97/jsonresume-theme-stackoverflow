# Stack Overflow theme for jsonresume [![npm version](https://badge.fury.io/js/jsonresume-theme-stackoverflow.svg)](http://badge.fury.io/js/jsonresume-theme-stackoverflow)

**Printable version with custom CSS**

[DEMO](https://francesco.netlify.app/)

## Getting started

### Install the command line

Create your resume in json on [jsonresume](https://jsonresume.org)

The official [resume-cli](https://github.com/jsonresume/resume-cli) to run the development server.

Go ahead and install it:

```
npm install -g resume-cli
```

### Install and serve theme

Clone the repository

```
git clone https://github.com/francescoes/jsonresume-theme-stackoverflow.git
```

Create a new file `resume.json` in the root of the project and paste your resume JSON in it. You can use the [official JSON Resume schema](https://jsonresume.org/schema/) or the extended version below.

Install dependencies:

```
npm install
```

and simply run:

```
resume serve --theme .
```

### Social Profiles Icons

**Profiles supported with brand colors:**

Please note that all the [Font awesome brands icons](https://fontawesome.com/search?s=brands) are supported. Although only the ones listed below have a color code associated with it in my CSS file:

github, stack-overflow, linkedin, dribbble, twitter, facebook, pinterest, instagram, soundcloud, wordpress, youtube, flickr, google plus, tumblr, foursquare.

To have a social icon close the social link profile (or username) it is enough to set a `network` the name of the Social Network (es: 'Stack Overflow'). I am replacing spaces with dashes (`-`) and transforming all the network name to all lowercase to match the Font awesome naming convention for brands icons.

#### Support to extra fields

With stackoverflow theme it is possible to add:

- `keywords` to each 'work', 'publication' and 'volunteer' item
- `summary` to each 'interests' and 'education' item
- `birth` to 'basics' (might be commonly used in Europe)

example of the extra `birth` object:

```
"birth": {
  "place": "New York",
  "state": "USA",
  "date": "1988"
}
```

## Example Resume JSON

This is the extended JSON structure for a resume. It includes extra fields that are not part of the official JSON Resume schema.

### Skills

Available skills levels are:

- Beginner
- Intermediate
- Advanced
- Fluent
- Master
- Native speaker

### JSON

```json
{
  "basics": {
    "name": "John Doe",
    "label": "Programmer",
    "image": "",
    "birth": {
      "place": "New York",
      "state": "USA",
      "date": "1988"
    },
    "website": "https://johndoe.com",
    "email": "john@gmail.com",
    "phone": "(912) 555-4321",
    "location": {
      "address": "2712 Broadway St",
      "postalCode": "CA 94115",
      "city": "San Francisco",
      "countryCode": "US",
      "region": "California"
    },
    "profiles": [
      {
        "network": "Twitter",
        "username": "john",
        "url": "https://twitter.com/john"
      }
    ],
    "summary": "A summary of John Doe…"
  },
  "skills": [
    {
      "name": "Web Development",
      "level": "Master",
      "levelDisplay": "Master",
      "keywords": ["HTML", "CSS", "JavaScript"]
    }
  ],
  "work": [
    {
      "company": "Company",
      "position": "President",
      "website": "https://company.com",
      "startDate": "2013-01-01",
      "endDate": "2014-01-01",
      "summary": "Summary…",
      "highlights": ["Started the company"],
      "location": {
        "city": "San Francisco",
        "region": "California"
      },
      "url": "https://company.com",
      "keywords": ["HTML", "CSS", "JavaScript"]
    }
  ],
  "projects": [
    {
      "name": "Project",
      "startDate": "2019-01-01",
      "endDate": "2021-01-01",
      "highlights": ["Won award at AIHacks 2016"],
      "url": "https://project.com",
      "location": {
        "city": "San Francisco",
        "region": "California",
        "countryCode": "US"
      },
      "keywords": ["HTML", "CSS", "JavaScript"],
      "summary": "Summary..."
    }
  ],
  "volunteer": [
    {
      "organization": "Organization",
      "startDate": "2012-01-01",
      "endDate": "2013-01-01",
      "position": "Volunteer",
      "website": "https://organization.com",
      "summary": "Summary…",
      "highlights": ["Awarded 'Volunteer of the Month'"],
      "location": {
        "city": "San Francisco",
        "region": "California",
        "countryCode": "US"
      },
      "keywords": ["HTML", "CSS", "JavaScript"]
    }
  ],
  "education": [
    {
      "institution": "University",
      "url": "https://institution.com/",
      "area": "Software Development",
      "studyType": "Bachelor",
      "startDate": "2011-01-01",
      "endDate": "2013-01-01",
      "gpa": "4.0",
      "courses": ["DB1101 - Basic SQL"],
      "location": {
        "city": "San Francisco",
        "region": "California",
        "countryCode": "US"
      },
      "summary": "Summary…"
    }
  ],
  "awards": [
    {
      "title": "Award",
      "date": "2014-11-01",
      "awarder": "Company",
      "summary": "Summary…"
    }
  ],
  "certificates": [
    {
      "name": "Certificate",
      "date": "2021-11-07",
      "issuer": "Company",
      "url": "https://certificate.com"
    }
  ],
  "publications": [
    {
      "name": "Publication",
      "publisher": "Company",
      "releaseDate": "2014-10-01",
      "website": "https://publication.com",
      "summary": "Summary…",
      "keywords": ["HTML", "CSS", "JavaScript"]
    }
  ],
  "languages": [
    {
      "language": "English",
      "fluency": "Native speaker",
      "fluencyDisplay": "Native speaker"
    }
  ],
  "interests": [
    {
      "name": "Wildlife",
      "summary": "Summary…",
      "keywords": ["Ferrets", "Unicorns"]
    }
  ],
  "references": [
    {
      "name": "Jane Doe",
      "reference": "Reference…"
    }
  ]
}
```

## Contribution

Fork the project, add your feature (or fix your bug) and open a pull request OR

[Open an issue](https://github.com/francescoes/jsonresume-theme-stackoverflow/issues/new) if you find find or if you would like to have extra fields or changes

## License

Available under the [MIT license](http://opensource.org/licenses/mit-license.php).
