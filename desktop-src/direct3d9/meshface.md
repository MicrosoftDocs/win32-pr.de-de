---
description: Wird von der Mesh-Vorlage verwendet, um die Gesichter eines Netzes zu definieren. Jedes Element des nfakevertexindices-Arrays verweist auf einen Mesh-Vertex, der zum Erstellen der Vorderseite verwendet wird.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: Meshface
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123445"
---
# <a name="meshface"></a>Meshface

Wird von der [**Mesh**](mesh.md) -Vorlage verwendet, um die Gesichter eines Netzes zu definieren. Jedes Element des nfakevertexindices-Arrays verweist auf einen Mesh-Vertex, der zum Erstellen der Vorderseite verwendet wird.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Hierbei gilt:

-   nfakevertexindices: Anzahl der Indizes.
-   Array DWORD Facetten Index \[ nfakevertexindices \] -Array von Indizes.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



