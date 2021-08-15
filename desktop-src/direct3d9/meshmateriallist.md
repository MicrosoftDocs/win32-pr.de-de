---
description: Wird in einem Gittermodellobjekt verwendet, um anzugeben, welches Material für welche Gesichter gilt. Das Element nMaterials gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798786"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Wird in einem Gittermodellobjekt verwendet, um anzugeben, welches Material für welche Gesichter gilt. Das Element nMaterials gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.

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

-   nMaterials : Ein DWORD. Die Anzahl der Materialien.
-   nFaceIndexes: Ein DWORD. Die Anzahl der Indizes.
-   faceIndexes \[ nFaceIndexes: \] Ein Array von DWORDs, die die Gesichtsindizes enthalten.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



