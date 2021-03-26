---
title: Grammatik
description: HLSL-Anweisungen werden mithilfe der folgenden Regeln für die Grammatik erstellt.
ms.assetid: 683248e9-6fc7-451a-906b-6e0aab1b0c8c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d2346e1ca2302f80c796558b4aa2bbdce016d494
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516520"
---
# <a name="grammar"></a>Grammatik

HLSL-Anweisungen werden mithilfe der folgenden Regeln für die Grammatik erstellt.

-   [Leerzeichen](#whitespace)
-   [Gleit Komma Zahlen](#floating-point-numbers)
-   [Ganze Zahlen](#integer-numbers)
-   [Zeichen](#characters)
-   [Zeichenfolgen](#strings)
-   [Identifiers (Bezeichner)](#identifiers)
-   [Operatoren](#operators)
-   [Zugehörige Themen](#related-topics)

## <a name="whitespace"></a>Leerraum

Die folgenden Zeichen werden als Leerzeichen erkannt.



|                            |
|----------------------------|
| SPACE                      |
| TAB                        |
| EOL                        |
| C-Stil Kommentare (/ \* \* /) |
| C++-Stil Kommentare (//)    |



 

## <a name="floating-point-numbers"></a>Gleit Komma Zahlen

Gleit Komma Zahlen werden in HLSL wie folgt dargestellt:

-   Bruchteil-Konstante Exponent-Part (opt) Floating-Suffix (opt)

    Exponent-Part-enumerationszeichen für Digit-Sequence (opt)

-   Bruch Komma Konstante:

    Ziffern Sequenz (opt). Ziffern Sequenz

    Ziffern Sequenz.

-   Exponent-Part:

    e-Sign (opt)-Ziffern Sequenz

    E-Sign (opt)-Ziffern Sequenz

-   sign : eins der folgenden Zeichen

    \+ -

-   Ziffern Sequenz:

    digit

    digit-sequence-Stelle

-   floating-suffix : eins der folgenden Zeichen

    h h f f l l

    Verwenden Sie das Suffix "L", um ein vollständiges Gleit Komma Trennzeichen mit 64-Bit-Genauigkeit anzugeben. Standardmäßig ist ein Gleit Komma Wert von 32 Bit.

    Der Compiler erkennt z. b. den folgenden Literalwert als Gleit Komma-Literale mit 32-Bit-Genauigkeit und ignoriert die unteren Bits:

    ```
    double x = -0.6473313946860445;
    ```

    

    Der Compiler erkennt den folgenden Literalwert als Gleit Komma-Literale mit 64-Bit-Genauigkeit:

    ```
    double x = -0.6473313946860445L;
    ```

    

## <a name="integer-numbers"></a>Ganze Zahlen

Ganzzahlige Zahlen werden in HLSL wie folgt dargestellt:

-   integer-Konstante Integer-Suffix (opt)
-   ganzzahlige Konstante: eine von

    \# (Dezimalzahl)

    0 \# (oktale Zahl)

    0x (hexadezimale \# Zahl)

-   ganzzahliges Suffix kann eines der folgenden sein:

    u u l l

## <a name="characters"></a>Zeichen

Zeichen werden in HLSL wie folgt dargestellt:



|                                           |                                                                 |
|-------------------------------------------|-----------------------------------------------------------------|
| „c“                                       | Art                                                     |
| ' \\ a ' ' \\ b ' ' \\ f ' ' \\ b ' ' \\ r ' ' \\ t ' ' \\ v ' | entkam                                                       |
| '\\\#\#\#'                                | (oktale Escapezeichen, jede \# ist eine oktale Ziffer)                       |
| " \\ x \# "                                   | (Hex-Escapezeichen, ist hexadezimal \# Zahl, beliebige Anzahl von Ziffern)            |
| " \\ c"                                     | (c ist ein anderes Zeichen, einschließlich umgekehrter Schrägstriche und Anführungszeichen) |



 

Escapezeichen werden in Präprozessorausdrücken nicht unterstützt.

## <a name="strings"></a>Zeichenfolgen

Zeichen folgen werden in HLSL wie folgt dargestellt:

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



Auch ein beliebiges anderes einzelnes Zeichen, das nicht mit einer anderen Regel identisch war.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




