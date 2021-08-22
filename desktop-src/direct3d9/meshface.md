---
description: Wird von der Mesh-Vorlage verwendet, um die Gesichter eines Gitters zu definieren. Jedes Element des nFaceVertexIndices-Arrays verweist auf einen Gittervertex, der zum Erstellen des Gesichts verwendet wird.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: MeshFace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ea35d1db9e33644638455bc42cc2cbef320f748d96b086037dea6f10607dbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563530"
---
# <a name="meshface"></a>MeshFace

Wird von der [**Mesh-Vorlage**](mesh.md) verwendet, um die Gesichter eines Gitternetzes zu definieren. Jedes Element des nFaceVertexIndices-Arrays verweist auf einen Gittervertex, der zum Erstellen des Gesichts verwendet wird.

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

Hierbei gilt:

-   nFaceVertexIndices: Anzahl der Indizes.
-   array DWORD faceVertexIndices \[ nFaceVertexIndices \] – Array von Indizes.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



