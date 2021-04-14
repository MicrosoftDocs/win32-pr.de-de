---
description: Gibt Scheitelpunkt Farben für ein Mesh an, anstatt ein Material pro Gesicht oder pro Mesh anzuwenden.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: Meshvertexcolors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392474"
---
# <a name="meshvertexcolors"></a>Meshvertexcolors

Gibt Scheitelpunkt Farben für ein Mesh an, anstatt ein Material pro Gesicht oder pro Mesh anzuwenden.

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

Hierbei gilt:

-   nvertexcolors: Anzahl der Farben. Dies entspricht der Anzahl der Scheitel Punkte im Mesh.
-   Array indexcolor vertexcolors \[ nvertexcolors \] -Array von indizierten Farben. Siehe [**indexedcolor**](indexedcolor.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



