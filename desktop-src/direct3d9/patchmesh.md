---
description: Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: Patchmesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcdefac9799736c796aef7cbb7222ab1942540d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520891"
---
# <a name="patchmesh"></a>Patchmesh

Definiert ein Mesh, das von Bézier-Patches definiert wird. Das erste Array ist eine Liste von Vertices, und das zweite Array definiert die Patches für das Mesh, indem es in das vertexarray indiziert wird.

``` syntax
template PatchMesh
{
    < D02C95CC-EDBA-4305-9B5D-1820D7704BBF >
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nPatches;
    array Patch patches[nPatches];
    [ ... ]
}
```

Hierbei gilt:

-   nvertices-Anzahl der Scheitel Punkte.
-   Vertices \[ nvertices \] -Array von Vertices. Siehe [**Vektor**](vector.md).
-   npatches-Anzahl der Patches.
-   Patches \[ npatches \] -Array von Patches. Siehe [**Patch**](patch.md).
-   \[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden. Dadurch wird die Architektur erweiterbar.

Die Patches verwenden die Scheitel Punkte im Array von Vertices als Steuerungs Punkte für die einzelnen Patches. Dies ist eine Legacy Vorlage. Die neueste patchmesh-Vorlage ist [**PatchMesh9**](patchmesh9.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



