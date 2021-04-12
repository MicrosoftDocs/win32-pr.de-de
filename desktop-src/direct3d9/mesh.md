---
description: Definiert ein einfaches Mesh. Das erste Array ist eine Liste von Scheitel Punkten, während das zweite Array die Gesichter des Netzes durch Indizierung in das vertexarray definiert.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Mesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480699"
---
# <a name="mesh"></a>Mesh

Definiert ein einfaches Mesh. Das erste Array ist eine Liste von Scheitel Punkten, während das zweite Array die Gesichter des Netzes durch Indizierung in das vertexarray definiert.

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

-   nvertices-Anzahl der Scheitel Punkte.
-   Array Vektor vertices \[ nvertices \] -Array von Vertices, jeweils vom Typ "Vector". Siehe [**Vektor**](vector.md).
-   ngesichter: Anzahl der Flächen.
-   Array meshface Gesichter \[ ngesichter \] -Array von Gesichtern, jeweils vom Typ "meshface". Siehe [**meshface**](meshface.md).
-   \[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden. Dadurch wird die Architektur erweiterbar. [**Material**](material.md) -und [**texturefilename**](texturefilename.md) -Vorlagen werden in der Regel verwendet.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



