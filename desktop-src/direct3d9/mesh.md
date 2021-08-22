---
description: Definiert ein einfaches Gitternetz. Das erste Array ist eine Liste von Scheitelpunkten, und das zweite Array definiert die Gesichter des Gitternetzes, indem es in das Scheitelpunktarray indiziert wird.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Mesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce4cf6fb6a3eee3417a7d0fe1594164c1e22df9d118f4f995955f8070fc015
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240740"
---
# <a name="mesh"></a>Mesh

Definiert ein einfaches Gitternetz. Das erste Array ist eine Liste von Scheitelpunkten, und das zweite Array definiert die Gesichter des Gitternetzes, indem es in das Scheitelpunktarray indiziert wird.

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

Hierbei gilt:

-   nVertices: Anzahl der Scheitelpunkte.
-   array Vector vertices \[ nVertices \] : Array von Scheitelpunkten, jeder vom Typ Vector. Weitere Informationen finden Sie unter [**Vektor**](vector.md).
-   nFaces: Anzahl von Gesichtern.
-   array MeshFace faces \[ nFaces \] : Array von Gesichtern vom Typ MeshFace. Weitere Informationen finden Sie unter [**MeshFace**](meshface.md).
-   \[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden. Dadurch wird die Architektur erweiterbar. [**Material-**](material.md) und [**TextureFilename-Vorlagen**](texturefilename.md) werden in der Regel verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



