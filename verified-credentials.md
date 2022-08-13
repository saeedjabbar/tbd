## What are Verifiable Credentials(Vis)? 

When you hear the word verified credentials, what comes to mind? Is it a drivers liscenes, a passport, a birth certificate, college degree or student id? The common thread of these forms of credentials is that they are physical items, verified by recognized centralized bodies like a government agency or accredited university.  

So how does translate into the digital world where in a few clicks someone can make a fictious identity. Meet verifiable credentials(VCs),  a digitally signed electronic credential that follows an open standard, that lets you create, own, and manage your credentials across a variety of platforms. You can view the standard on W3C [here](https://www.w3.org/TR/vc-data-model/).

## Why do we need them?

Over the course of your digital history you've likely signed up for hundreds of apps and services with elements of your personal data fragmented, such as your name, email address, or more sensitive information like your date of birth, gender. These services then share your data with other third parties with or without your consent that you may not even be aware of. It's difficult to go back deactivate your profiles, delete your accounts, or reclaim in additional data these services have collected on you. Worse as if there is a data breach in one of these services and now your data is out in the public.

Verified Credentials aims to solve these problems by putting the power to manage your back into your hands. Imagine being able to own and control your personal data by only allowing access to services that require it and having the power to disable services that no longer need it. You can even manage your data on your own self hosted decentralized web node via an identity hub without relying on any centralized third party. 

Additional you can have multiple verified credentials for various use cases such as a student id, a drivers id, a passport or a certificate you earned. You can also have one specific verified credential with multiple presentation layers such as a passport where certain meta data is when used in a drivers id, such as your legal name and date of birth. See the W3C [documentation](https://www.w3.org/TR/vc-data-model/#presentations) for more on presentation layers.

## How do they work?

Who actually issues a verified credential, how does it get verified and who verifies the verifier? 

Let's look at the following example of the manual way credentials are issued. You've been accepted to your top university of choice and now need a student ID to access both the campus and online resources. Particulary you want to apply for a campus parking permit as well. 

Typically this process would involve you taking physical copies of multiple forms of ID verification such as a passport, birth certificate, and drivers ID to a physical office. Then after a few days of various checks, you're finally issued a physical student ID card from that university. The university trusts the entity that issued your birth certificate, passport, and drivers ID to create a student ID for you. They can even look up you by the identificaiton numbers on these documents. 

But what if someone in the admissions office, looked up your drivers ID and notice those parking tickets you had when you first got your liscenes. Were they even allowed to do so and could this bias their decision to give you a parking permit?

**The current process looks something like this.**

![https://i.imgur.com/VAllCMz.png](https://i.imgur.com/VAllCMz.png)



## Using Verified Credentials 

Before we dive into verified credentials, we need to first look at digital identifiers(DIDs). DIDs are unique identifiers that let us reference various verified credentials and the entities that also issue those credentials. For example a government can have their own unqiue DID, as well as a bank, and forms of credentials such as a birth certificate or drivers ID. You can see a growing list of DID identifiers [here](https://w3c.github.io/did-spec-registries/#did-methods). 

**DIDs use the following schema**

![did:example:12345abcde](https://w3c-ccg.github.io/did-primer/did-primer-diagrams/did-format.png)

*Credit: W3C*

DIDs can then be used to create a verified credential by electronically signing it and assigning it to a holder, similiarly to how blocks are cryptogrpahically linked in a blockchain. The holder can then choose how much of that credential they want to present to an entity requesting that credential. An example could be an employer, let's call them CompanyX, who looking up the DID of your college diploma from UniversityY. 

CompanyX would query the issuer of your diploma, in this case the UniversityY that issued it as a verified credential and also look up the DID of that university in a verfiable data registry (VDR). Think of VDR's as just lists that can managed and maintained by various parties such as wallets, financial instuitons, DAOs, non-profits, etc. If your credentitials are verified but some how UniversityY is on a list of non-accdeited instituions in the USA but accredited institutions in Europe, it would be up to the CompanyX to decide if they want to accept it.

The diagram below outlines the flow of this process.

![](https://www.w3.org/TR/vc-data-model/diagrams/ecosystem.svg)

*Credit: W3C*

Now we're going look at VCs, using the student who needs a student ID and a parking permit from our previous example. The university would run verification checks with the DIDs provided for each document such as the passport, drivers id, and birth certificate but the student would be limited to the scope of the presentation layer to just basic bio data that is required such as a legal name, date of birth, etc. So no one from the student department will be able to see your ticketing history on your drivers ID.

Below is  a high level overview of this process in the image below but for a more detailed view see the [W3C](https://www.w3.org/TR/vc-data-model/#credentials) documentation.

![](https://i.imgur.com/hGm7nKm.png)

## Use cases

-  Employment checks without being invasive 
- Managing of health records, land titles, etc
- Managing of various forms of personal identification such as passports, driver id's 
- KYC (Know Your Customer) checks for financial insitutions, businesses, etc
- Managing youe gamer profile across different metaverses
- Managing Memberships

DIDs and VCs allow us to create credentials and identities on an interoperable ecosystem that allow developers and businesse to build a new wave of products, applications, and services that put users in control.