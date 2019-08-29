# Svör við spurningum á verkefni 1:

### 1. Hvað er nullog undefined?
null og undefined er það sama (nema ekki sama gagnatýpan) sem þýðir að gildi (á t.d breytu) sé óskilgreind (ekkert)

### 2. Hvað gerir 'use strict' í JavaScript kóða?
Hreinsar út gamla galla í javascript

### 3. Hver er munurinn á let,varog const?
var er gamla leiðin til að skilgreina breytur, áður en let og const kom þá voru breytur alltaf global nema ef þær voru inn í falli, en fyrir utan að þú gerðir fall gerðu slaufusvigar ekki neitt til að block'a breytur fyrir utan slaufusvigana, let er til að laga það og const er eins og let nema þú getur ekki breytt const

### 4. Endurskrifaðu eftirfarandi kóða með for lykkjunni.
#### Kóðinn fyrir neðan

// =====================================

for(let x = 9; x >= 1; x--){
	console.log("hello " + x);
}

// =====================================

### 5. Skilgreindusama falliðá þrjá mismunandi vegu.
#### Kóðarnir fyrir neðan

// =====================================

// leið 1
function fall(){}

// leið 2
let fall = function(){}

// leið 3
// (function(){})(); // keyrir sjálfkrafa

// =====================================

### 6. Útskýrðu hvað eftirfarandi kóði gerir, hvað gera svigarnir?
Þetta prentar út 'Hello World', fallið er inn í sviganum og svigarnir í endanum keyra láta fallið keyrast sjálfkrafa

### 7. Af hverju birtist 1 en ekki 10?
Fallið b, það býr til fallið "a", en það er inn í fallinu "b", en það er þegar til breytan "a", svo javascript býr til pláss
fyrir *fallið* "a" (í fallinu "b"), svo kemur "return" og þá á fallið að hætta að keyra, en ef við tökum út "return" þá ættirðu
ennþá að fá 1, það er vegna þess að þú ert bara að breyta *fallinu* "a" í breytu, og þá er "a" í "b" bara local breyta, vegna
þess að *fallið* "a" var local inn í fallinu "b". En *fallið* "a" er neðst í kóðanum, en javascript endurraðar alltaf kóðanum
þannig að þegar þú keyrir fallið "b" þá er skilgreiningin á *fallinu* "a" sett efst á fallið "b"


### 8. Leystu lið 20 í Lesson 6 (Arrays)á Udacity https://classroom.udacity.com/courses/ud803
#### Kóðinn fyrir neðan

// =====================================

let words = ["cat", "in", "hat"];
words.forEach(function(word, num, all) {
  console.log(all.toString());
});

// =====================================

### 9. Leystu lið 22 í Lesson 6 (Arrays)á Udacity https://classroom.udacity.com/courses/ud803
#### Kóðinn fyrir neðan

// =====================================

let bills = [50.23, 19.12, 34.01,
    100.11, 12.15, 9.90, 29.11, 12.99,
    10.00, 99.22, 102.20, 100.10, 6.77, 2.22
];

let totals = bills.map(function(bill){
    return Number.parseFloat((bill * 1.15).toFixed(2));
});

console.log(totals);

// =====================================

### 10. Skrifaðu forrití JavaScript sem sprengir staflan (stack overflow).
#### Kóðinn fyrir neðan

// =====================================

function boom(){
	boom();
}
boom();

// =====================================
