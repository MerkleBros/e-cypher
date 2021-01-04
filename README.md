### e-cypher
[Live example at cozy.computer/e-cypher](https://cozy.computer/e-cypher)

Take a paragraph of English letters and convert it to `e-cypher`; take a paragraph of `e-cypher` and convert it to English.

In `e-cypher`, each letter is lowercased and replaced by a string of repeating `e` characters, where `a = 1 (a -> e), b = 2 (b -> ee), c = 3 (c -> eee)...`. Additionally, capital e (`E`) is used to denote character breaks. Other characters are preserved.

Example of converting an English phrase to `e-cypher`:

```
"Green eggs and ham" ->

eeeeeeeEeeeeeeeeeeeeeeeeeeEeeeeeEeeeeeEeeeeeeeeeeeeeeE eeeeeEeeeeeeeEeeeeeeeEeeeeeeeeeeeeeeeeeeeE eEeeeeeeeeeeeeeeEeeeeE eeeeeeeeEeEeeeeeeeeeeeeeE
```

### Repeating letter cyphers with ecypher.js
You can make a repeating-letter cypher with other letters besides `e` and with other alphabets besides English using `ecypher.js`.

```
import * as ecypher from './ecypher.js';

const aCypher = ecypher.buildCypher("abcdefghijklmnopqrstuvwxyz", "a");

console.log(ecypher.encypher("hello", aCypher));
// Outputs: aaaaaaaaAaaaaaAaaaaaaaaaaaaAaaaaaaaaaaaaAaaaaaaaaaaaaaaaA

console.log(ecypher.decypher(
  "aaaaaaaaAaaaaaAaaaaaaaaaaaaAaaaaaaaaaaaaAaaaaaaaaaaaaaaaA",
  aCypher
));
// Outputs: hello
```
