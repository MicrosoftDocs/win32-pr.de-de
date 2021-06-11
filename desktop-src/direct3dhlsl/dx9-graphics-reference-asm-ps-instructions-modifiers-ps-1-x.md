---
title: Modifizierer für ps_1_X
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c97196040a8f5f9888cb2fb354dcc18ca3743c7
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988725"
---
# <a name="modifiers-for-ps_1_x"></a>Modifizierer für ps \_ 1 \_ X

Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Verwenden Sie sie beispielsweise, um das Ergebnis durch den Faktor 2 zu multiplizieren oder zu dividieren oder um das Ergebnis zwischen 0 und 1 zu klammern. Anweisungsmodifizierer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Zielregister geschrieben wird.

Eine Liste der Modifizierer ist unten dargestellt.



| Modifizierer | BESCHREIBUNG                   | Syntax           | Version |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_x2     | Multiplizieren mit 2                 | Anweisung \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplizieren mit 4                 | Anweisung \_ x4  | X       | X    | X    | X    |
| \_x8     | Multiplizieren mit 8                 | Anweisung \_ x8  |         |      |      | X    |
| \_d2     | Division durch 2                   | Anweisung \_ d2  | X       | X    | X    | X    |
| \_d4     | Division durch 4                   | Anweisung \_ d4  |         |      |      | X    |
| \_d8     | Division durch 8                   | Anweisung \_ d8  |         |      |      | X    |
| \_Sat    | Saturate (Klammer von 0 und 1) | Anweisung \_ sa | X       | X    | X    | X    |



 

-   Der Multiplikationsmodifizierer multipliziert die Registerdaten mit einer Zweierleistung, nachdem sie gelesen wurden. Dies ist identisch mit einer Verschiebung nach links.
-   Der Divide-Modifizierer dividiert die Registerdaten nach dem Lesen durch eine Zweierkraft. Dies ist identisch mit einer Verschiebung nach rechts.
-   Der Saturate-Modifizierer klammert den Bereich der Registerwerte von 0 bis 1.

Anweisungsmodifizierer können für arithmetische Anweisungen verwendet werden. Sie dürfen nicht für Texturadressenanweisungen verwendet werden.

Multiplikationsmodifizierer

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis mit zwei multipliziert.


```
add_x2 dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert. Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt. Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 geklammert. Das Ergebnis wird im Zielregister gespeichert.


```
add_x2_sat dest, src0, src1
```



Divide-Modifizierer

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis durch zwei dividiert.


```
add_d2 dest, src0, src1
```



Saturate-Modifizierer

Bei arithmetischen Anweisungen klammert der Sättigungsmodifizierer das Ergebnis dieser Anweisung für jede Komponente in den Bereich 0,0 bis 1,0. Im folgenden Beispiel wird die Verwendung dieses Anweisungsmodifizierers veranschaulicht.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Dieser Vorgang erfolgt nach jedem Multiplikations- oder Divisionsanweisungsmodifizierer. \_Sat wird am häufigsten verwendet, um Punktproduktergebnisse zu klammern. Sie ermöglicht jedoch auch eine konsistente Emulation von Multipassmethoden, bei denen der Framepuffer immer im Bereich von 0 bis 1 liegt, und der DirectX 6- und 7.0-Multitextursyntax, bei der die Sättigung in jeder Phase definiert ist.

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis für jede Komponente in den Bereich 0,0 bis 1,0 klammert.


```
add_sat dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert. Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt. Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 geklammert. Das Ergebnis wird im Zielregister gespeichert.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen zum Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




