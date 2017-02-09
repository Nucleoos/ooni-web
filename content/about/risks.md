# Risks: Things you should know before using ooniprobe

OONI's software tests (called ooniprobe) are designed to test networks for
symptoms of censorship, surveillance and traffic manipulation and, in some
countries around the world, **legal** and/or **extra-legal risks** could emerge.
We therefore strongly urge you to consult with lawyers *prior* to downloading,
installing and running ooniprobe, and to carefully read the documentation below.

* [*Legal and extra-legal risks*](#legal-and-extra-legal-risks)

* [*Detection of ooniprobe usage*](#detection-of-ooniprobe-usage)

    * [*Surveillance*](#surveillance)

    * [*Tested services*](#tested-services)

    * [*Physical or remote access to a user's device*](#physical-or-remote-access-to-a-users-device)

    * [*Publication of measurements*](#publication-of-measurements)

* [*ooniprobe software tests*](#ooniprobe-software-tests)

    * [*Legality of tested websites*](#legality-of-tested-websites)

    * [*Legality of ooniprobe tests*](#legality-of-ooniprobe-tests)

    * [*Legality of anonymity software*](#legality-of-anonymity-software)

* [*Legal advice*](#legal-advice)

**Note:** The risks described below are quite speculative. To our
knowledge, no ooniprobe user has ever faced consequences from the risks
described below. Nonetheless, we strongly encourage you to read the following
information regarding potential risks associated with the use of ooniprobe.

## Legal and extra-legal risks

The legal risks of downloading, installing and running ooniprobe can vary from
country to country, which is why we advise you to consult with local lawyers. In
extreme cases, any form of active network measurement could be illegal, or even
considered a form of espionage.

Many countries have a lengthy history of subjecting digital rights activists to
various forms of abuse that could make it dangerous for individuals in these
countries to run ooniprobe. The use of ooniprobe might therefore subject users
to severe civil, criminal, or extra-judicial penalties, and such sanctions can
potentially include:

* Imprisonment

* Physical assaults

* Large fines

* Receiving threats

* Being placed on government watchlists

* Targeted for surveillance

While most countries don't have laws which specifically prohibit the use of
network measurement software, it's important to note that the use of ooniprobe
can *still* potentially be criminalized in certain countries under other,
broader laws if, for example, its use is viewed as an illegal or anti-government
activity. ooniprobe users might also face the risk of being criminalized on the
grounds of *national security* if the data obtained and published by running
ooniprobe is viewed as jeopardizing the country's external or internal security.

We strongly encourage you to consult with lawyers and understand legal risks
*prior* to running ooniprobe. Some questions you can ask lawyers related to the
use of ooniprobe can include the following:

* Does country X have laws in force that restrict or prohibit the use of:

  * **network measurement software**?

  * **censorship detection software**?

  * **censorship circumvention software**?

* Does country X have laws in force that restrict or prohibit certain types
  of **internet access**? (for example, is it illegal to access certain
  websites?)

* Does country X have laws in force or ISP License Agreements that require
  Internet Service Providers (ISPs) to track users' online activities and to
  retain such records?

* Have laws or rules in country X ever been used to criminalize groups or
  individuals based on their internet activity? (this does not necessarily need
  to be specific to network measurements)

## Detection of ooniprobe usage

Various legal and extra-legal risks (as explained in the previous section) might
potentially emerge if third parties (such as governments and ISPs) who view the
use of ooniprobe as an illegal or generally "suspicious" activity detect an
ooniprobe user.

The use of ooniprobe can potentially be detected by third parties through the
following:

### Surveillance

Third parties (such as your government, ISP and/or employer) monitoring your
internet activity will be able to see all web traffic generated by ooniprobe,
including your IP address, and might be able to link it to you personally.

Many countries employ sophisticated surveillance measures that allow governments
to track individuals' online activities – even if they are using a VPN or a
proxy server to protect their privacy. In such countries, governments might be
able to identify you as an ooniprobe user regardless of what measures you take to
protect your online privacy. 

### Tested services

Services connected to by ooniprobe will be able to see your IP address and might be
able to detect that you are using ooniprobe. You can view which services ooniprobe tests
[here](https://github.com/citizenlab/test-lists/tree/master/lists).

### Physical or remote access to a user's device

As with any other software, the usage of ooniprobe can leave traces. As such,
anyone with physical or remote access to your computer might be able to see
that you have downloaded, installed or run ooniprobe.

To remove traces of ooniprobe usage, you can re-install your operating system or
wipe your computer and remove everything (operating system, programs and files)
from your hard drive.

### Publication of measurements

The public (including third parties who view the usage of ooniprobe as illegal or
"suspicious") will be able to see the information collected by ooniprobe once it's
published through:

* [OONI Explorer](https://explorer.ooni.torproject.org/world/)

* [OONI's list of measurements](https://measurements.ooni.torproject.org/)

Unless users **[opt-out](https://ooni.torproject.org/about/data-policy/)**, all
measurements that are generated through ooniprobe tests are by default sent to
OONI's measurement collector and automatically published through the above
resources.

Published data will include your approximate location, the network (ASN) you are
connecting from, and when you ran ooniprobe. Other identifying information, such
as your IP address, is *not* deliberately collected, but might be included in
HTTP headers or other metadata. The full page content downloaded by ooniprobe
could potentially include further information if, for example, a website
includes tracking codes or custom content based on your network location. Such
information could potentially aid third parties in detecting you as an ooniprobe
user.

## ooniprobe software tests

OONI has developed multiple free software tests, each one of which is designed
to perform a different function and can therefore potentially entail different
types of legal and/or extra-legal risks.

In summary, OONI's tests are designed to:

* Examine whether websites are blocked

* Examine whether instant messaging (IM) apps (such as WhatsApp or Facebook Messenger) are blocked

* Detect the presence of systems which might be responsible for censorship,
  surveillance and traffic manipulation

* Examine whether censorship circumvention tools, such as [Tor
bridges](https://bridges.torproject.org/), [Psiphon](https://psiphon.ca/) and
[Lantern](https://getlantern.org/), are blocked

We urge you to review the
**[specifications](https://github.com/TheTorProject/ooni-spec/tree/master/test-specs)**
for each ooniprobe test carefully, prior to running them.

### Legality of tested websites

When running OONI's [web connectivity test](https://ooni.torproject.org/nettest/web-connectivity/) you will connect to and download data from various websites
which are included in the following two lists:

* **[Country-specific test list](https://github.com/citizenlab/test-lists/tree/master/lists)** 
  (search for your country's test list based on its country code)

* **[Global test list](https://github.com/citizenlab/test-lists/blob/master/lists/global.csv)** 
  (including a list of globally accessed websites)

Many websites included in the above lists will likely be controversial and can
include pornography or hate speech, which might be illegal to access in your
country. We therefore recommend that you examine carefully whether you are
willing to take the risk of accessing and downloading data from such websites
through ooniprobe tests.

If you are uncertain of the potential implications of connecting to and
downloading data from the websites listed in the above lists, you can pass your
*own* test list with the ooniprobe `-f` command line option.

### Legality of ooniprobe tests

While network measurements or the use of censorship detection software might not
be illegal per se, some network tests that ooniprobe does might be against the *terms
of service of your Internet Service Provider (ISP)* or legally questionable in
your country.

OONI's **[HTTP-invalid-request-line](https://ooni.torproject.org/nettest/http-invalid-request-line/)** test, for example, *might* trigger the suspicion of
your ISP when sending out-of-spec messages to an echo service. Some ooniprobe
tests are designed to connect to and download data from potentially legally
questionable websites (as mentioned in the previous section), while others
examine the reachability of instant messaging apps and circumvention tools (such
as [Psiphon](https://psiphon.ca/) and [Lantern](https://getlantern.org/)) which
might be illegal or viewed as controversial in some countries.

### Legality of anonymity software

The installation of [Tor](https://www.torproject.org/) software, which is
designed for online anonymity, is a *prerequisite* for using ooniprobe.

Furthermore, OONI's **[Vanilla Tor](https://ooni.torproject.org/nettest/vanilla-tor/)** test is designed to examine the
reachability of the Tor network, while OONI's **[bridge-reachability](https://ooni.torproject.org/nettest/tor-bridge-reachability/)**
test is designed to check whether [Tor bridges](https://bridges.torproject.org/)
are blocked or not.

Similarly, the following OONI tests require the installation of circumvention
software:

* **[Psiphon](https://ooni.torproject.org/nettest/psiphon/)**

* **[Lantern](https://ooni.torproject.org/nettest/lantern/)**

We therefore encourage you to consult with a lawyer on the legality of anonymity
software (such as Tor, a VPN or a proxy) *prior* to using ooniprobe.

## Legal advice

In addition to consulting with laywers, you can also reach out to us with
specific inquiries at **contact@openobservatory.org**. Please note though that we
are *not* lawyers, but we might be able to seek legal advice for you or to put
you in touch with lawyers who could address your questions and/or concerns.

Some relevant resources include:

* [Tor Legal FAQ](https://www.eff.org/torchallenge/faq.html)

* [EFF Know Your Rights](https://www.eff.org/issues/know-your-rights)


**Note:** The use of ooniprobe is at your *own risk* in accordance to OONI's software
[license](https://github.com/TheTorProject/ooni- probe/blob/master/LICENSE) and
neither the OONI project nor its parent organization, the Tor Project, can be
held liable.