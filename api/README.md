TODO
----

* Define roles
    * Admin: Access everything
    * Signatory: (Better name?) Elligable for signature field
* Implement [CSRF](http://www.slimframework.com/docs/features/csrf.html)
* Implement [logging](https://github.com/Seldaek/monolog)

Schema brainstorming
--------------------
All schemas implicitly have id attribute

* Request belong to User
* Request has 0+ Users (CC list) (M:M index table)
* Request has 0+ Items
* Request attributes:
    * QuoteNum
    * VendName
    * Signature0 (One for each purchase level)
    * Signature1
    * Signature2
    * ...
* Item belongs to Request
* Item attributes:
    * PartNum
    * Description
    * Quantity
    * Price
* User has 0+ Requests
* User has 0+ Roles
* User attributes:
    * Name
    * Login
    * Email
* Role attributes:
    * Name
    * Description
