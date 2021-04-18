---
description: Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: Vertexduplicationindizes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341086"
---
# <a name="vertexduplicationindices"></a>Vertexduplicationindizes

Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind. Dupliziert das Ergebnis, wenn sich ein Scheitelpunkt auf einer Glättungs Gruppe oder Material Grenze befindet. Der Zweck dieser Vorlage besteht darin, dem Lade Modul zu gestatten, zu bestimmen, welche Scheitel Punkte, die verschiedene Peripherie Parameter aufweisen, tatsächlich die gleichen vertexen im Modell sind. Bestimmte Anwendungen (z. b. die Mesh-Vereinfachung) können diese Informationen nutzen.

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

-   nindizes-Anzahl der Scheitelpunkt Indizes. Dies ist die Anzahl der Scheitel Punkte im Mesh.
-   noriginalvertices: Anzahl der Scheitel Punkte im Mesh, bevor eine Duplizierung erfolgt.
-   Die Wert Indizes \[ n enthalten \] den Vertexindex, den Vertex \[ n \] im Vertex-Array für das Mesh hätte hätten, wenn keine Duplizierung aufgetreten wäre. Indizes in diesem Array, die gleich sind, weisen auf doppelte Scheitel Punkte hin.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



