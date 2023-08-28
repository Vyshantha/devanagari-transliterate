# NPM Package : devanagari-transliterate
The package transliteration texts from Devanagari देवनागरी (devanāgarī) script to Latin script based on [ISO 15919](https://en.wikipedia.org/wiki/ISO_15919). Additionally the application transliterate texts from Latin script based on [IAST](https://en.wikipedia.org/wiki/International_Alphabet_of_Sanskrit_Transliteration), or [Harvard-Kyoto](https://en.wikipedia.org/wiki/Harvard-Kyoto), or [SLP-1](https://en.wikipedia.org/wiki/SLP1) or [ISO 15919](https://en.wikipedia.org/wiki/ISO_15919) to Devanagari देवनागरी (devanāgarī) script. To experiment functionality of this package use the [Devanagari Transliterator App](https://vyshantha.github.io/devanagaritransliterate/) website on you browser.

## Install [Node](https://nodejs.org/en/download), [NPM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) and then install this package
```npm install devanagari-transliterate```

## Usage
### Import the "devanagari-transliterate" package

```
const sanskrittransliterate = require("devanagari-transliterate");
```

### Method call in code 
```sanskrittransliterate(type, direction, input)```
> type
>> 'SLP' \
>> 'HK' \
>> 'IAST' \
>> 'ISO'

> direction
>> 'latin2devanagari' \
>> 'latin2ISO' \
>> 'devanagari2latin'

> input
>> text in SLP-1 for devanāgarī \
>> text in Harvard-Kyoto for devanāgarī \
>> text in IAST for devanāgarī \
>> text in ISO-15919 for devanāgarī \
>> text in देवनागरी

### SLP-1 transliteration examples :

```
console.log('SLP >> देवनागरी : ', sanskrittransliterate("SLP","latin2devanagari","saMskfta"));  
    // Expected SLP >> देवनागरी : संस्कृत
console.log('SLP >> देवनागरी : ', sanskrittransliterate("SLP","latin2devanagari","manu1\\^ maˆjnâ ja\\h na/m vâhthāˆ ma\\nu prasthaH jaV maZ"));
    // Expected SLP >> देवनागरी : मनु१॒॑  म॑ज्न॑  ज॒ह्  न꣫म्  व॑ह्था॑  म॒नु  प्रस्थः  जᳶ  मᳵ
console.log('SLP >> ISO : ', sanskrittransliterate("SLP","latin2ISO","saMskfta"));
    // Expected SLP >> ISO :  saṁskr̥ta
console.log('SLP >> ISO : ', sanskrittransliterate("SLP","latin2ISO","manu1\\^ maˆjnâ ja\\h na/m vâhthāˆ ma\\nu prasthaH jaV maZ")); 
    // Expected SLP >> ISO : manu1̱̍ ma̍jna̍ ja̱h na꣫m va̍hthā̍ ma̱nu prasthaḥ jaᳶ maᳵ
```

### Harvard-Kyoto transliteration examples :

```
console.log('H-K >> देवनागरी : ', sanskrittransliterate("HK","latin2devanagari","saMskRta"));
    // Expected H-K >> देवनागरी : संस्कृत
onsole.log('H-K >> देवनागरी : ', sanskrittransliterate("HK","latin2devanagari","anuklRp klRRmanyaplRRn")); 
    // Expected H-K >> देवनागरी : अनुकॢप् अनुकलृप्  कॣमंयपॣन् कलॄमंयपलॄन्
console.log('H-K >> ISO : ', sanskrittransliterate("HK","latin2ISO","saMskRta")); 
    // Expected H-K >> ISO :  saṁskr̥ta
console.log('H-K >> ISO : ', sanskrittransliterate("HK","latin2ISO","anuklRp klRRmanyaplRRn")); 
    // Expected H-K >> ISO : anukl̥p kl̥̄manyapl̥̄n
```

### IAST transliteration examples :

```
console.log('IAST >> देवनागरी : ', sanskrittransliterate("IAST","latin2devanagari","saṃskṛta"));   
    // Expected IAST >> देवनागरी : संस्कृत
console.log('IAST >> ISO : ', sanskrittransliterate("IAST","latin2ISO","saṃskṛta")); 
    // Expected IAST >> ISO :  saṁskr̥ta
```

### ISO transliteration examples :

```
console.log('ISO >> देवनागरी : ', sanskrittransliterate("ISO","latin2devanagari","samskr̥ta")); 
    // Expected ISO >> देवनागरी : संस्कृत
console.log('देवनागरी >> ISO : ', sanskrittransliterate("ISO","latin2devanagari","maˆjnâ jàh nám vâhthāˆ ma̲nu")); 
    // Expected देवनागरी >> म॑ज्न॑  ज॒ह्  न꣫म्  व॑ह्था॑  म॒नु
```

### देवनागरी transliteration examples :

```
console.log('देवनागरी >> ISO : ', sanskrittransliterate("ISO","devanagari2latin","संस्कृता")); 
    // Expected देवनागरी >> ISO with strict nasalisation :  samskr̥tā
```

## Execution 
Given the above JavaScript code is included into a script.js file : ```node script.js```

## License
Distributed under the MIT License. See LICENSE for more information.

## Contact Author
[Github](https://github.com/Vyshantha)

## Report Issues
[Code](https://github.com/Vyshantha/devanagari-transliterate)
