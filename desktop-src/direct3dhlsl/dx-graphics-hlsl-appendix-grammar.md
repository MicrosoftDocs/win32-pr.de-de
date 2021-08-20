---
title: Grammatik
description: HLSL-Anweisungen werden mit den folgenden Regeln für die Grammatik erstellt.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86549f441752e72fd11a741a061fcaf839eca0140f4766b0932094d74dc78085
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855070"
---
# <a name="grammar"></a>Grammatik

HLSL-Anweisungen werden mit den folgenden Regeln für die Grammatik erstellt.

-   [Leerraum](#whitespace)
-   [Gleitkommazahlen](#floating-point-numbers)
-   [Ganze Zahlen](#integer-numbers)
-   [Zeichen](#characters)
-   [Zeichenfolgen](#strings)
-   [Identifiers (Bezeichner)](#identifiers)
-   [Operatoren](#operators)
-   [Zugehörige Themen](#related-topics)

## <a name="whitespace"></a>Leerraum

Die folgenden Zeichen werden als Leerzeichen erkannt.

- SPACE
- TAB
- Eol
- Kommentare im C-Stil (/ \* \* /)
- Kommentare im C++-Stil (/)

## <a name="floating-point-numbers"></a>Gleitkommazahlen

Gleitkommazahlen werden in HLSL wie folgt dargestellt:

-   fractional-constant exponent-part(opt) floating-suffix(opt)

    digit-sequence exponent-part floating-suffix(opt)

-   fractional-constant :

    digit-sequence(opt) . digit-sequence

    digit-sequence .

-   exponent-part :

    e sign(opt) digit-sequence

    E sign(opt) digit-sequence

-   sign : eins der folgenden Zeichen

    \+ -

-   digit-sequence :

    digit

    digit-sequence-Stelle

-   floating-suffix : eins der folgenden Zeichen

    h H f F l L

    Verwenden Sie das Suffix "L", um ein vollständiges Gleitkommaliteral mit 64-Bit-Genauigkeit anzugeben. Ein 32-Bit-Float-Literal ist die Standardeinstellung.

    Beispielsweise erkennt der Compiler den folgenden Literalwert als Gleitkommaliteral mit 32-Bit-Genauigkeit und ignoriert die unteren Bits:

    ```
    double x = -0.6473313946860445;
    ```

    

    Der Compiler erkennt den folgenden Literalwert als Gleitkommaliteral mit 64-Bit-Genauigkeit:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Ganze Zahlen

Ganzzahlige Zahlen werden in HLSL wie folgt dargestellt:

-   integer-constant integer-suffix(opt)
-   integer-constant: eine von

    \# (Dezimalzahl)

    0 \# (Oktalzahl)

    0x \# (Hexadezimalzahl)

-   integer-suffix kann eine der folgenden Sein:

    u U l L

## <a name="characters"></a>Zeichen

Zeichen werden in HLSL wie folgt dargestellt:



| Zeichen                                          | BESCHREIBUNG                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| „c“                                       | (Zeichen)                                                     |
| \\'a' ' \\ b' ' \\ f' ' \\ b' ' \\ r' ' \\ t' ' \\ v' | (Escapes)                                                       |
| '\\\#\#\#'                                | (oktales Escape,jedes \# ist eine Oktalziffer)                       |
| ' \\ x \# '                                   | (Hexadezimale \# Escapezeichen, hexadezimale Zahl, beliebige Anzahl von Ziffern)            |
| ' \\ c'                                     | (c ist ein anderes Zeichen, einschließlich schräger Schrägstriche und Anführungszeichen) |



 

Escapes werden in Präprozessorausdrücken nicht unterstützt.

## <a name="strings"></a>Zeichenfolgen

Zeichenfolgen werden in HLSL wie folgt dargestellt:

"s" (s ist eine beliebige Zeichenfolge mit Escapes).

## <a name="identifiers"></a>Bezeichner

Bezeichner werden in HLSL wie folgt dargestellt:


```
    [A-Za-z_][A-Za-z0-9_]*
```



## <a name="operators"></a>Operatoren


```
##, #@, ++, --, &, &, &, ||, ==, ::, <<, <<=, >>, >>=, ..., 
<=, >=, !=, *=, /=, +=, -=, %=, &=, |=, ^=, ->
```



Auch alle anderen einzelnen Zeichen, die nicht mit einer anderen Regel übereinstimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




