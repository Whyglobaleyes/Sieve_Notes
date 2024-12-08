# Sieve_Notes
Some help-notes for writing Sieve filters: would be great to find a working tool/ GUI for this or Geany Syntax highlighting



## Sieve
A language/ protocol used by email servers specifying `filters` to be applied to email messages that are then `filed`/ `actioned` .


## GENERAL SYNTAX

#### Line Ending
Every line must be terminated with a semi-colon 

#### Shebang
Every SieveFile starts with a first line specifying the extensions (modules) needed
 `require ["imap4flags","copy", "fileinto", "mailbox", "body", "envelope", "reject"];` 

#### Comments
Either bash-script `# hash symbol` or PHP-style `/* this is a comment, can be multiline */` comments are allowed .


------

# AVAILABLE EXTENSIONS 

* imap4flags
* copy
* fileinto
* mailbox
* body
* envelope
* reject

------

# AVAILABLE FILTERS

## SENT MESSAGES
> 
> Maybe This Works:
>
>       if exists "Delivered-To" {expire "day" "30";}
>
> https://www.reddit.com/r/ProtonMail/comments/16gt82i/sieve_filter_and_sent_messages/?rdt=61556
### -OR- 
set a domainwide bcc every message then filter the inbound messages to select the ones sent by me 

------

# AVAILABLE ACTIONS 

-----------------------------

##### References
1. https://en.m.wikipedia.org/wiki/Sieve_(mail_filtering_language)
2. https://web.archive.org/web/20041126062029/http://www.cyrusoft.com/sieve/
3. https://p5r.uk/blog/2011/sieve-tutorial.html
4. https://docs.gandi.net/en/gandimail/sieve/sieve_tutorial.html
5. https://help.alwaysdata.com/en/e-mails/use-sieve-scripts/
6. https://www.pair.com/support/kb/sieve-syntax-and-common-recipes/
7. https://support.sparkpost.com/momentum/3/3-reference/sieve-syntax-basic
8. https://www.fastmail.help/hc/en-us/articles/360060591373-How-to-use-Sieve
9. https://www.fastmail.help/hc/en-us/articles/360058753794-Sieve-examples
10. https://support.tigertech.net/sieve
