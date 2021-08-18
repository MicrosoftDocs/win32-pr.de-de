---
description: Techniken stellen die Rendering-Darstellung zur Verfügung. Eine Technik kapselt den Effektzustand, der einen Renderingstil bestimmt. Eine Technik besteht aus einem oder mehr Durchläufen.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Techniken und Durchläufe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9999927d96a914b80f870a2128b0eae12074616e4ae787b011551b6aab919220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044208"
---
# <a name="techniques-and-passes-direct3d-9"></a>Techniken und Durchläufe (Direct3D 9)

Techniken stellen die Rendering-Darstellung zur Verfügung. Eine Technik kapselt den Effektzustand, der einen Renderingstil bestimmt. Eine Technik besteht aus einem oder mehr Durchläufen.

## <a name="techniques"></a>Techniken

Die Syntax zum Aufrufen einer Technik lautet wie folgt:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Hierbei gilt:

-   id ist ein optionaler eindeutiger Name.
-   annotation ist 0 (null) oder mehr optionale Teile von benutzerspezifischen Informationen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit \_ Anmerkungen.](using-an-effect.md)
-   pass(es) ist 0 (null) oder mehr Durchläufe. Jeder Durchgang enthält Zustandszuweisungen. Siehe unten.

## <a name="passes"></a>Übergibt

Ein Durchgang enthält die Zustandszuweisungen, die zum Rendern erforderlich sind.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Hierbei gilt:

-   id ist ein optionaler eindeutiger Name.
-   annotation ist ein oder mehrere optionale benutzerspezifische Informationen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effektparametern mit \_ Anmerkungen.](using-an-effect.md)
-   -Zuweisung(en) weist 0 (null) oder mehr Zustandswerte zu oder wertet einen oder mehrere Ausdrücke aus. Siehe [Effektzustände (Direct3D 9)](effect-states.md) und [Ausdrücke (Direct3D 9).](expressions.md)

Übergibt alle bis auf die letzte Zuweisung in einer Reihe von wiederholten Zuweisungen zum gleichen Zustand.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effect-Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



