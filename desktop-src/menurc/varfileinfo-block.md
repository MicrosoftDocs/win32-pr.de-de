---
title: Varfileingefo-Block Anweisung
description: Beschreibt die Form des Variablen Informations Blocks.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menüs der varfilanfo-Block Anweisung und weitere Ressourcen
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038136"
---
# <a name="varfileinfo-block-statement"></a>Varfileingefo-Block Anweisung

Definiert einen Variablen Informationsblock.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Einer der sprach Bezeichner, der im Abschnitt "Hinweise" angegeben ist.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charder TID*
</dt> <dd>

Einer der Zeichensatz Bezeichner, der im Abschnitt "Hinweise" angegeben ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es können mehr als ein Bezeichnerpaar angegeben werden, aber jedes Paar muss durch ein Komma vom vorangehenden paar getrennt werden.

Der *LangID* -Parameter gibt einen der folgenden Sprachcodes an.



| Code   | Sprache            | Code   | Sprache                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabisch              | 0x0415 | Polnisch                    |
| 0x0402 | Bulgarisch           | 0x0416 | Portugiesisch (Brasilien)       |
| 0x0403 | Katalanisch             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinesisch (traditionell) | 0x0418 | Rumänisch                  |
| 0x0405 | Tschechisch               | 0x0419 | Russisch                   |
| 0x0406 | Dänisch              | 0x041a | Croato-Serbian (lateinisch)    |
| 0x0407 | Deutsch              | 0x041b | Slowakisch                    |
| 0x0408 | Griechisch               | 0x041c | Albanisch                  |
| 0x0409 | US-Englisch        | 0x041d | Schwedisch                   |
| 0x040A | Castilisch Spanisch   | 0x041E | Thailändisch                      |
| 0x040b | Finnisch             | 0x041f | Türkisch                   |
| 0x040c | Französisch              | 0x0420 | Urdu                      |
| 0x040d | Hebräisch              | 0x0421 | Bahasa                    |
| 0x040e | Ungarisch           | 0x0804 | Chinesisch (vereinfacht)        |
| 0x040f | Isländisch           | 0x0807 | Deutsch (Schweiz)              |
| 0x0410 | Italienisch             | 0x0809 | Vereinigtes Königreich: Englisch              |
| 0x0411 | Japanisch            | 0x080a | Spanisch (Mexiko)          |
| 0x0412 | Koreanisch              | 0x080c | Französisch (Belgien)            |
| 0x0413 | Niederländisch               | 0x0c0c | Französisch (Kanada)           |
| 0x0414 | Norwegisch – Bokmal  | 0x100c | Schweiz Französisch              |
| 0x0810 | Schweizer Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Belgisch Niederländisch       | 0x081a | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch – Nynorsk | ?      | ?                         |



 

Der *charsetid* -Parameter gibt einen der folgenden Zeichensatz Bezeichner an:



| Bezeichner | Zeichensatz              |
|------------|----------------------------|
| 0          | 7-Bit-ASCII                |
| 932        | Japan (Shift – JIS X-0208) |
| 949        | Korea (Shift – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Lateinisch-2 (Osteuropäisch) |
| 1251       | Kyrillisch                   |
| 1252       | Mehrsprachige               |
| 1253       | Griechisch                      |
| 1254       | Türkisch                    |
| 1255       | Hebräisch                     |
| 1256       | Arabisch                     |



 

 

 




