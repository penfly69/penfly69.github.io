---
title: "Which Secure Email Provider Is the One For You?"
---


Posted by: DeepDotWeb
    
    
<span>August 3, 2015</span>


       
<p>As privacy consciousness has increased, phrases like “zero knowledge” and “end-to-end encryption” have become buzzwords of sorts. Many businesses, products, and online services have sprung up in the wake of Edward Snowden hoping to get a slice of the rapidly expanding market for privacy-enhancing technology. But which ones are all talk and which deliver? Let&#8217;s take a look at a few email providers who might fit the bill.</p>
<p style="text-align: center;"><a href="/vpn-comparison-chart/">&gt;&gt;Hide Your Tor usage from your ISP &#8211; Click here for the best VPN&#8217;s&lt;&lt; </a></p>
<p><strong>ProtonMail</strong></p>
<p>Started in 2013, <a href="https://protonmail.ch/">ProtonMail</a> specifically cites Edward Snowden as an inspiration for their service. They make a big deal out of two things: the fact that they are based in Switzerland, and their two password system. The gist is that ProtonMail is marketing themselves as the “Swiss bank account” of email providers. Indeed, they say just that on <a href="https://protonmail.ch/pages/security-details">the page</a> detailing their security measures: their servers “are colocated in some of the same secured and guarded datacenters used by Switzerland&#8217;s famed private banks”. Elsewhere they boast of a “secure datacenter facility hidden inside a Swiss granite mountain” and that this is a “former military command center deep inside the Swiss Alps”.</p>
<p>This all sounds very impressive, but what&#8217;s the nitty gritty? The touted two password system works as follows: the first password logs the user into their account. This leads to a page titled “Decrypt mailbox” prompting them to enter a second password. This password unlocks the user&#8217;s symmetrically encrypted 2048 bit private RSA key which in turn decrypts their mailbox. The decryption process happens entirely locally in the client&#8217;s browser using JavaScript so that there is no room for ProtonMail to intercept the passphrase protecting the secret key. The private key and mailbox are both encrypted using AES-256. It is an implementation of OpenPGP.js.</p>
<p>ProtonMail is still in beta but the user experience is on the whole very smooth and mature. There may be a short wait if you request an account at the moment, as a sudden spike in popularity coinciding with their IndieGoGo campaign maxed out their servers.</p>
<p>In the meantime many exciting features are in the pipeline. While they strive to make the encryption and decryption invisible in the name of usability, optional key management is on its way allowing users to import GPG keys of non-ProtonMail users so that the security can interoperate with other services. Aliases are also coming soon.</p>
<p>If you and a non-ProtonMail user can agree on a passphrase beforehand, you can also exchange end-to-end encrypted messages with people who have no knowledge of cryptography whatsoever. ProtonMail&#8217;s code is not yet open source but they have announced plans to release it in the future.</p>
<p><strong>Tutanota</strong></p>
<p>If you&#8217;re looking for a service that&#8217;s a little more mature than ProtonMail, the German provider <a href="https://tutanota.de/">Tutanota</a> may be for you. Founded in 2011, they <a href="https://tutanota.de/blog/posts/beta-time-is-over-release-notes">officially</a> left beta on the 24<sup>th</sup> March 2015. Notably, Tutanota does <em>not </em>utilise the popular PGP method for encrypting messages. Instead, they <a href="https://tutanota.uservoice.com/knowledgebase/articles/470724-why-does-tutanota-not-use-pgp">explain</a>, theirs is a custom solution using 2048 bit RSA keys and AES-128 created on the compelling grounds that PGP does not encrypt the subject line of emails. If you are wary of using cryptography that&#8217;s less tried and tested, some reassurance may be found in the fact that Tutanota, unlike ProtonMail, has already open sourced its code. Tutanota also has apps for iOS and Android, and a plugin for Outlook so that users don&#8217;t have to access their accounts using a web browser – all developments that are still on the cards for ProtonMail.</p>
<p>However Tutanota logs users in and decrypts their mailboxes using the same passphrase, which means a little more trust is required if you are to believe the claim that they can&#8217;t and won&#8217;t access users&#8217; messages. Nonetheless the user experience is just as smooth as ProtonMail&#8217;s and Tutanota also allows email exchanges encrypted by passphrase for private correspondence with users of other services.</p>
<p>If you need your account immediately, Tutanota is probably the best choice as there is no longer a waiting period to take advantage of their services. When creating your account you can also choose from a variety of domains: tutanota.de, tutanota.com, tutamail.com, keemail.me, and my personal favourite: tuta.io. Tutanota <a href="https://tutanota.de/blog/posts/tutanota-and-tor">warns</a> that the account creation process freezes if you use Tor Browser inside Windows, so watch out if that is your intention, but they are working on fixing this.</p>
<p><strong>Lavaboom</strong></p>
<p>Also from Germany is Lavaboom which started in 2013 and might be described as a cross between ProtonMail and Tutanota in that it utilises OpenPGP.js but uses a single password system. The similarly named Lavabit famously shut down rather than hand over its private SSL key to the US government as part of its investigation into Edward Snowden&#8217;s leak. Lavaboom, which came about shortly afterwards, is clearly named in its honour.</p>
<p>Lavaboom has opted to use <a href="https://lavaboom.com/security">4096 bit RSA keys</a> – twice the size of ProtonMail&#8217;s and Tutanota&#8217;s. If a strong key is the most important thing to you, this may be the best choice. When creating your account, you are offered to choose between using “Lavaboom sync”, meaning Lavaboom&#8217;s servers store your private keys encrypted or saving your keys to your browser&#8217;s cache. The downside of the latter method is that in the event your cache is wiped, you will no longer be able to access your emails unless you have saved a back up of your key and re-upload it when you next log in, so be careful that you don&#8217;t lose access to your inbox by destroying your keys.</p>
<p>I did find that Lavaboom&#8217;s user experience isn&#8217;t quite as mature as Tutanota&#8217;s and ProtonMail&#8217;s. When creating my account and sometimes when logging in using Tor Browser inside Linux, the loading page freezes at “Initializing OpenPGP.js” requiring me to refresh the page until it works properly. Nonetheless, Lavaboom is still in beta so we can expect quirks like this to be ironed out. I hope that in the course of this, the process of choosing between caching your keys or using Lavaboom sync is made clearer, as it was initially a bit confusing for a provider whose aim is make encryption easy. However it could be appealing if you&#8217;re looking for more fine-grained control than ProtonMail and Tutanota can offer.</p>
<p><strong>Honourable Mentions</strong></p>
<p>You may notice that not only do the three providers reviewed here all use JavaScript-based encryption and decryption, but they are also all hosted on the clearweb. Though they are Tor-friendly, you may be looking for providers that host their own Tor-hidden services.</p>
<p>If so, <a href="http://lelantoss7bcnwbv.onion/">Lelantos</a> is a paid though cheap service on Tor who may interest you. It is a little more advanced than the other three but it offers some impressive features like allowing users to import their own public key so that, if they are sent unencrypted emails, they are encrypted automatically on entering the server. While it is much better if the sender encrypts the message before sending, it is still preferable to no encryption at all. Members are also allowed to register over 100 aliases and create temporary addresses. A lifetime account costs 0.136BTC, or about $32.</p>
<p><a href="http://sigaintevyh2rzvw.onion/">S</a><a href="http://sigaintevyh2rzvw.onion/">igaint</a> offers both free and paid versions of their service. Their upgrade page explains the difference between the two plans: a $30 lifetime subscription grants you increased storage, SMTPS/IMAPS/POP3S support, full disk encryption, easier PGP integration, Bitmessage support, and priority customer service.</p>
<p><a href="http://s4bysmmsnraf7eut.onion/">R</a><a href="http://s4bysmmsnraf7eut.onion/">uggedinbox.com</a> is a fully free email provider offering both clearweb access over TLS/SSL and a Tor onion site. If you&#8217;d like a privacy-friendly email provider and don&#8217;t mind managing your own PGP keys, this is an attractive choice. IMAP, POP3, and SMTP are all free of charge and you can also create temporary accounts with a pre-set expiry date. When logging in to web mail, you can choose between the JS-less SquirrelMail or the more modern RoundCube which requires JS. While free, users are encouraged to donate to their BTC address on their homepage. RuggedInbox also sells <a href="http://s4bysmmsnraf7eut.onion/prices.php">VPSes</a> to those who want their own private email servers.</p>
<p>While it may be a nuisance, the best security is always offered by being in control of your own private key. Services that simplify key management often sacrifice a large amount of that control, but for the purpose of emailing people without knowledge of cryptography, the increase in security and privacy is significant when compared to providers like Hotmail or Gmail. Therefore, if all you are looking for is to go about your daily activities with greater privacy, providers like ProtonMail, TutaNota and Lavaboom offer you just that. For extraordinary protection, never trust your key management to a third party.</p>
    
    

Updated: 2015-08-03
    
    

