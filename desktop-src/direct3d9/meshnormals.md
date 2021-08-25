---
description: Definiert Normals für ein Gitternetz.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a261dd8dbd46cf26116657b983eca4f693603869a80bf2fb110c0f165221ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846460"
---
# <a name="meshnormals"></a>MeshNormals

Definiert Normals für ein Gitternetz. Das erste Array von Vektoren sind die normalen Vektoren selbst, und das zweite Array ist ein Array von Indizes, die angeben, welche Normalwerte auf ein bestimmtes Gesicht angewendet werden sollen. Der Wert des nFaceNormals-Members sollte der Anzahl der Gesichter in einem Gitternetz entspricht.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Hierbei gilt:

-   nNormale: Anzahl der Normalzahlen.
-   array Vector normals \[ nNormals \] : Array von Normals. Siehe [**Vektor**](vector.md).
-   nFaceNormals: Anzahl der Gesichtsnormale.
-   Array MeshFace faceNormals \[ nFaceNormals \] – Array von Gitternetz-Gesichtsnormalen. Weitere Informationen [**finden Sie unter MeshFace**](meshface.md).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



