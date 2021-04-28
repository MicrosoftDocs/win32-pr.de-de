---
description: 'FaceAdencyency: Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Netz Duplikate voneinander sind.'
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdencyency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090508"
---
# <a name="faceadjacency"></a>FaceAdencyency

Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Netz Duplikate voneinander sind. Duplikate ergeben sich, wenn sich ein Scheitelpunkt an einer Glättungsgruppe oder Materialgrenze befindet. Der Zweck dieser Vorlage besteht darin, dem Ladeprogramm zu ermöglichen, zu bestimmen, welche Scheitelpunkte mit unterschiedlichen Peripherieparametern tatsächlich die gleichen Scheitelpunkte im Modell sind. Bestimmte Anwendungen (z. B. Mesh-Vereinfachung) können diese Informationen nutzen.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Hierbei gilt:

-   nIndices: Anzahl der Indizes im Gitternetz.
-   indizes \[ nIndices: \] Array von Indizes.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



