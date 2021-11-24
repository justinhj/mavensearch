# Maven search

## Goal
Programmatically search Maven using Rust library that will eventually be a nvim plugin yay

## Resources
https://search.maven.org/classic/#api

Example query 

`curl https://search.maven.org/solrsearch/select\?q\=zio-json\&rows\=1\&wt\=json | jq`

Output

```
{
  "responseHeader": {
    "status": 0,
    "QTime": 2,
    "params": {
      "q": "zio-json",
      "core": "",
      "defType": "dismax",
      "spellcheck": "true",
      "qf": "text^20 g^5 a^10",
      "indent": "off",
      "fl": "id,g,a,latestVersion,p,ec,repositoryId,text,timestamp,versionCount",
      "start": "",
      "sort": "score desc,timestamp desc,g asc,a asc",
      "spellcheck.count": "5",
      "rows": "1",
      "wt": "json",
      "version": "2.2"
    }
  },
  "response": {
    "numFound": 31,
    "start": 0,
    "docs": [
      {
        "id": "dev.zio:zio-json_2.13",
        "g": "dev.zio",
        "a": "zio-json_2.13",
        "latestVersion": "0.2.0-M2",
        "repositoryId": "central",
        "p": "jar",
        "timestamp": 1636537987000,
        "versionCount": 9,
        "text": [
          "dev.zio",
          "zio-json_2.13",
          "-sources.jar",
          "-javadoc.jar",
          ".jar",
          ".pom"
        ],
        "ec": [
          "-sources.jar",
          "-javadoc.jar",
          ".jar",
          ".pom"
        ]
      }
    ]
  },
  "spellcheck": {
    "suggestions": []
  }
}
```

