---
description: 'VertexDuplicationIndices: Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Gitternetz dupliziert sind.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090178"
---
# <a name="vertexduplicationindices"></a>VertexDuplicationIndices

Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelungen im Gitternetz Duplikate voneinander sind. Duplikate ergeben sich, wenn sich ein Scheitelpunkt an einer Glättungsgruppe oder Materialgrenze befindet. Mit dieser Vorlage soll dem Lader ermöglicht werden, zu bestimmen, welche Scheitelpunkte, die verschiedene Peripherieparameter enthalten, tatsächlich dieselben Scheitelpunkte im Modell sind. Bestimmte Anwendungen (z. B. die Mesh-Vereinfachung) können diese Informationen nutzen.

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
-   Die Wertindizes n enthalten den Scheitelpunktindex, den Scheitelpunkt n im Vertexarray für das Gitternetz hätte, wenn keine \[ \] \[ \] Duplizierung aufgetreten wäre. Indizes in diesem Array, die identisch sind, weisen daher auf doppelte Scheitelungen hin.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



