---
description: Diese Vorlage wird pro Mesh instanziiert.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: Skingewichtungen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520883"
---
# <a name="skinweights"></a>Skingewichtungen

Diese Vorlage wird pro Mesh instanziiert. Innerhalb eines Netzes wird eine Sequenz von n Instanzen dieser Vorlage angezeigt, wobei n die Anzahl der Knochen (X-Datei Rahmen) ist, die die Scheitel Punkte im Mesh beeinflussen. Jede Instanz der Vorlage definiert im Grunde den Einfluss eines bestimmten Knochen im Mesh. Es gibt eine Liste der Scheitelpunkt Indizes und eine entsprechende Liste von Gewichtungen.

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

-   Der Name des Knochens, dessen Auswirkung definiert wird, ist transformnodename, und ngewichtet ist die Anzahl der Scheitel Punkte, die von diesem Knochen betroffen sind.
-   Die Scheitel Punkte, die von diesem Knochen beeinflusst werden, sind in vertexindizes enthalten, und die Gewichtungen für die einzelnen Scheitel Punkte, die von diesem Knochen beeinflusst werden, sind in Gewichtungen enthalten.
-   Matrix matrixoffset wandelt die Gitter Scheitel Punkte in den Raum des Knochens um. Bei der Verkettung mit der Transformation des Streams werden dadurch die Raumkoordinaten des Netzes bereitstellt, die vom Knochen betroffen sind. Siehe [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



