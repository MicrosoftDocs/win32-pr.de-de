---
description: Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3d8232fe8c83358feb216acfb45a7877d7acb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338886"
---
# <a name="patchmesh9"></a>PatchMesh9

Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.

``` syntax
template PatchMesh9
{
    < B9EC94E1-B9A6-4251-BA18-94893F02C0EA >
    DWORD Type;
    DWORD Degree;
    DWORD Basis;
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
} 
```

Hierbei gilt:

-   Typ-patchmesh-Typ: Rechteck, Dreieck oder N-Patch.
-   Grad-Grad der Variablen in der Kurven Gleichung.
-   Der Grund für den Typ einer hochwertigen patchoberfläche.
-   nvertices-Anzahl der Scheitel Punkte.
-   Vertices \[ nvertices \] -Array von Vertices. Siehe [**Vektor**](vector.md).
-   npatches-Anzahl der Patches.
-   Patches \[ npatches \] -Array von Patches. Siehe [**Patch**](patch.md).
-   \[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden. Dadurch wird die Architektur erweiterbar.

Die Patches verwenden die Scheitel Punkte im Array von Vertices als Steuerungs Punkte für die einzelnen Patches.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



