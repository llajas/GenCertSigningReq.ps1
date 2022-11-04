Creating SSL Certificate Requests needs a lot of Time, so the Solution is - PowerShell!
Reinout Segers wrote a fantastic Script how to create easy an SSL Certificate Request by PowerShell, I edited it a bit and I Post it here on my Blog.
Have fun with it...

---

Script has been adjusted to allow commas within variables to be passed through into 'settings.inf' without error.

The script in its original form provides an invalid CSR with all information appended into the 'Common Name' field when passed a variable (namely the organization name) with a comma (ie. 'O=Contoso, Inc.').

By changing the delimiter to a semi-colon, the variables get parsed into 'settings.inf' correctly once again, providing a valid CSR to be dispatched to your CA for processing.