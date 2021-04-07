---
description: Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: Facefaceency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745569"
---
# <a name="faceadjacency"></a>Facefaceency

Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind. Dupliziert das Ergebnis, wenn sich ein Scheitelpunkt auf einer Glättungs Gruppe oder Material Grenze befindet. Der Zweck dieser Vorlage besteht darin, dem Lade Modul zu gestatten, zu bestimmen, welche Scheitel Punkte, die verschiedene Peripherie Parameter aufweisen, tatsächlich die gleichen vertexen im Modell sind. Bestimmte Anwendungen (z. b. die Mesh-Vereinfachung) können diese Informationen nutzen.

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

Hierbei gilt:

-   nindizes: Anzahl der Indizes im Mesh.
-   Indizes \[ nindizes \] -Array von Indizes.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



