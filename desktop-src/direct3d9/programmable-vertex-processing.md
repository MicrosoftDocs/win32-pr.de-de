---
description: Wenn Sie einen programmierten Vertex-Shader verwenden, werden die Elemente, die im Ziel Vertex-Puffer aktualisiert werden, vom Shader-Funktionsprogramm gesteuert.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Programmierbare Vertex-Verarbeitung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344794"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Programmierbare Vertex-Verarbeitung (Direct3D 9)

Wenn Sie einen programmierten Vertex-Shader verwenden, werden die Elemente, die im Ziel Vertex-Puffer aktualisiert werden, vom Shader-Funktionsprogramm gesteuert. Wenn die Anwendung in eines der Ziel-Vertex-Register schreibt, wird das entsprechende Element in jedem Scheitelpunkt des Ziel Vertex-Puffers aktualisiert. Elemente im Ziel Vertex-Puffer, auf die nicht von der Anwendung geschrieben wird, werden nicht geändert. [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) schlägt fehl, wenn die Anwendung in Elemente schreibt, die nicht im Ziel Vertex-Puffer vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
