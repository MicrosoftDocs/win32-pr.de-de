---
description: Diese Vorlage wird pro Gitternetz instanziiert.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627910"
---
# <a name="skinweights"></a>SkinWeights

Diese Vorlage wird pro Gitternetz instanziiert. Innerhalb eines Gitternetzes wird eine Sequenz von n Instanzen dieser Vorlage angezeigt, wobei n die Anzahl von Bildern (X Dateirahmen) ist, die die Scheitelpunkte im Netz beeinflussen. Jede Instanz der Vorlage definiert im Grunde den Einfluss eines bestimmten Gitters auf das Netz. Es gibt eine Liste der Scheitelpunktindizes und eine entsprechende Liste von Gewichtungen.

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

Hierbei gilt:

-   Der Name der Mandanten, deren Einfluss definiert wird, ist transformNodeName, und nWeights ist die Anzahl der Scheitelpunkte, die von diesem Gitter betroffen sind.
-   Die von diesem Maß beeinflussten Scheitelpunkte sind in vertexIndices enthalten, und die Gewichtungen für die einzelnen Scheitelpunkte, die von diesem Gitter beeinflusst werden, sind in Gewichtungen enthalten.
-   Die MatrixmatrixOffset transformiert die Gittervertices in den Raum des Gitters. Bei Verkettung mit der Transformation des Glanzes stellt dies die Raumkoordinaten des Gitternetzes bereit, die von der Brille betroffen sind. Siehe [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



