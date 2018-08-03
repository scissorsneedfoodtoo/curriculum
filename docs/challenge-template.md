### Lesson Template

```
{
  "id": "Unique identifier (alphanumerical, MongoDB _id)",
  "title": "Challenge Title",
  "description": [
    "A Description of the challenge and what is required to pass",
    "A new string in the array will create a new paragraph."
  ],
  "tests": [
    {
      "text": "Should return \"foo\".",
      "testString": "A stringified function using Chai asserts"
    }
  ],
  "challengeType": 1,
  "translations": {
    "language-code": {
      "title": "The Title in a Different Language",
      "description": [
        "The description in a different language."
      ]
    }
  },
  "files": {
    "indexjs": {
      "key": "indexjs",
      "ext": "js",
      "name": "index",
      "contents": [
        "// code displayed in the editor by default",
        "// a new string in the array is a new line"
      ],
      "head": [
        "A place for test setup",
        "Can be thought of as mocha's beforeEach()"
      ],
      "tail": [
        "A place for test tear down",
        "Can be thought of as mocha's afterEach()"
        ]
    }
  }
},
```