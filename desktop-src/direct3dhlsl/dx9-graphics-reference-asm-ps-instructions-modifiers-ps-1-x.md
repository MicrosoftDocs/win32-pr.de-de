---
title: Modifiziererer für ps_1_X
description: Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird.
ms.assetid: 15b892da-b6fd-4bd5-8889-bc48035e7819
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbc8a9b13f7ffc29cf84bc839409f29bea6c8c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856959"
---
# <a name="modifiers-for-ps_1_x"></a>Modifiziererer für PS \_ 1 \_ X

Anweisungsmodifiziererer wirken sich auf das Ergebnis der Anweisung aus, bevor Sie in das Ziel Register geschrieben wird. Verwenden Sie diese beispielsweise, um das Ergebnis durch einen Faktor von zwei zu multiplizieren oder aufzuteilen, oder um das Ergebnis zwischen null und eins zu binden. Anweisungsmodifiziererer werden angewendet, nachdem die Anweisung ausgeführt wurde, aber bevor das Ergebnis in das Ziel Register geschrieben wurde.

Eine Liste der Modifizierer ist unten dargestellt.



| Modifizierer | BESCHREIBUNG                   | Syntax           | Version |      |      |      |
|----------|-------------------------------|------------------|---------|------|------|------|
|          |                               |                  | 1\_1    | 1\_2 | 1 \_ 3 | 1\_4 |
| \_x2     | Multiplizieren um 2                 | Anweisung \_ x2  | X       | X    | X    | X    |
| \_x4     | Multiplizieren um 4                 | Anweisung \_ X4  | X       | X    | X    | X    |
| \_x8     | Multiplizieren um 8                 | Anweisung \_ x8  |         |      |      | X    |
| \_D2     | Dividieren durch 2                   | Anweisung \_ D2  | X       | X    | X    | X    |
| \_D4     | Dividieren durch 4                   | Anweisung \_ D4  |         |      |      | X    |
| \_D8     | Dividieren durch 8                   | Anweisung \_ D8  |         |      |      | X    |
| \_gesetzt    | Vollständig (Klammer zwischen 0 und 1) | Anweisung \_ Sat | X       | X    | X    | X    |



 

-   Der Multiplikations Modifizierer multipliziert die Register Daten mit einer Potenz von zwei, nachdem Sie gelesen wurde. Dies ist das gleiche wie bei einer UMSCHALT links.
-   Der Divide-Modifizierer dividiert die Register Daten durch eine Potenz von zwei, nachdem Sie gelesen wurde. Dies ist das gleiche wie ein UMSCHALT Recht.
-   Der Bezeichner "Bezeichner" bindet den Bereich der Registerwerte von 0 (null) auf 1.

Anweisungsmodifiziererer können in arithmetischen Anweisungen verwendet werden. Sie dürfen nicht in Textur Adress Anweisungen verwendet werden.

Modifizierer multiplizieren

In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen und das Ergebnis mit zwei multipliziert.


```
add_x2 dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungs Modifizierer kombiniert. Zuerst werden zwei Farben in den Quell Operanden (src0 und Quelle1) hinzugefügt. Das Ergebnis wird dann mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden. Das Ergebnis wird im Ziel Register gespeichert.


```
add_x2_sat dest, src0, src1
```



Divide-Modifizierer

In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen und das Ergebnis durch zwei dividiert.


```
add_d2 dest, src0, src1
```



-Modifizierer

Bei arithmetischen Anweisungen bindet der Sättigungs Modifizierer das Ergebnis dieser Anweisung für jede Komponente in den Bereich 0,0 bis 1,0. Im folgenden Beispiel wird gezeigt, wie dieser Anweisungs Modifizierer verwendet wird.


```
dp3_sat r0, t0_bx2, v0_bx2    ; t0 is bump, v0 is light direction
```



Dieser Vorgang tritt nach jedem Multiplikations-oder Teilungs Anweisungs Modifizierer auf. \_"Sat" wird am häufigsten verwendet, um Punktprodukt Ergebnisse zu binden. Sie ermöglicht jedoch auch eine konsistente Emulation von Multipass-Methoden, bei denen sich der Frame Puffer immer im Bereich von 0 bis 1 und in der Multitextur-Syntax von DirectX 6 und 7,0 befindet, in der die Sättigung definiert ist, die in jeder Phase auftritt.

In diesem Beispiel wird das Ziel Register (dest) mit der Summe der beiden Farben in den Quell Operanden (src0 und Quelle1) geladen, und das Ergebnis wird für jede Komponente in den Bereich 0,0 bis 1,0 geklammert.


```
add_sat dest, src0, src1
```



In diesem Beispiel werden zwei Anweisungs Modifizierer kombiniert. Zuerst werden zwei Farben in den Quell Operanden (src0 und Quelle1) hinzugefügt. Das Ergebnis wird mit zwei multipliziert und für jede Komponente zwischen 0,0 und 1,0 gebunden. Das Ergebnis wird im Ziel Register gespeichert.


```
add_x2_sat dest, src0, src1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




