---
description: PatchMesh definiert ein Gitternetz, das von Bézierpatches definiert wird, einschließlich einer Liste von Scheitelpunkte und patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.
ms.assetid: vs|directx_sdk|~\patchmesh.htm
title: PatchMesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabb3846246c7fb76a7146baf0b30bd9730fe24b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404713"
---
# <a name="patchmesh"></a>PatchMesh

Definiert ein durch Bézierpatches definiertes Gitternetz. Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Patches für das Gitternetz durch Indizierung in das Scheitelpunktarray.

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

-   nVertices: Anzahl der Scheitelzeichen.
-   sctices \[ nVertices \] : Array von Scheiteltices. Siehe [**Vektor**](vector.md).
-   nPatches: Anzahl der Patches.
-   patches \[ nPatches: \] Array von Patches. Weitere Informationen [**finden Sie unter Patchen von**](patch.md).
-   \[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden. Dadurch wird die Architektur erweiterbar.

Die Patches verwenden die Scheitelpunkte im Array von Scheitelpunkten als Kontrollpunkte für jeden Patch. Dies ist eine Legacyvorlage. Die neueste Patch mesh-Vorlage ist [**PatchMesh9.**](patchmesh9.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



