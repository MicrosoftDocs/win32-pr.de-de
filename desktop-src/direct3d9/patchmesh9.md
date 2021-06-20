---
description: PatchMesh9 definiert ein durch Bézierpatches definiertes Gitternetz, einschließlich einer Liste von Scheitelpunkte und patches für das Gitternetz durch Indizierung im Scheitelpunktarray.
ms.assetid: 642ca513-c83e-4c6d-845c-0eaecc232728
title: PatchMesh9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811e593117f2ec57a4718ea8078d96bcea87e71f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404703"
---
# <a name="patchmesh9"></a>PatchMesh9

Definiert ein durch Bézierpatches definiertes Gitternetz. Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.

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
-   Degree: Grad der Variablen in der Kurvengleichung.
-   Basis: Basistyp einer hochwertigen Patchoberfläche.
-   nVertices: Anzahl der Scheitelzeichen.
-   sctices \[ nVertices \] : Array von Scheiteltices. Siehe [**Vektor**](vector.md).
-   nPatches: Anzahl der Patches.
-   patches \[ nPatches: \] Array von Patches. Weitere Informationen [**finden Sie unter Patchen von**](patch.md).
-   \[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden. Dadurch wird die Architektur erweiterbar.

Die Patches verwenden die Scheitelpunkte im Array von Scheitelpunkten als Kontrollpunkte für jeden Patch.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



