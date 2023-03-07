# BreachdirectoryCopySHA1

https://breachdirectory.org/

Simple JavaScript to copy all SHA1 hashes from Breachdirectory

# Hash

```javascript
document.querySelector('option[value="5"]').value = '500000';
const select = document.querySelector('select[name="passwords_length"]');
const option = select.querySelector('option[value="500000"]');
option.selected = true;
select.dispatchEvent(new Event('change'));
var sha1Regex = /\b([a-f0-9]{40})\b/gi;
var domContent = document.documentElement.outerHTML;
var sha1Matches = domContent.match(sha1Regex);
var sha1Hashes = sha1Matches.join("\n");
copy(sha1Hashes);
```

# Hash:Password

```javascript
document.querySelector('option[value="5"]').value = '500000';
const select = document.querySelector('select[name="passwords_length"]');
const option = select.querySelector('option[value="500000"]');
option.selected = true;
select.dispatchEvent(new Event('change'));


const htmlContent = document.documentElement.outerHTML;
const regex = /<td[^>]*>([^<]*)<\/td>\s*<td[^>]*>([^<]*)<\/td>/g;

let match;
let passwordList = '';
while (match = regex.exec(htmlContent)) {
  const password = match[1].trim();
  const hash = match[2].trim();
  passwordList += `${hash}:${password}\n`;
}

copy(passwordList)

```

SHA1 -> https://hashes.com/en/decrypt/hash

