---
description: In MOF sind Zahlen Ziffern, die numerische Werte beschreiben. MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden, und ermöglicht auch, dass diese Zahlen in unterschiedlichen Formaten vorliegen. In der folgenden Tabelle sind die numerischen Werte aufgeführt, die MOF unterstützt.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Zahlen (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3441988bb91d4bb2f3742016f01cb69996e3dcb55081a6723d851ed74cc1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555138"
---
# <a name="numbers-wmi"></a>Zahlen (WMI)

In MOF sind Zahlen Ziffern, die numerische Werte beschreiben. MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden, und ermöglicht auch, dass diese Zahlen in unterschiedlichen Formaten vorliegen. In der folgenden Tabelle sind die numerischen Werte aufgeführt, die MOF unterstützt.



| Datentyp  | Automatisierungstyp | BESCHREIBUNG                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **sint8**  | **VT \_ I2**      | 8-Bit-Ganzzahl mit Vorzeichen.<br/>                                                                                                                                        |
| **sint16** | **VT \_ I2**      | 16-Bit-Ganzzahl mit Vorzeichen.<br/>                                                                                                                                       |
| **sint32** | VT \_ I4          | 32-Bit-Ganzzahl mit Vorzeichen.<br/>                                                                                                                                       |
| **sint64** | **VT \_ BSTR**    | 64-Bit-Ganzzahl mit Vorzeichen in Zeichenfolgenform. Dieser Typ folgt dem Hexadezimal- oder Dezimalformat gemäß den C-Regeln der American National Standards Institute (ANSI).<br/> |
| **real32** | **VT \_ R4**      | 4-Byte-Gleitkommawert, der dem IEEE-Standard (Institute of Electrical and Electronics Engineers, Inc.) folgt.<br/>                                        |
| **real64** | **VT \_ R8**      | 8-Byte-Gleitkommawert, der dem IEEE-Standard folgt.<br/>                                                                                                  |
| **uint8**  | **VT \_ UI1**     | 8-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                      |
| **uint16** | **VT \_ I4**      | 16-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                     |
| **uint32** | **VT \_ I4**      | 32-Bit-Ganzzahl ohne Vorzeichen.<br/>                                                                                                                                     |
| **uint64** | **VT \_ BSTR**    | 64-Bit-Ganzzahl ohne Vorzeichen in Zeichenfolgenform. Dieser Typ folgt dem Hexadezimal- oder Dezimalformat gemäß ANSI C-Regeln.<br/>                                           |



 

Obwohl der MOF-Code flexibel ist, treten beim Umgang mit Automation einige Änderungen auf:

-   Sie müssen 64-Bit-Ganzzahlen als Zeichenfolgen codieren.

    Automation unterstützt keinen ganzzahligen 64-Bit-Typ.

-   Automatisierungstypen entsprechen nicht immer in Bitgröße MOF-Datentypen.

    Automation verwendet beispielsweise VT \_ I4, um einen 16-Bit-Wert ohne Vorzeichen zurückzugeben. Diese Diskrepanz besteht aufgrund von Problemen mit der Anmeldeerweiterung. Wenn Automation \_ VT I2 anstelle von VT \_ I4 verwendet, scheint 65.536 der Wert 1 zu sein, was Typ- und Bereichsprobleme verursacht. Analog dazu stellt Automation den **uint32-Typ** als VT I4 dar, \_ da kein größerer ganzzahliger Typ vorhanden ist, der **uint32** enthält.

-   Sie müssen keine Darstellung für 8-Bit-Zahlentypen ändern.

    Automation unterstützt VT \_ UI1, einen 8-Bit-Typ ohne Vorzeichen.

MOF unterstützt lange Konstanten. Sie deklarieren eine lange Konstante mithilfe einer einfachen Reihe von Ziffern mit einem optionalen negativen Vorzeichen. Eine long-Konstante darf die Größe der Variablen nicht überschreiten, die deklariert ist, um sie zu speichern. Einige Beispiele für lange Konstanten sind 1000 und 12310.

MOF unterstützt auch alternative numerische Formate. In der folgenden Tabelle sind die Sonderzeichen aufgeführt, die Sie verwenden müssen, um hexadezimale, binäre und oktale Konstanten zu beschreiben.



| Konstante               | Sonderzeichen     | Beispiel                   |
|------------------------|-----------------------|---------------------------|
| Decimal<br/>     | Keine<br/>       | val = 65<br/>       |
| Hexadezimal<br/> | 0x-Präfix<br/>  | val = 0x41<br/>     |
| Oktal<br/>       | Führende 0<br/>  | val = 0101<br/>     |
| Binary<br/>      | Nachgestelltes B<br/> | val = 1000001B<br/> |



 

Sie können eine Gleitkommakonstante verwenden, um wissenschaftliche Notation sowie Bruchzahlen darzustellen, wie im Folgenden gezeigt:

``` syntax
3.14
-3.14
-1.2778E+02
```

WMI betrachtet Gleitkommakonstanten als **VT \_ R8-Typen** für Automation.

Im folgenden Beispiel werden Klassen- und Instanzdeklarationen beschrieben, die veranschaulichen, wie die einzelnen numerischen Datentypen zum Festlegen von Eigenschaften verwendet werden:

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

 

 




