---
description: Definiert den Patch für ein B&\# 233; Zier Steuerelement. Das Array definiert die Steuerungs Punkte für den Patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859977"
---
# <a name="patch"></a>Patch

Definiert einen Patch für das Bézier-Steuerelement. Das Array definiert die Steuerungs Punkte für den Patch.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Hierbei gilt:

-   ncontrolindices-Anzahl von Steuerungspunkt Indizes.
-   Array DWORD controlindices \[ ncontrolindices \] -Array von Steuerungspunkt Indizes.

Der Typ des Patches wird durch die Anzahl von Kontrollpunkten definiert, wie in der folgenden Tabelle dargestellt.



| Anzahl von Kontrollpunkten | type                              |
|--------------------------|-----------------------------------|
| 10                       | Eckige, eckige Bézier-Patch     |
| 15                       | Dreiecks-Patch für quartic Bézier   |
| 16                       | Patch für Quad-Bézier-Quad-Rechteck |



 

Die Reihenfolge der Kontrollpunkte wird in einem Spiralmuster angegeben, wie in den folgenden Diagrammen für dreieckige und rechteckige Patches gezeigt.

Für dreieckige Patches wird das folgende Muster verwendet.

![Diagramm des Musters für dreieckige Patches](images/tripatch.png)

Rechteckige Patches verwenden das folgende Muster.

![Diagramm des Musters für rechteckige Patches](images/quadpatch.png)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



