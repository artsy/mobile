# Artsy in a Nutshell

If you're interested in how the engineering team is set up specifically, I'd recommend this blog post: [Artsy's Engineering Organization Stack, 2016](http://artsy.github.io/blog/2016/03/28/artsy-engineering-organization-stack/). I'll be quoting it in here occasionally.

Artsy is well known for our work in the open source domain, but as developers we regularly get asked "What is Artsy?"  Well, Artsy pays our wages, so we probably owe you and the company an explanation.

The mission:

> Artsy is a company whose mission is to make all the world’s art accessible to anyone with an Internet connection.

With a vision of:

> A world where art is as popular a part of culture as music.

Artsy has 5 core values:

* Art meets Science 
* People are Paramount 
* Quality Worthy of Art 
* Positive Energy 
* Openness

### What does this mean in practice?

We map large aspects of the Art world in our apps and websites: [Shows](https://www.artsy.net/art-fairs), [Galleries](https://www.artsy.net/galleries), [Fairs](https://www.artsy.net/art-fairs), [Auctions](https://www.artsy.net/auctions), [Museums & Institutions](https://www.artsy.net/institutions).

> We are a resource for art collecting and education. Artsy features the world’s leading galleries, museum collections, foundations, artist estates, art fairs, and benefit auctions, all in one place. Our growing database of 350,000 images of art, architecture, and design by 50,000 artists spans historical, modern, and contemporary works, and includes the largest online database of contemporary art. Artsy is used by art lovers, museum-goers, patrons, collectors, students, and educators to discover, learn about, and collect art.

Currently we are [about ~140](https://www.linkedin.com/company/802712?trk=vsrp_companies_cluster_name&trkInfo=VSRPsearchId%3A202598361462836584173%2CVSRPtargetId%3A802712%2CVSRPcmpt%3Acompanies_cluster) [people](http://artsy.github.io/blog/2016/03/28/artsy-engineering-organization-stack/).

The development team is ~30 people, working on a mix of mature and shiny technologies.

### How do we make money?

From [Artsy's Engineering Organization Stack, 2016](http://artsy.github.io/blog/2016/03/28/artsy-engineering-organization-stack/):

> Artsy has 3 businesses: _Listings_, _Marketplace_ and _Content_.

> **Listings**: Artsy [gallery partners](https://www.artsy.net/galleries) pay a flat monthly subscription fee to list an unlimited number of artworks for sale, plus a host of other benefits. They do not pay a commission fee on sales made through Artsy.

> **Marketplace**: In 2015 Artsy expanded into hosting commercial auctions on our platform. Much like our Listings business, we work with top auction houses. The latter pay commissions from sales. Check out [current auctions on Artsy](https://www.artsy.net/auctions).

> **Content**: We are also working on making Artsy a go-to platform for brands to co-create and distribute content that engages a global arts and culture audience. In 2015 we debuted our first sponsored content feature on Artsy, a [series of 11 educational short films about the Venice Biennale in partnership with UBS](https://www.artsy.net/venice-biennale-2015) (if anything, [watch this amazing video](https://www.artsy.net/article/artsy-editorial-behind-the-venice-biennale-2015-a-short-history-of-the-world-s-most-important-art-exhibition)).

### How/why do you produce so much OSS?

We bake it into our engineering team culture. I'll quote the [Artsy team culture post on objc.io](https://www.objc.io/issues/22-scale/artsy/)

> The Artsy mobile team is small, especially in contrast to the other teams in this issue of objc.io. Despite this, we’re notable for our impact on the community. Members of our iOS development team are — and have been — involved in almost all major open-source projects in the Cocoa community.

...

> There are well-understood reasons to reduce the size and complexity of any given codebase. By writing small, well-tested components, we increase the overall stability and cohesion of our apps. Additionally, by writing reusable libraries, we reduce effort when building multiple apps.

...

> Dividing our applications into small, reusable pieces has a lot of technical advantages, but it also allows us to create distinct owners for the different components. When we do this, we need to make sure that we consciously spread knowledge to other team members

...

> People often ask why we operate in the open as we do. We’ve already discussed our technical motivations, as well as the sense of purpose it gives individual team members, but honestly, working in the open is just smart business. For example, we’re working on a single open-source library to handle authentication with our API. Not only does this make writing apps against our API easier for us, but it makes it easier for everyone else. Huzzah!


...

> We do know that some of our competitors use our code, because they offer their fixes back to us. We do the same. In reality, the biggest challenge to a business open sourcing a project is the obligation of stewardship. This responsibility is mostly a matter of working with people and needs to be managed correctly — especially if a project gains enough popularity. Most projects don’t get large enough for their stewardship to become burdensome.

...

> The extra time necessary to create and maintain open-source code often helps us unwind and relax from our day-to-day tasks, and over-communicating on GitHub has helped the remote members of our team.

We take the time to educate the rest of the team about why OSS is important for us, ranging [from company videos](http://code.dblock.org/2015/02/09/becoming-open-source-by-default.html) to in-house training sessions on GitHub. We work hard on this. 

To quote [dblock](http://code.dblock.org)'s post on [OSS by Default](http://code.dblock.org/2015/02/09/becoming-open-source-by-default.html):

> To quote Scott Berkun’s A Year Without Pants: attributes of culture don’t arrive by some technique sprinkled around the company years after it started. This applies to organizations and individuals alike - I didn’t start my Engineering career with open-source, but my thinking has evolved, naturally, to a point where I was enthusiastic about it, and then to a place where I was doing it every day.

...

> Nobody ever told me that I must write open-source software. I have written and continue to write mountains of closed-source code and create more closed-source projects every day. However, as many engineers, I am motivated to create smaller, nimbler, reusable and well-tested components. Well designed libraries reduce the size of any application and help keep code dry. Well documented systems are easier to use by new team members. Well tested ones are faster to add features to and don’t break as often. By default, I contribute to other people’s generic open-source solutions to save time and money by not reinventing the wheel. Taking this further, I spend significant amount of time extracting non-domain-specific code into new or existing open-source libraries, reducing the footprint of the proprietary applications I work on.

We consider working in OSS the best way to be competitive.

### Do you like Art?

Aye.
