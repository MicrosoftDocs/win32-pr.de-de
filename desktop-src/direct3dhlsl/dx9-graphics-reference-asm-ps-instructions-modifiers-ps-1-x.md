---
title: Modifizierer für ps_1_X
description: Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Erfahren Sie mehr über Modifizierer für ps_1_X.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9291d818252c95bc11fae72bd3311ec733a45fa
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129939"
---
# <a name="modifiers-for-ps_1_x"></a>Modifizierer für PS \_ 1 \_ X

Anweisungsmodifizierer beeinflussen das Ergebnis der Anweisung, bevor sie in das Zielregister geschrieben wird. Verwenden Sie sie beispielsweise, um das Ergebnis mit einem Faktor von zwei zu multiplizieren oder zu dividieren oder um das Ergebnis zwischen 0 und 1 zu binden. Anweisungsmodifizierer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Zielregister geschrieben wird.

Eine Liste der Modifizierer ist unten dargestellt.



| Modifizierer | BESCHREIBUNG                   | Syntax           | Version 1 \_ 1 | Version 1 \_ 2     |Version 1 \_ 3    | Version 1 \_ 4    |
|----------|-------------------------------|------------------|---------|------|------|------|
| \_x2     | Multiplizieren mit 2                 | Anweisung \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplizieren mit 4                 | Anweisung \_ x4  | X       | X    | X    | X    |
| \_x8     | Multiplizieren mit 8                 | Anweisung \_ x8  |         |      |      | X    |
| \_d2     | Dividieren durch 2                   | Anweisung \_ d2  | X       | X    | X    | X    |
| \_d4     | Dividieren durch 4                   | Anweisung \_ d4  |         |      |      | X    |
| \_d8     | Dividieren durch 8                   | Anweisung \_ d8  |         |      |      | X    |
| \_sat    | Saturate (Klammer von 0 und 1) | \_Anweisungs-Sat | X       | X    | X    | X    |



 

-   Der Multiplikationsmodifizierer multipliziert die Registerdaten nach dem Lesen mit einer Potenz von zwei. Dies entspricht einer Verschiebung nach links.
-   Der Divisionsmodifizierer dividiert die Registerdaten durch eine Potenz von zwei, nachdem sie gelesen wurden. Dies entspricht einer Verschiebung nach rechts.
-   Mit dem Saturate-Modifizierer wird der Bereich der Registerwerte von 0 (null) bis 1 (1) klammern.

Anweisungsmodifizierer können für arithmetische Anweisungen verwendet werden. Sie dürfen nicht für Texturadressanweisungen verwendet werden.

Multiplikationsmodifizierer

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis mit zwei multipliziert.


```
add_x2 dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert. Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt. Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden. Das Ergebnis wird im Zielregister gespeichert.


```
add_x2_sat dest, src0, src1
```



Division-Modifizierer

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis durch zwei dividiert.


```
add_d2 dest, src0, src1
```



Saturate-Modifizierer

Bei arithmetischen Anweisungen klammern die Sättigungsmodifizierer das Ergebnis dieser Anweisung in den Bereich von 0,0 bis 1,0 für jede Komponente ein. Im folgenden Beispiel wird die Verwendung dieses Anweisungsmodifizierer veranschaulicht.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Dieser Vorgang tritt nach jedem Multiplikations- oder Divisionsanweisungsmodifizierer auf. \_sat wird am häufigsten verwendet, um Punktproduktergebnisse zu klammern. Sie ermöglicht jedoch auch eine konsistente Emulation von Multipass-Methoden, bei denen sich der Framepuffer immer im Bereich von 0 bis 1 und in der Multitexture-Syntax von DirectX 6 und 7.0 befindet, in der die Sättigung in jeder Phase definiert ist.

In diesem Beispiel wird das Zielregister (dest) mit der Summe der beiden Farben in den Quellopernden (src0 und src1) geladen und das Ergebnis für jede Komponente in den Bereich von 0,0 bis 1,0 eingebunden.


```
add_sat dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungsmodifizierer kombiniert. Zunächst werden zwei Farben in den Quellopernden (src0 und src1) hinzugefügt. Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden. Das Ergebnis wird im Zielregister gespeichert.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




