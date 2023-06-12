# Cross Site Scripting on default complement

# Overview of the Vulnerability
This vulnerability makes it possible to inject content into zip code forms, where it is possible to perform the execution in a reflected way.
As a default component of Ecommerce, it has a field where it performs address queries, but when sanitizing the input there is a loophole where it is possible to bypass the security control through "-" symbols.
<br>
Example payload:
```javascript
<s-v-g o-n-l-o-a-d=a-l-e-r-t-('r00t1ng')>
```
<br>
# Step to reproduce:
- On url, change a fields /carrinho/endereco/adicionar?cep={INJECT_HERE}
<br> 
<br> 
# Proof of Concept
<img src="https://i.imgur.com/O1Gq62d.png">
<br>
<br>
# Google Hacking:

inurl: carrinho/endereco/adicionar?cep= <br>
inurl: endereco/adicionar?cep=
