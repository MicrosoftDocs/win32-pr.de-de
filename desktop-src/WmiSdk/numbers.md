---
description: In MOF sind Zahlen Ziffern, die numerische Werte beschreiben. MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden. Außerdem können diese Zahlen in unterschiedlichen Formaten vorliegen. In der folgenden Tabelle werden die numerischen Werte aufgelistet, die von MOF unterstützt werden.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Zahlen (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346890"
---
# <a name="numbers-wmi"></a>Zahlen (WMI)

In MOF sind Zahlen Ziffern, die numerische Werte beschreiben. MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden. Außerdem können diese Zahlen in unterschiedlichen Formaten vorliegen. In der folgenden Tabelle werden die numerischen Werte aufgelistet, die von MOF unterstützt werden.



| Datentyp  | Automatisierungstyp | BESCHREIBUNG                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | 8-Bit-Ganzzahl mit Vorzeichen.<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | Ganze 16-Bit-Zahl mit Vorzeichen.<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | 32-Bit-Ganzzahl mit Vorzeichen.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | 64-Bit-Ganzzahl mit Vorzeichen in Form einer Zeichenfolge. Dieser Typ folgt dem Hexadezimal-oder Dezimal Format gemäß den American National Standards Institute (ANSI) C-Regeln.<br/> |
| **real32** | **VT \_ R4**      | ein 4-Byte-Gleit Komma Wert, der dem Institute of Electrical and Electronics Engineers, Inc. (IEEE) Standard folgt.<br/>                                        |
| **real64** | **VT \_ R8**      | 8-Byte-Gleit Komma Wert, der auf den IEEE-Standard folgt.<br/>                                                                                                  |
| **Uint8**  | **VT \_ UI1**     | 8-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                      |
| **uint16** | **VT \_ I4**      | 16-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | 32-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | 64-Bit-Ganzzahl ohne Vorzeichen in Form einer Zeichenfolge. Dieser Typ folgt dem Hexadezimal-oder Dezimal Format gemäß den ANSI C-Regeln.<br/>                                           |



 

Obwohl der MOF-Code flexibel ist, treten beim Umgang mit Automation einige Änderungen auf:

-   Sie müssen 64-Bit-Ganzzahlen als Zeichen folgen codieren.

    Automation unterstützt keinen ganzzahligen 64-Bit-Typ.

-   Automatisierungs Typen entsprechen nicht immer den MOF-Datentypen.

    Automation verwendet beispielsweise VT \_ I4, um einen 16-Bit-Wert ohne Vorzeichen zurückzugeben. Diese Abweichung ist aufgrund von Problemen mit der Signatur Erweiterung vorhanden. Wenn \_ die Automatisierung die Verwendung von VT I2 anstelle von VT I4 verwendet \_ hat, scheint 65.536 der Wert 1 zu sein, was zu Typen-und Bereichs Problemen führt. Ebenso stellt Automation den **UInt32** -Typ als VT \_ I4 dar, da kein größerer ganzzahliger Typ vorhanden ist, der **UInt32** enthalten soll.

-   Sie müssen keine Darstellung für 8-Bit-Zahlen Typen ändern.

    Automation unterstützt VT \_ UI1, einen 8-Bit-Typ ohne Vorzeichen.

MOF unterstützt lange Konstanten. Sie deklarieren eine lange Konstante mit einer einfachen Reihe von Ziffern mit einem optionalen negativen Vorzeichen. Eine lange Konstante darf nicht die Größe der Variablen überschreiten, die für die Speicherung deklariert ist. Einige Beispiele für lange Konstanten sind 1000 und 12310.

MOF unterstützt auch alternative numerische Formate. In der folgenden Tabelle werden die Sonderzeichen aufgelistet, die Sie zum Beschreiben von hexadezimalen, binären und oktalen Konstanten verwenden müssen.



| Konstante               | Sonderzeichen     | Beispiel                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | Keine<br/>       | Val = 65<br/>       |
| Hexadezimal<br/> | 0x-Präfix<br/>  | Val = 0x41<br/>     |
| Oktal<br/>       | Führende 0<br/>  | Val = 0101<br/>     |
| Binary<br/>      | Nachfolgende B<br/> | Val = 1000001b<br/> |



 

Sie können eine Gleit Komma Konstante verwenden, um wissenschaftliche Schreibweise und Bruchteile darzustellen, wie im folgenden dargestellt:

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI betrachtet Gleit Komma Konstanten als **VT \_ R8** -Typen für die Automatisierung.

Im folgenden Beispiel werden Klassen-und instanzdeklarationen beschrieben, die veranschaulichen, wie die einzelnen numerischen Datentypen verwendet werden, um Eigenschaften festzulegen:

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




