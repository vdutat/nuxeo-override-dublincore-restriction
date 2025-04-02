# nuxeo-override-dublincore-restriction

## About / Synopsis

This plugin demonstrates how to override the `dublincore` schema in order to enforce a 64-character maximum length on property `dc:title`.

It was generated with the following commands:
```
mmkdir nuxeo-override-dublincore-restriction && cd $_
nuxeo b multi-module contribution
mkdir -p nuxeo-override-dublincore-restriction-core/src/main/resources/schema
# edit nuxeo-override-dublincore-restriction-core/src/main/resources/schema/dublincore.xsd
# edit nuxeo-override-dublincore-restriction-core/src/main/resources/OSGI-INF/overrideschemadublincore-contrib.xml
# change maven-internal to maven-private in parent POM
mvn clean package

nuxeo b package
mvn install
```

## Requirements

Building requires the following software:

* git
* maven

## Build

```
git clone ...
cd nuxeo-override-dublincore-restriction

mvn clean install
```

[![Java CI with Maven](https://github.com/vdutat/nuxeo-override-dublincore-restriction/actions/workflows/maven.yml/badge.svg)](https://github.com/vdutat/nuxeo-override-dublincore-restriction/actions/workflows/maven.yml)

## Installation

```
nuxeoctl mp-install nuxeo-override-dublincore-restriction/nuxeo-override-dublincore-restriction-package/target/nuxeo-override-dublincore-restriction-*.zip
```

## Support

**These features are not part of the Nuxeo Production platform, they are not supported**

These solutions are provided for inspiration and we encourage customers to use them as code samples and learning resources.

This is a moving project (no API maintenance, no deprecation process, etc.) If any of these solutions are found to be useful for the Nuxeo Platform in general, they will be integrated directly into platform, not maintained here.


## License

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)

## About Nuxeo

Nuxeo Platform is an open source Content Services platform, written in Java. Data can be stored in both SQL & NoSQL databases.

The development of the Nuxeo Platform is mostly done by Nuxeo employees with an open development model.

The source code, documentation, roadmap, issue tracker, testing, benchmarks are all public.

Typically, Nuxeo users build different types of information management solutions for [document management](https://www.nuxeo.com/solutions/document-management/), [case management](https://www.nuxeo.com/solutions/case-management/), and [digital asset management](https://www.nuxeo.com/solutions/dam-digital-asset-management/), use cases. It uses schema-flexible metadata & content models that allows content to be repurposed to fulfill future use cases.

More information is available at [www.nuxeo.com](https://www.nuxeo.com).

