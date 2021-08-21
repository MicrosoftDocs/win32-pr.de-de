---
title: MOF-Zeichenfolgen
description: Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die normalerweise als für Menschen lesbarer Text vorgesehen ist.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf1b79d6f9de8cca5589efca879c68bb3de68882c6cd6759d076421c5c543c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992280"
---
# <a name="mof-strings"></a>MOF-Zeichenfolgen

Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die normalerweise als für Menschen lesbarer Text vorgesehen ist. MOF beschreibt zwei Typen von Zeichenfolgen, die verwenden, um einzelne oder mehrere Zeichen zu enthalten. MOF verfügt auch über eine Reihe von Regeln, die die Verwendung von Anführungszeichen innerhalb einer Zeichenfolge beschreiben.

In der folgenden Tabelle sind die Zeichenfolgendatentypen für MOF aufgeführt.



| Datentyp  | Automatisierungstyp | Beschreibung                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **VT \_ I2**      | Einzelnes 16-Bit-Unicode-Zeichen im UCS-2-Format (Universal Character Set 2)<br/> |
| **string** | **VT \_ BSTR**    | Unicode-Zeichenfolge<br/>                                                    |



 

Befolgen Sie beim Schreiben von Zeichenfolgen für MOF die folgenden Richtlinien:

-   Umschließt Einzelzeichenkonstanten mit einfachen Anführungszeichen.

    Wenn Sie keine einfachen Anführungszeichen mit Einzelzeichenkonstanten verwenden, müssen Sie die ganzzahlige Darstellung des Unicode-Zeichenwerts verwenden. Optional können Sie das Zeichen wie gezeigt mit der \\ x-Escapesequenz aus dem C-Standard American National Standards Institute (ANSI) angeben:

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Da MOF auf Unicode basiert, können Sie auch 16-Bit-Werte angeben.

    Beachten Sie, dass Einzelzeichenkonstanten im ANSI C-Format von doppelten Anführungszeichen umgeben sind.

-   Umschließt Zeichenfolgen mit doppelten Anführungszeichen.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Verketten aufeinander folgender Anführungszeichenfolgen mit einem oder mehreren Leerzeichen.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Verwenden Sie eine Escapesequenz, die mit einem umgekehrten Schrägstrich beginnt, um Anführungszeichen in eine Zeichenfolge einzubetten.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

Im folgenden Beispiel wird beschrieben, wie Zeichenfolgeneigenschaften und ein Zeichenfolgenparameter initialisiert werden:

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




