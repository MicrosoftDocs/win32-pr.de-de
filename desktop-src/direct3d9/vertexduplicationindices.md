---
description: 'VertexDuplicationIndices: Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Gitternetz dupliziert sind.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ac9b43e0aa05d75727e24bb4677ef0b21fcb41366800185551c48f5fb76f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290335"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelungen im Gitternetz Duplikate voneinander sind. Duplikate ergeben sich, wenn sich ein Scheitelpunkt an einer Glättungsgruppe oder Materialgrenze befindet. Mit dieser Vorlage soll dem Lader ermöglicht werden, zu bestimmen, welche Scheitelpunkte, die unterschiedliche Peripherieparameter enthalten, tatsächlich dieselben Scheitelpunkte im Modell sind. Bestimmte Anwendungen (z. B. die Mesh-Vereinfachung) können diese Informationen nutzen.

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

Hierbei gilt:

-   nIndices : Anzahl der Scheitelpunktindizes. Dies ist die Anzahl der Scheitelzeichen im Gitternetz.
-   nOriginalVertices: Anzahl der Scheitelzeichen im Netz, bevor dupliziert wird.
-   Die Wertindizes n enthalten den Scheitelpunktindex, den Scheitelpunkt n im Scheitelpunktarray für das Gitternetz hätte, wenn keine \[ \] \[ \] Duplizierung aufgetreten wäre. Indizes in diesem Array, die identisch sind, weisen daher auf doppelte Scheitelungen hin.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



