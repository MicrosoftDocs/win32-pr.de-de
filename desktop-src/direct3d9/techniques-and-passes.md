---
description: Techniken stellen den renderingmuskel bereit. Eine Technik kapselt den Effekt Zustand, der einen Renderingstil bestimmt. Eine Technik besteht aus einem oder mehreren Durchläufen.
ms.assetid: 0a4d8f44-c7c0-4355-ac7f-6bc3315eeff0
title: Techniken und Pässe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3a68ac40db16b3e6819adf6fcd1f8a6f790325
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345602"
---
# <a name="techniques-and-passes-direct3d-9"></a>Techniken und Pässe (Direct3D 9)

Techniken stellen den renderingmuskel bereit. Eine Technik kapselt den Effekt Zustand, der einen Renderingstil bestimmt. Eine Technik besteht aus einem oder mehreren Durchläufen.

## <a name="techniques"></a>O

Die Syntax zum Aufrufen einer Technik lautet wie folgt:


```
technique [ id ]  [< annotation(s) >] 
    { pass(es) }
```



Hierbei gilt:

-   ID ist ein optionaler eindeutiger Name.
-   die Anmerkung ist 0 (null) oder mehr optionale benutzerspezifische Informationen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).
-   "Pass (es)" ist 0 (null) oder größer. Jeder Durchlauf enthält Zustands Zuweisungen. Siehe unten.

## <a name="passes"></a>Ausweisen

Ein Durchlauf enthält die zum renderbedarf erforderlichen Zustands Zuweisungen.


```
pass  [ id ]  [< annotation(s) >] 
    { state assignment(s) }
```



Hierbei gilt:

-   ID ist ein optionaler eindeutiger Name.
-   die Anmerkung ist eine oder mehrere optionale benutzerspezifische Informationen. Weitere [Informationen finden Sie unter Hinzufügen von Informationen zu Effekt Parametern mit \_ Anmerkungen](using-an-effect.md).
-   Zuweisung (en) weist NULL oder mehr Zustands Werte zu oder wertet mindestens einen Ausdruck aus. Weitere Informationen finden Sie unter [Wirkungs Zustände (Direct3D 9)](effect-states.md) und [Ausdrücke (Direct3D 9)](expressions.md).

Übergibt alle außer der letzten Zuweisung in einem Satz von wiederholten Zuweisungen in denselben Zustand.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



