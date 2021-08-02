## Description
Mycroft TTS plugin for [ResponsiveVoice](https://responsivevoice.org/)

## Install

`pip install ovos-tts-plugin-responsivevoice`

## Configuration

There are 2 possible ways to configure this plugin, the prefered way is to explicitly select a voice, see a list bellow

NOTE: some voices might ignore pitch / rate / volume

```json
  "tts": {
    "module": "ovos-tts-plugin-responsivevoice",
    "ovos-tts-plugin-responsivevoice": {
      "voice": "UKEnglishMale",
      "pitch": 0.5,
      "rate": 0.5,
      "vol": 1
    }
 }
```

Alternatively you can request a language and a gender, i have noticed funny behaviour like gender switching depending on utterance, i believe this is due to some weird caching on resposonsive voice servers

If a voice is set lang and gender will be ignored

```json
  "tts": {
    "module": "ovos-tts-plugin-responsivevoice",
    "ovos-tts-plugin-responsivevoice": {
      "lang": "en-us",
      "gender": "male",
      "pitch": 0.5,
      "rate": 0.5,
      "vol": 1
    }
  }
```
### Voice list

Notes: 
- this list was [automatically scrapped](https://github.com/HelloChatterbox/py_responsivevoice/tree/master/data) for previous versions of 
responsive voice and is outdated, [some voices behave funny](https://github.com/HelloChatterbox/py_responsivevoice/issues/8)
- There are LOTS of duplicate voices with different names, some seem to have 
been deprecated and fallback to a different engine
- All Microsoft voices seem to be deprecated and fallback to english female
- Some of these will simply use espeak, don"t be fooled by the size of this list

```json
{"af": ["AfrikaansMale", "FallbackAfrikans"],
 "af-za": ["AfrikaansMale"],
 "ar": ["ArabicMale",
        "ArabicFemale",
        "FallbackArabic",
        "Maged",
        "FallbackArabicMale"],
 "ar-sa": ["ArabicMale", "ArabicFemale", "Maged"],
 "bs": ["BosnianMale", "FallbackBosnianMale"],
 "ca": ["CatalanMale", "FallbackCatalan"],
 "ca-es": ["CatalanMale"],
 "cs": ["CzechFemale", "CzechMale", "FallbackCzech", "CzechMale2", "Zuzana"],
 "cs-cz": ["CzechFemale", "CzechMale", "Zuzana"],
 "cy": ["WelshMale", "FallbackWelsh"],
 "da": ["DanishFemale", "DanishMale", "FallbackDanish", "DanishMale2", "Sara"],
 "da-dk": ["DanishFemale", "DanishMale", "Sara"],
 "de": ["DeutschFemale",
        "DeutschMale",
        "FallbackDeutschFemale",
        "GermanGermany",
        "Anna",
        "MicrosoftHeddaMobileGermanGermany",
        "MicrosoftKatjaMobileGermanGermany",
        "Helena",
        "MicrosoftHeddaGermanGermany",
        "MicrosoftKatjaGermanGermany",
        "MicrosoftStefanGermanGermany",
        "MicrosoftStefanMobileGermanGermany",
        "MicrosoftHeddaDesktopGermanGermany",
        "MicrosoftKatjaDesktopGermanGermany",
        "MicrosoftStefanDesktopGermanGermany",
        "Martin",
        "FallbackDeutschMale"],
 "de-de": ["DeutschFemale",
           "DeutschMale",
           "GermanGermany",
           "Anna",
           "MicrosoftHeddaMobileGermanGermany",
           "MicrosoftKatjaMobileGermanGermany",
           "Helena",
           "MicrosoftHeddaGermanGermany",
           "MicrosoftKatjaGermanGermany",
           "MicrosoftStefanGermanGermany",
           "MicrosoftStefanMobileGermanGermany",
           "MicrosoftHeddaDesktopGermanGermany",
           "MicrosoftKatjaDesktopGermanGermany",
           "MicrosoftStefanDesktopGermanGermany",
           "Martin"],
 "el": ["GreekFemale", "GreekMale", "FallbackGreek", "GreekMale2", "Melina"],
 "el-gr": ["GreekFemale", "GreekMale", "Melina"],
 "en": ["UKEnglishFemale",
        "UKEnglishMale",
        "USEnglishFemale",
        "USEnglishMale",
        "AustralianFemale",
        "AustralianMale",
        "FallbackUKFemale",
        "FallbackenGBFemale",
        "FallbackUSEnglish",
        "FallbackAustralianFemale",
        "FallbackUKEnglishMale",
        "FallbackUSEnglishMale",
        "EnglishUnitedKingdom",
        "EnglishIndia",
        "EnglishUnitedStates",
        "Karen",
        "Daniel",
        "Moira",
        "SamanthaEnhanced",
        "Samantha",
        "Tessa",
        "MicrosoftDavidMobileEnglishUnitedStates",
        "MicrosoftZiraMobileEnglishUnitedStates",
        "MicrosoftMarkMobileEnglishUnitedStates",
        "MicrosoftGeorgeMobileEnglishUnitedKingdom",
        "MicrosoftSusanMobileEnglishUnitedKingdom",
        "MicrosoftHazelMobileEnglishUnitedKingdom",
        "MicrosoftHeeraMobileEnglishIndia",
        "Catherine",
        "Arthur",
        "Martha",
        "MicrosoftDavidEnglishUnitedStates",
        "MicrosoftZiraEnglishUnitedStates",
        "MicrosoftMarkEnglishUnitedStates",
        "MicrosoftGeorgeEnglishUnitedKingdom",
        "MicrosoftSusanEnglishUnitedKingdom",
        "MicrosoftHazelEnglishUnitedKingdom",
        "MicrosoftHeeraEnglishIndia",
        "MicrosoftRaviEnglishIndia",
        "MicrosoftRaviMobileEnglishIndia",
        "MicrosoftDavidDesktopEnglishUnitedStates",
        "MicrosoftZiraDesktopEnglishUnitedStates",
        "MicrosoftMarkDesktopEnglishUnitedStates",
        "MicrosoftGeorgeDesktopEnglishUnitedKingdom",
        "MicrosoftSusanDesktopEnglishUnitedKingdom",
        "MicrosoftHazelDesktopEnglishUnitedKingdom",
        "MicrosoftHeeraDesktopEnglishIndia",
        "MicrosoftRaviDesktopEnglishIndia",
        "Gordon",
        "Aaron",
        "Nicky",
        "FallbackAustralianMale",
        "MicrosoftAnnaEnglishUnitedStates"],
 "en-au": ["AustralianFemale",
           "AustralianMale",
           "FallbackAustralianFemale",
           "Karen",
           "Catherine",
           "Gordon",
           "FallbackAustralianMale"],
 "en-gb": ["UKEnglishFemale",
           "UKEnglishMale",
           "FallbackUKFemale",
           "FallbackenGBFemale",
           "FallbackUKEnglishMale",
           "EnglishUnitedKingdom",
           "Daniel",
           "MicrosoftGeorgeMobileEnglishUnitedKingdom",
           "MicrosoftSusanMobileEnglishUnitedKingdom",
           "MicrosoftHazelMobileEnglishUnitedKingdom",
           "Arthur",
           "Martha",
           "MicrosoftGeorgeEnglishUnitedKingdom",
           "MicrosoftSusanEnglishUnitedKingdom",
           "MicrosoftHazelEnglishUnitedKingdom",
           "MicrosoftGeorgeDesktopEnglishUnitedKingdom",
           "MicrosoftSusanDesktopEnglishUnitedKingdom",
           "MicrosoftHazelDesktopEnglishUnitedKingdom"],
 "en-ie": ["Moira"],
 "en-in": ["EnglishIndia",
           "MicrosoftHeeraMobileEnglishIndia",
           "MicrosoftHeeraEnglishIndia",
           "MicrosoftRaviEnglishIndia",
           "MicrosoftRaviMobileEnglishIndia",
           "MicrosoftHeeraDesktopEnglishIndia",
           "MicrosoftRaviDesktopEnglishIndia"],
 "en-us": ["USEnglishFemale",
           "USEnglishMale",
           "FallbackUSEnglish",
           "FallbackUSEnglishMale",
           "EnglishUnitedStates",
           "SamanthaEnhanced",
           "Samantha",
           "MicrosoftDavidMobileEnglishUnitedStates",
           "MicrosoftZiraMobileEnglishUnitedStates",
           "MicrosoftMarkMobileEnglishUnitedStates",
           "MicrosoftDavidEnglishUnitedStates",
           "MicrosoftZiraEnglishUnitedStates",
           "MicrosoftMarkEnglishUnitedStates",
           "MicrosoftDavidDesktopEnglishUnitedStates",
           "MicrosoftZiraDesktopEnglishUnitedStates",
           "MicrosoftMarkDesktopEnglishUnitedStates",
           "Aaron",
           "Nicky",
           "MicrosoftAnnaEnglishUnitedStates"],
 "en-za": ["Tessa"],
 "eo": ["EsperantoMale", "FallbackEsperanto"],
 "es": ["SpanishFemale",
        "SpanishMale",
        "SpanishLatinAmericanFemale",
        "SpanishLatinAmericanMale",
        "CatalanMale",
        "FallbackSpanishFemale",
        "FallbackSpanishLatinAmericanFemale",
        "SpanishSpain",
        "SpanishMexico",
        "SpanishUnitedStates",
        "Monica",
        "Paulina",
        "MicrosoftHelenaMobileSpanishSpain",
        "MicrosoftLauraMobileSpanishSpain",
        "MicrosoftSabinaMobileSpanishMexico",
        "MicrosoftHelenaSpanishSpain",
        "MicrosoftLauraSpanishSpain",
        "MicrosoftSabinaSpanishMexico",
        "MicrosoftPabloSpanishSpain",
        "MicrosoftRaulSpanishMexico",
        "MicrosoftPabloMobileSpanishSpain",
        "MicrosoftRaulMobileSpanishMexico",
        "MicrosoftHelenaDesktopSpanishSpain",
        "MicrosoftLauraDesktopSpanishSpain",
        "MicrosoftSabinaDesktopSpanishMexico",
        "MicrosoftPabloDesktopSpanishSpain",
        "MicrosoftRaulDesktopSpanishMexico",
        "FallbackSpanishMale",
        "FallbackSpanishLatinAmericanMale"],
 "es-419": ["FallbackSpanishLatinAmericanFemale",
            "FallbackSpanishLatinAmericanMale"],
 "es-ca": ["CatalanMale"],
 "es-es": ["SpanishFemale",
           "SpanishMale",
           "SpanishSpain",
           "Monica",
           "MicrosoftHelenaMobileSpanishSpain",
           "MicrosoftLauraMobileSpanishSpain",
           "MicrosoftHelenaSpanishSpain",
           "MicrosoftLauraSpanishSpain",
           "MicrosoftPabloSpanishSpain",
           "MicrosoftPabloMobileSpanishSpain",
           "MicrosoftHelenaDesktopSpanishSpain",
           "MicrosoftLauraDesktopSpanishSpain",
           "MicrosoftPabloDesktopSpanishSpain"],
 "es-mx": ["SpanishLatinAmericanFemale",
           "SpanishLatinAmericanMale",
           "SpanishMexico",
           "Paulina",
           "MicrosoftSabinaMobileSpanishMexico",
           "MicrosoftSabinaSpanishMexico",
           "MicrosoftRaulSpanishMexico",
           "MicrosoftRaulMobileSpanishMexico",
           "MicrosoftSabinaDesktopSpanishMexico",
           "MicrosoftRaulDesktopSpanishMexico"],
 "es-us": ["SpanishUnitedStates"],
 "fi": ["FinnishFemale",
        "FinnishMale",
        "FallbackFinnish",
        "FinnishMale2",
        "Satu"],
 "fi-fi": ["FinnishFemale", "FinnishMale", "Satu"],
 "fr": ["FrenchFemale",
        "FrenchMale",
        "FallbackFrenchFemale",
        "FrenchBelgium",
        "FrenchFrance",
        "Amelie",
        "Thomas",
        "MicrosoftJulieMobileFrenchFrance",
        "Marie",
        "MicrosoftJulieFrenchFrance",
        "MicrosoftHortenseFrenchFrance",
        "MicrosoftPaulFrenchFrance",
        "MicrosoftHortenseMobileFrenchFrance",
        "MicrosoftPaulMobileFrenchFrance",
        "MicrosoftJulieDesktopFrenchFrance",
        "MicrosoftHortenseDesktopFrenchFrance",
        "MicrosoftPaulDesktopFrenchFrance",
        "FrenchDaniel",
        "FallbackFrenchMale"],
 "fr-be": ["FrenchBelgium"],
 "fr-ca": ["Amelie"],
 "fr-fr": ["FrenchFemale",
           "FrenchMale",
           "FrenchFrance",
           "Thomas",
           "MicrosoftJulieMobileFrenchFrance",
           "Marie",
           "MicrosoftJulieFrenchFrance",
           "MicrosoftHortenseFrenchFrance",
           "MicrosoftPaulFrenchFrance",
           "MicrosoftHortenseMobileFrenchFrance",
           "MicrosoftPaulMobileFrenchFrance",
           "MicrosoftJulieDesktopFrenchFrance",
           "MicrosoftHortenseDesktopFrenchFrance",
           "MicrosoftPaulDesktopFrenchFrance",
           "FrenchDaniel"],
 "he": ["Carmit"],
 "he-il": ["Carmit"],
 "hi": ["HindiFemale",
        "HindiMale",
        "TamilMale",
        "FallbackHindiFemale",
        "HindiIndia",
        "Lekha",
        "FallbackHindiMale"],
 "hi-in": ["HindiFemale", "HindiMale", "TamilMale", "HindiIndia", "Lekha"],
 "hr": ["CroatianMale", "SerboCroatianMale", "FallbackCroatianMale"],
 "hr-hr": ["CroatianMale", "SerboCroatianMale"],
 "ht": ["FallbackHaitianCreole"],
 "hu": ["HungarianFemale",
        "HungarianMale",
        "FallbackHungarianFemale",
        "HungarianMale2",
        "Mariska"],
 "hu-hu": ["HungarianFemale", "HungarianMale", "Mariska"],
 "hy": ["ArmenianMale", "FallbackArmenian"],
 "hy-am": ["ArmenianMale"],
 "id": ["IndonesianFemale",
        "IndonesianMale",
        "FallbackIndonesianFemale",
        "Damayanti",
        "FallbackIndonesianMale"],
 "id-id": ["IndonesianFemale", "IndonesianMale", "Damayanti"],
 "in": ["IndonesianIndonesia"],
 "in-id": ["IndonesianIndonesia"],
 "is": ["IcelandicMale", "FallbackIcelandic"],
 "is-is": ["IcelandicMale"],
 "it": ["ItalianFemale",
        "ItalianMale",
        "FallbackItalianFemale",
        "ItalianItaly",
        "Alice",
        "MicrosoftElsaMobileItalianItaly",
        "MicrosoftElsaItalianItaly",
        "MicrosoftCosimoItalianItaly",
        "MicrosoftCosimoMobileItalianItaly",
        "MicrosoftElsaDesktopItalianItaly",
        "MicrosoftCosimoDesktopItalianItaly",
        "FallbackItalianMale"],
 "it-it": ["ItalianFemale",
           "ItalianMale",
           "ItalianItaly",
           "Alice",
           "MicrosoftElsaMobileItalianItaly",
           "MicrosoftElsaItalianItaly",
           "MicrosoftCosimoItalianItaly",
           "MicrosoftCosimoMobileItalianItaly",
           "MicrosoftElsaDesktopItalianItaly",
           "MicrosoftCosimoDesktopItalianItaly"],
 "ja": ["JapaneseFemale",
        "JapaneseMale",
        "FallbackJapaneseFemale",
        "JapaneseJapan",
        "Kyoko",
        "MicrosoftAyumiMobileJapaneseJapan",
        "MicrosoftHarukaMobileJapaneseJapan",
        "Oren",
        "MicrosoftAyumiJapaneseJapan",
        "MicrosoftHarukaJapaneseJapan",
        "MicrosoftIchiroJapaneseJapan",
        "MicrosoftIchiroMobileJapaneseJapan",
        "MicrosoftAyumiDesktopJapaneseJapan",
        "MicrosoftHarukaDesktopJapaneseJapan",
        "MicrosoftIchiroDesktopJapaneseJapan",
        "Hattori",
        "FallbackJapaneseMale"],
 "ja-jp": ["JapaneseFemale",
           "JapaneseMale",
           "JapaneseJapan",
           "Kyoko",
           "MicrosoftAyumiMobileJapaneseJapan",
           "MicrosoftHarukaMobileJapaneseJapan",
           "Oren",
           "MicrosoftAyumiJapaneseJapan",
           "MicrosoftHarukaJapaneseJapan",
           "MicrosoftIchiroJapaneseJapan",
           "MicrosoftIchiroMobileJapaneseJapan",
           "MicrosoftAyumiDesktopJapaneseJapan",
           "MicrosoftHarukaDesktopJapaneseJapan",
           "MicrosoftIchiroDesktopJapaneseJapan",
           "Hattori"],
 "ko": ["KoreanFemale",
        "KoreanMale",
        "FallbackKoreanFemale",
        "KoreanSouthKorea",
        "Yuna",
        "MicrosoftHeamiKoreanKorean",
        "MicrosoftHeamiMobileKoreanKorean",
        "MicrosoftHeamiDesktopKoreanKorean",
        "MicrosoftHeamiDesktopKorean",
        "FallbackKoreanMale"],
 "ko-kr": ["KoreanFemale",
           "KoreanMale",
           "KoreanSouthKorea",
           "Yuna",
           "MicrosoftHeamiKoreanKorean",
           "MicrosoftHeamiMobileKoreanKorean",
           "MicrosoftHeamiDesktopKoreanKorean",
           "MicrosoftHeamiDesktopKorean"],
 "la": ["LatinFemale", "LatinMale", "FallbackLatinFemale", "LatinMale2"],
 "lv": ["LatvianMale", "FallbackLatvianMale"],
 "lv-lv": ["LatvianMale"],
 "md": ["MoldavianFemale", "MoldavianMale"],
 "me": ["MontenegrinMale"],
 "mk": ["MacedonianMale", "FallbackMacedonianMale"],
 "mk-mk": ["MacedonianMale"],
 "mo": ["FallbackMoldavianFemale"],
 "nb": ["NorwegianFemale", "NorwegianMale"],
 "nb-no": ["NorwegianFemale", "NorwegianMale"],
 "nl": ["DutchFemale",
        "DutchMale",
        "FallbackDutchFemale",
        "DutchNetherlands",
        "Ellen",
        "Xander",
        "FallbackDutchMale"],
 "nl-be": ["Ellen"],
 "nl-nl": ["DutchFemale", "DutchMale", "DutchNetherlands", "Xander"],
 "no": ["FallbackNorwegian", "NorwegianMale2", "Nora"],
 "no-no": ["Nora"],
 "pl": ["PolishFemale",
        "PolishMale",
        "FallbackPolishFemale",
        "PolishPoland",
        "Zosia",
        "MicrosoftPaulinaMobilePolishPoland",
        "MicrosoftPaulinaPolishPoland",
        "MicrosoftAdamPolishPoland",
        "MicrosoftAdamMobilePolishPoland",
        "MicrosoftPaulinaDesktopPolishPoland",
        "MicrosoftAdamDesktopPolishPoland",
        "FallbackPolishMale"],
 "pl-pl": ["PolishFemale",
           "PolishMale",
           "PolishPoland",
           "Zosia",
           "MicrosoftPaulinaMobilePolishPoland",
           "MicrosoftPaulinaPolishPoland",
           "MicrosoftAdamPolishPoland",
           "MicrosoftAdamMobilePolishPoland",
           "MicrosoftPaulinaDesktopPolishPoland",
           "MicrosoftAdamDesktopPolishPoland"],
 "pt": ["BrazilianPortugueseFemale",
        "BrazilianPortugueseMale",
        "PortugueseFemale",
        "PortugueseMale",
        "FallbackBrazilianPortugueseFemale",
        "FallbackPortuguese",
        "PortugueseBrazil",
        "PortuguesePortugal",
        "Luciana",
        "Joana",
        "MicrosoftMariaMobilePortugueseBrazil",
        "MicrosoftMariaPortugueseBrazil",
        "MicrosoftDanielPortugueseBrazil",
        "MicrosoftDanielMobilePortugueseBrazil",
        "MicrosoftMariaDesktopPortugueseBrazil",
        "MicrosoftDanielDesktopPortugueseBrazil",
        "FallbackBrazilianPortugueseMale",
        "FallbackPortugueseMale"],
 "pt-br": ["BrazilianPortugueseFemale",
           "BrazilianPortugueseMale",
           "PortugueseFemale",
           "PortugueseMale",
           "FallbackBrazilianPortugueseFemale",
           "PortugueseBrazil",
           "Luciana",
           "MicrosoftMariaMobilePortugueseBrazil",
           "MicrosoftMariaPortugueseBrazil",
           "MicrosoftDanielPortugueseBrazil",
           "MicrosoftDanielMobilePortugueseBrazil",
           "MicrosoftMariaDesktopPortugueseBrazil",
           "MicrosoftDanielDesktopPortugueseBrazil",
           "FallbackBrazilianPortugueseMale"],
 "pt-pt": ["FallbackPortuguese",
           "PortuguesePortugal",
           "Joana",
           "FallbackPortugueseMale"],
 "ro": ["RomanianFemale", "FallbackRomanian", "Ioana"],
 "ro-ro": ["RomanianFemale", "Ioana"],
 "ru": ["RussianFemale",
        "RussianMale",
        "FallbackRussian",
        "RussianRussia",
        "Milena",
        "MicrosoftIrinaMobileRussianRussia",
        "MicrosoftIrinaRussianRussia",
        "MicrosoftPavelRussianRussia",
        "MicrosoftPavelMobileRussianRussia",
        "MicrosoftIrinaDesktopRussianRussia",
        "MicrosoftPavelDesktopRussianRussia",
        "FallbackRussianMale"],
 "ru-ru": ["RussianFemale",
           "RussianMale",
           "RussianRussia",
           "Milena",
           "MicrosoftIrinaMobileRussianRussia",
           "MicrosoftIrinaRussianRussia",
           "MicrosoftPavelRussianRussia",
           "MicrosoftPavelMobileRussianRussia",
           "MicrosoftIrinaDesktopRussianRussia",
           "MicrosoftPavelDesktopRussianRussia"],
 "sh": ["FallbackSerboCroation"],
 "sk": ["SlovakFemale", "SlovakMale", "FallbackSlovak", "SlovakMale2", "Laura"],
 "sk-sk": ["SlovakFemale", "SlovakMale", "Laura"],
 "sq": ["AlbanianMale", "FallbackAlbanian"],
 "sq-al": ["AlbanianMale"],
 "sr": ["SerbianMale", "FallbackSerbianMale", "FallbackMontenegrinMale"],
 "sr-me": ["FallbackMontenegrinMale"],
 "sr-rs": ["SerbianMale"],
 "sv": ["SwedishFemale",
        "SwedishMale",
        "FallbackSwedish",
        "SwedishMale2",
        "Alva"],
 "sv-se": ["SwedishFemale", "SwedishMale", "Alva"],
 "sw": ["SwahiliMale", "FallbackSwahili"],
 "sw-ke": ["SwahiliMale"],
 "ta": ["FallbackTamil"],
 "th": ["ThaiFemale",
        "ThaiMale",
        "FallbackThaiFemale",
        "ThaiThailand",
        "Kanya",
        "FallbackThaiMale"],
 "th-th": ["ThaiFemale", "ThaiMale", "ThaiThailand", "Kanya"],
 "tr": ["TurkishFemale",
        "TurkishMale",
        "FallbackTurkish",
        "TurkishTurkey",
        "Yelda",
        "FallbackTurkishMale"],
 "tr-tr": ["TurkishFemale", "TurkishMale", "TurkishTurkey", "Yelda"],
 "vi": ["VietnameseFemale",
        "VietnameseMale",
        "FallbackVietnameseMale",
        "FallbackVietnameseFemale"],
 "vi-vn": ["VietnameseFemale", "VietnameseMale"],
 "zh": ["ChineseFemale",
        "ChineseMale",
        "ChineseHongKongFemale",
        "ChineseHongKongMale",
        "ChineseTaiwanFemale",
        "ChineseTaiwanMale",
        "FallbackChinese",
        "ChineseChina",
        "ChineseHongKong",
        "ChineseHongKong2",
        "ChineseTaiwan",
        "TingTing",
        "SinJi",
        "MeiJia",
        "FallbackChineseHongKongFemale",
        "FallbackChineseTaiwanFemale",
        "MicrosoftHuihuiMobileChineseSimplifiedPRC",
        "MicrosoftYaoyaoMobileChineseSimplifiedPRC",
        "MicrosoftTracyMobileChineseTraditionalHongKongSAR",
        "Yushu",
        "MicrosoftHuihuiChineseSimplifiedPRC",
        "MicrosoftYaoyaoChineseSimplifiedPRC",
        "MicrosoftTracyChineseTraditionalHongKongSAR",
        "MicrosoftHanhanChineseTraditionalTaiwan",
        "MicrosoftKangkangChineseSimplifiedPRC",
        "MicrosoftDannyChineseTraditionalHongKongSAR",
        "MicrosoftYatingChineseTraditionalTaiwan",
        "MicrosoftZhiweiChineseTraditionalTaiwan",
        "MicrosoftHanhanMobileChineseTraditionalTaiwan",
        "MicrosoftKangkangMobileChineseSimplifiedPRC",
        "MicrosoftDannyMobileChineseTraditionalHongKongSAR",
        "MicrosoftYatingMobileChineseTraditionalTaiwan",
        "MicrosoftZhiweiMobileChineseTraditionalTaiwan",
        "MicrosoftHuihuiDesktopChineseSimplifiedPRC",
        "MicrosoftYaoyaoDesktopChineseSimplifiedPRC",
        "MicrosoftTracyDesktopChineseTraditionalHongKongSAR",
        "MicrosoftHanhanDesktopChineseTraditionalTaiwan",
        "MicrosoftKangkangDesktopChineseSimplifiedPRC",
        "MicrosoftDannyDesktopChineseTraditionalHongKongSAR",
        "MicrosoftYatingDesktopChineseTraditionalTaiwan",
        "MicrosoftZhiweiDesktopChineseTraditionalTaiwan",
        "LiMu",
        "MicrosoftHanhanDesktopChineseTaiwan",
        "FallbackChinese2",
        "FallbackChineseHK",
        "FallbackChineseTW",
        "MicrosoftLiliChineseChina"],
 "zh-cn": ["ChineseFemale",
           "ChineseMale",
           "FallbackChinese",
           "ChineseChina",
           "TingTing",
           "MicrosoftHuihuiMobileChineseSimplifiedPRC",
           "MicrosoftYaoyaoMobileChineseSimplifiedPRC",
           "MicrosoftTracyMobileChineseTraditionalHongKongSAR",
           "Yushu",
           "MicrosoftHuihuiChineseSimplifiedPRC",
           "MicrosoftYaoyaoChineseSimplifiedPRC",
           "MicrosoftTracyChineseTraditionalHongKongSAR",
           "MicrosoftKangkangChineseSimplifiedPRC",
           "MicrosoftKangkangMobileChineseSimplifiedPRC",
           "MicrosoftHuihuiDesktopChineseSimplifiedPRC",
           "MicrosoftYaoyaoDesktopChineseSimplifiedPRC",
           "MicrosoftTracyDesktopChineseTraditionalHongKongSAR",
           "MicrosoftKangkangDesktopChineseSimplifiedPRC",
           "LiMu",
           "FallbackChinese2",
           "MicrosoftLiliChineseChina"],
 "zh-hk": ["ChineseHongKongFemale",
           "ChineseHongKongMale",
           "ChineseHongKong",
           "ChineseHongKong2",
           "SinJi",
           "FallbackChineseHongKongFemale",
           "MicrosoftDannyChineseTraditionalHongKongSAR",
           "MicrosoftDannyMobileChineseTraditionalHongKongSAR",
           "MicrosoftDannyDesktopChineseTraditionalHongKongSAR",
           "FallbackChineseHK"],
 "zh-tw": ["ChineseTaiwanFemale",
           "ChineseTaiwanMale",
           "ChineseTaiwan",
           "MeiJia",
           "FallbackChineseTaiwanFemale",
           "MicrosoftHanhanChineseTraditionalTaiwan",
           "MicrosoftYatingChineseTraditionalTaiwan",
           "MicrosoftZhiweiChineseTraditionalTaiwan",
           "MicrosoftHanhanMobileChineseTraditionalTaiwan",
           "MicrosoftYatingMobileChineseTraditionalTaiwan",
           "MicrosoftZhiweiMobileChineseTraditionalTaiwan",
           "MicrosoftHanhanDesktopChineseTraditionalTaiwan",
           "MicrosoftYatingDesktopChineseTraditionalTaiwan",
           "MicrosoftZhiweiDesktopChineseTraditionalTaiwan",
           "MicrosoftHanhanDesktopChineseTaiwan",
           "FallbackChineseTW"]}        
```
