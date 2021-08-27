---
description: Definiert einen B&\# 233;Zier-Steuerelementpatch. Das -Array definiert die Steuerungspunkte für den Patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f57ac0cec68a1e8d1651c0e6ad2aabde6f1f6b949b085aa0dc35bd6e02c82a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118629"
---
# <a name="patch"></a>Patch

Definiert einen Bézier-Steuerelementpatch. Das -Array definiert die Steuerungspunkte für den Patch.

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

Hierbei gilt:

-   nControlIndices: Anzahl der Kontrollpunktindizes.
-   array DWORD controlIndices \[ nControlIndices \] : Array von Steuerelementpunktindizes.

Der Typ des Patches wird durch die Anzahl der Kontrollpunkte definiert, wie in der folgenden Tabelle dargestellt.



| Anzahl der Kontrollpunkte | type                              |
|--------------------------|-----------------------------------|
| 10                       | Kubischer dreieckiger Bézierpatch     |
| 15                       | Quartic Bézier triangular patch (Dreieckspatch für Quartic Bézier)   |
| 16                       | Kubischer Bézier-Quad-Rechteckpatch |



 

Die Reihenfolge der Kontrollpunkte wird in einem Kästchenmuster angegeben, wie in den folgenden Diagrammen für dreieckige und rechteckige Patches dargestellt.

Für dreieckige Patches wird das folgende Muster verwendet.

![Diagramm des Musters für dreieckige Patches](images/tripatch.png)

Rechteckige Patches verwenden das folgende Muster.

![Diagramm des Musters für rechteckige Patches](images/quadpatch.png)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



