---
title: MOF-Zeichen folgen
description: Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die in der Regel als lesbarer Text gedacht ist.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863795"
---
# <a name="mof-strings"></a>MOF-Zeichen folgen

Eine Zeichenfolge ist ein Datentyp, der eine Zeichenfolge enthält, die in der Regel als lesbarer Text gedacht ist. MOF beschreibt zwei Arten von Zeichen folgen, die verwenden, um einzelne oder mehrere Zeichen zu speichern. MOF verfügt auch über eine Reihe von Regeln, die die Verwendung von Anführungszeichen innerhalb einer Zeichenfolge beschreiben.

In der folgenden Tabelle sind die Zeichen folgen Datentypen für MOF aufgeführt.



| Datentyp  | Automatisierungstyp | BESCHREIBUNG                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **VT \_ I2**      | Einzelnes 16-Bit-Unicode-Zeichen im UCS-2-Format (Universal Character Set 2)<br/> |
| **string** | **VT \_ BSTR**    | Unicode-Zeichenfolge<br/>                                                    |



 

Beachten Sie beim Schreiben von Zeichen folgen für MOF die folgenden Richtlinien:

-   Umschließen Sie Einzelzeichen Konstanten in einfache Anführungszeichen.

    Wenn Sie keine einfachen Anführungszeichen mit Einzelzeichen Konstanten verwenden, müssen Sie die ganzzahlige Darstellung des Unicode-Zeichen Werts verwenden. Optional können Sie das Zeichen mit der \\ x-Escapesequenz aus dem American National Standards Institute (ANSI) C-Standard angeben, wie hier gezeigt:

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Da MOF auf Unicode basiert, können Sie auch 16-Bit-Werte angeben.

    Beachten Sie, dass Einzelzeichen Konstanten im ANSI C-Format in doppelte Anführungszeichen eingeschlossen sind.

-   Umschließen Sie Zeichen folgen in doppelte Anführungszeichen.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Verketten Sie nachfolgende Anführungszeichen folgen mit einem oder mehreren Leerzeichen.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Verwenden Sie eine Escapesequenz mit einem umgekehrten Schrägstrich, um Anführungszeichen in eine Zeichenfolge einzubetten.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

Im folgenden Beispiel wird beschrieben, wie Zeichen folgen Eigenschaften und ein Zeichen folgen Parameter initialisiert werden:

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

 

 




