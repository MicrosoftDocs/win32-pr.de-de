---
description: Wird in einem Mesh-Objekt verwendet, um anzugeben, welches Material für welche Gesichter gilt. Der nmaterials-Member gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: Meshmateriallist
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339645"
---
# <a name="meshmateriallist"></a>Meshmateriallist

Wird in einem Mesh-Objekt verwendet, um anzugeben, welches Material für welche Gesichter gilt. Der nmaterials-Member gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

Hierbei gilt:

-   nmaterials: ein DWORD. Die Anzahl der Materialien.
-   nfakeindexes: ein DWORD. Die Anzahl der Indizes.
-   fakeindexes \[ nfakeindexes \] : ein Array von DWords, das die Gesichts Indizes enthält.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



