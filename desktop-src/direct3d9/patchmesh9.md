---
description: PatchMesh9 definiert ein durch Bézierpatches definiertes Gitternetz, einschließlich einer Liste von Scheitelpunkten und patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20216bcfa33c3e3ef36dea999a6fef10384719254f4874a1da3907aa02551a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798536"
---
# <a name="patchmesh9"></a>PatchMesh9

Definiert ein durch Bézierpatches definiertes Gitternetz. Das erste Array ist eine Liste von Scheitelpunkten, und das zweite Array definiert die Patches für das Gitternetz, indem es in das Scheitelpunktarray indiziert wird.

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

-   Typ: Patchgitternetztyp: Rechteck, Dreieck oder N-Patch.
-   Degree: Der Grad der Variablen in der Kurvengleichung.
-   Basis: Basistyp einer Patchoberfläche mit hoher Ordnung.
-   nVertices: Anzahl der Scheitelpunkte.
-   Scheitelpunkte \[ nVertices: \] Array von Scheitelpunkten. Weitere Informationen finden Sie unter [**Vektor**](vector.md).
-   nPatches: Anzahl der Patches.
-   patches \[ nPatches \] : Array von Patches. Weitere Informationen finden Sie unter [**Patchen**](patch.md)von .
-   \[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden. Dadurch wird die Architektur erweiterbar.

Die Patches verwenden die Scheitelpunkte im Array von Scheitelpunkten als Kontrollpunkte für jeden Patch.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



