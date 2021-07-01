---
title: Grammatik
description: HLSL-Anweisungen werden mit den folgenden Grammatikregeln erstellt.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b77f1050beaee2b269d12e69704018e3c5abee6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129848"
---
# <a name="grammar"></a>Grammatik

HLSL-Anweisungen werden mit den folgenden Grammatikregeln erstellt.

-   [Leerraum](#whitespace)
-   [Gleitkommazahlen](#floating-point-numbers)
-   [Ganze Zahlen](#integer-numbers)
-   [Zeichen](#characters)
-   [Zeichenfolgen](#strings)
-   [Identifiers (Bezeichner)](#identifiers)
-   [Operatoren](#operators)
-   [Verwandte Themen](#related-topics)

## <a name="whitespace"></a>Leerraum

Die folgenden Zeichen werden als Leerzeichen erkannt.

- SPACE
- TAB
- Eol
- C-Stilkommentare (/ \* \* /)
- C++-Stilkommentare (/)

## <a name="floating-point-numbers"></a>Gleitkommazahlen

Gleitkommazahlen werden in HLSL wie folgt dargestellt:

-   fractional-constant exponent-part(opt) floating-suffix(opt)

    digit-sequence exponent-part floating-suffix(opt)

-   fractional-constant :

    digit-sequence(opt) . Ziffernsequenz

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

    Verwenden Sie das Suffix "L", um ein vollständiges Gleitkommaliteral mit 64-Bit-Genauigkeit anzugeben. Ein 32-Bit-Floatliteral ist die Standardeinstellung.

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

    0 \# (oktale Zahl)

    0x \# (Hexadezimalzahl)

-   Integer-Suffix kann eines der folgenden Sein:

    u U l L

## <a name="characters"></a>Zeichen

Zeichen werden in HLSL wie folgt dargestellt:



| Zeichen                                          | Beschreibung                                                                |
|-------------------------------------------|-----------------------------------------------------------------|
| „c“                                       | (Zeichen)                                                     |
| \\'a' ' \\ b' ' f ' \\ \\ b' ' \\ r' ' t ' ' \\ \\ v' | (Escapes)                                                       |
| '\\\#\#\#'                                | (oktales Escapezeichen, jedes \# ist eine oktale Ziffer)                       |
| ' \\ x \# '                                   | (hexadezimales Escapezeichen, \# ist eine hexadezimale Zahl, eine beliebige Anzahl von Ziffern)            |
| ' \\ c'                                     | (c ist ein anderes Zeichen, einschließlich umgekehrter Schrägstriche und Anführungszeichen) |



 

Escapen werden in Präprozessorausdrücken nicht unterstützt.

## <a name="strings"></a>Zeichenfolgen

Zeichenfolgen werden in HLSL wie folgt dargestellt:

"s" (s ist eine beliebige Zeichenfolge mit Escapezeichen).

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



Außerdem jedes andere einzelne Zeichen, das keiner anderen Regel entspricht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




