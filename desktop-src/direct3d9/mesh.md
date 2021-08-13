---
description: Definiert ein einfaches Gitter. Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Gesichter des Gitters durch Indizierung in das Scheitelpunktarray.
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

Definiert ein einfaches Gitter. Das erste Array ist eine Liste von Scheitelpunkte, und das zweite Array definiert die Gesichter des Gitters durch Indizierung in das Scheitelpunktarray.

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

-   nVertices: Anzahl der Scheitelzeichen.
-   array Vector vertices \[ nVertices \] – Array von Scheitelungen, die jeweils vom Typ Vector sind. Siehe [**Vektor**](vector.md).
-   nFaces: Anzahl der Gesichter.
-   Array MeshFace faces \[ nFaces \] : Array von Gesichtern, die jeweils vom Typ MeshFace sind. Weitere Informationen [**finden Sie unter MeshFace**](meshface.md).
-   \[ ... \] – Hier kann eine beliebige X-Dateivorlage verwendet werden. Dadurch wird die Architektur erweiterbar. [**Material-**](material.md) [**und TextureFilename-Vorlagen**](texturefilename.md) werden in der Regel verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



