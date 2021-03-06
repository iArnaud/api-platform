Dunglas's API platform
======================

*The new bread of web frameworks*

**The framework is still in development. The first public release is planned for
the end of June 2015**

Dunglas's API platform is a next-generation PHP web framework designed to create
API-first projects easily but without compromise in the field of extensibility and
flexibility:
- Use our awesome code generator to **bootstrap a fully-functional data model from
[Schema.org][8] vocabularies** with ORM mapping and validation (you can also do it
manually)
- **Expose in minutes an hypermedia REST API** that works out of the box by reusing
  entity metadata (ORM mapping, validation and serialization) ; that embraces [JSON-LD][1]
  and [Hydra][2] and provides a ton of features (CRUD, validation and error handling,
  relation embedding, filters, ordering...)
- Enjoy the **beautiful automatically generated API documentation** (Swagger-like)
- Add easily **[JSON Web Token][25] or [OAuth][26] authentication**
- Create specs and tests with a **developer friendly API context system** on top
  of [Behat][10]
- Develop your website UI, webapp, mobile app or anything else you want using
  **your preferred client-side technologies**! Tested and approved with **AngularJS**
  (integration included), **Ionic**, **React** and **native mobile** apps

Dunglas's API platform embraces open web standards (JSON-LD, Hydra, JWT, OAuth,
HTTP, HTML5...) and the [Linked Data][27] movement. Your API will automatically
expose structured data in Schema.org/JSON-LD. It means that your Dunglas's API
platform application is usable **out of the box** with technologies of the semantic
web.

It also that **your SEO will be improved** because **[Google recommends these formats][28]**.
And yes, Google crawls full-Javascript applications [as well as old-fashioned ones][29].

Last but not least, Dunglas's API platform is built on top of the [Symfony][5]
full-stack framework and follows its best practices. It means than you can:
- use **thousands of Symfony bundles** with API platform
- integrate API platform in **any existing Symfony application**
- reuse **all your Symfony skills** and benefit from the incredible
number of Symfony documentation
- enjoy the popular [Doctrine ORM][6] (used by default, but fully optional: you can
  use the data provider you want, including but not limited to MongoDB ODM and ElasticSearch)

Install
-------

Use [Composer][3] to create your new project:

    composer create-project dunglas/api-platform --stability=dev my-api

Start to hack
-------------

A demo application (a bookstore) is pre-installed.

* Run `app/console server:start` and open `http://localhost:8000` in any
  HTTP client to access the API.
* Open `http://localhost:8000/doc` to read the HTML documentation an play
  with the sandbox.
* Give a try to the [HydraConsole][4] client to leverage JSON-LD and Hydra
  features.
* Build your first custom client using Javascript, CORS headers are already
  configured. 

What's inside?
--------------

Dunglas's API platform provides rock solid foundations to build your project:

  * The full power of the [**Symfony**][5] framework and its ecosystem;

  * **[Doctrine][6] ORM/DBAL**;

  * [**PHP Schema**][7] to generate PHP entities from [Schema.org][8] types with Doctrine
    ORM mappings, Symfony validation and extended PHPDoc.

  * [**DunglasJsonLdApiBundle**][9] to expose in minutes your entities as
    a JSON-LD and Hydra enabled hypermedia REST API.
    
  * [**NelmioApiDocBundle**][24] integrated with DunglasJsonLdApiBundle to
    automatically generate a beautiful human-readable documentation and a
    sandbox to test the API.

  * [Behat][10] and [Behatch][11] configured to easily test the API.

  * An AppBundle you can use to start coding;

  * Annotations enabled for everything;

  * Swiftmailer and Twig to create beautiful emails;

It comes pre-configured with the following bundles:

  * [**Symfony**][5] - Dunglas's API platform is built on top of the
    full-stack Symfony framework

  * [**DunglasJsonLdApiBundle**][9] - Creates powerful Hypermedia APIs
    supporting JSON-LD and Hydra

  * [**NelmioCorsBundle**][12] - Support for CORS headers
  
  * [**NelmioApiDocBundle**][24] - Generates a human-readable documentation

  * [**FosHttpCacheBundle**][13] - Add powerful caching capacities, supports
    Varnish, Nginx a built-in PHP reverse proxy

  * [**SensioFrameworkExtraBundle**][14] - Adds several enhancements, including
    template and routing annotation capability

  * [**DoctrineBundle**][15] - Adds support for the Doctrine ORM

  * [**TwigBundle**][16] - Adds support for the Twig templating engine

  * [**SecurityBundle**][17] - Adds security by integrating Symfony's security
    component

  * [**SwiftmailerBundle**][18] - Adds support for Swiftmailer, a library for
    sending emails

  * [**MonologBundle**][19] - Adds support for Monolog, a logging library

  * **WebProfilerBundle** (in dev/test env) - Adds profiling functionality and
    the web debug toolbar

  * **SensioDistributionBundle** (in dev/test env) - Adds functionality for
    configuring and working with Symfony distributions

  * [**SensioGeneratorBundle**][20] (in dev/test env) - Adds code generation
    capabilities

All libraries and bundles included in Dunglas's API platform are
released under the MIT or BSD license.


Authentication support
----------------------

Json Web Token is a lightweight and popular way to handle authentication in a
stateless way. Install [**LexikJWTAuthenticationBundle**][21] to adds JWT support
to Dunglas's API platform.

Oauth support can also be easily added using [**FOSOAuthServerBundle**][22].

Enjoy!

Credits
-------

Built by [Kévin Dunglas][23]. Commercial support available upon request.

[1]:  http://json-ld.org
[2]:  http://hydra-cg.com
[3]:  http://getcomposer.org
[4]:  http://www.hydra-cg.com/
[5]:  http://symfony.com
[6]:  http://doctrine-project.org
[7]:  http://php-schema.dunglas.com
[8]:  http://schema.org
[9]:  https://github.com/dunglas/DunglasJsonLdApiBundle
[10]: http://behat.readthedocs.org
[11]: https://github.com/Behatch/contexts
[12]: https://github.com/nelmio/NelmioCorsBundle
[13]: http://foshttpcachebundle.readthedocs.org
[14]: http://symfony.com/doc/current/bundles/SensioFrameworkExtraBundle/index.html
[15]: http://symfony.com/doc/current/book/doctrine.html
[16]: http://symfony.com/doc/current/book/templating.html
[17]: http://symfony.com/doc/current/book/security.html
[18]: http://symfony.com/doc/current/cookbook/email.html
[19]: http://symfony.com/doc/current/cookbook/logging/monolog.html
[20]: http://symfony.com/doc/current/bundles/SensioGeneratorBundle/index.html
[21]: https://github.com/lexik/LexikJWTAuthenticationBundle
[22]: https://github.com/FriendsOfSymfony/FOSOAuthServerBundle
[23]: http://dunglas.fr
[24]: https://github.com/nelmio/NelmioApiDocBundle
[25]: http://jwt.io/
[26]: http://oauth.net/
[27]: http://en.wikipedia.org/wiki/Linked_data
[28]: https://developers.google.com/structured-data/
[29]: http://searchengineland.com/tested-googlebot-crawls-javascript-heres-learned-220157
