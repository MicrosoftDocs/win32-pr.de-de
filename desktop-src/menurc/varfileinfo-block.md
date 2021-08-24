---
title: VarFileInfo BLOCK-Anweisung
description: Beschreibt die Form des Variableninformationsblocks.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- VarFileInfo BLOCK-Anweisungsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846970"
---
# <a name="varfileinfo-block-statement"></a>VarFileInfo BLOCK-Anweisung

Definiert einen Variableninformationsblock.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

Einer der im Abschnitt "Hinweise" angegebenen Sprachbezeichner.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Einer der im Abschnitt "Hinweise" angegebenen Zeichensatzbezeichner.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es können mehrere Bezeichnerpaare angegeben werden, aber jedes Paar muss durch ein Komma vom vorherigen Paar getrennt werden.

Der *langID-Parameter* gibt einen der folgenden Sprachcodes an.



| Code   | Sprache            | Code   | Sprache                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabisch              | 0x0415 | Polnisch                    |
| 0x0402 | Bulgarisch           | 0x0416 | Portugiesisch (Brasilien)       |
| 0x0403 | Katalanisch             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinesisch (traditionell) | 0x0418 | Rumänisch                  |
| 0x0405 | Tschechisch               | 0x0419 | Russisch                   |
| 0x0406 | Dänisch              | 0x041A | Croato-Serbian (Lateinisch)    |
| 0x0407 | Deutsch              | 0x041B | Slowakisch                    |
| 0x0408 | Griechisch               | 0x041C | Albanisch                  |
| 0x0409 | Englisch (USA)        | 0x041D | Schwedisch                   |
| 0x040A | Castilienisch (Spanisch)   | 0x041E | Thailändisch                      |
| 0x040B | Finnisch             | 0x041F | Türkisch                   |
| 0x040C | Französisch              | 0x0420 | Urdu                      |
| 0x040D | Hebräisch              | 0x0421 | Bahasa                    |
| 0x040E | Ungarisch           | 0x0804 | Chinesisch (vereinfacht)        |
| 0x040F | Isländisch           | 0x0807 | Deutsch (Deutsch)              |
| 0x0410 | Italienisch             | 0x0809 | Vereinigtes Königreich: Englisch              |
| 0x0411 | Japanisch            | 0x080A | Spanisch (Mexiko)          |
| 0x0412 | Koreanisch              | 0x080C | Französisch (Französisch)            |
| 0x0413 | Niederländisch               | 0x0C0C | Französisch (Kanada)           |
| 0x0414 | Norwegisch – Bokmal  | 0x100C | Französisch (Französisch)              |
| 0x0810 | Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Niederländisch (Niederländisch)       | 0x081A | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch – Nynorsk | ?      | ?                         |



 

Der *charsetID-Parameter* gibt einen der folgenden Zeichensatzbezeichner an:



| Bezeichner | Zeichensatz              |
|------------|----------------------------|
| 0          | 7-Bit-ASCII                |
| 932        | Japan (Shift – JIS X-0208) |
| 949        | Korea (Umschalten – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Osteerisch) |
| 1251       | Kyrillisch                   |
| 1252       | Mehrsprachige               |
| 1253       | Griechisch                      |
| 1254       | Türkisch                    |
| 1255       | Hebräisch                     |
| 1256       | Arabisch                     |



 

 

 




