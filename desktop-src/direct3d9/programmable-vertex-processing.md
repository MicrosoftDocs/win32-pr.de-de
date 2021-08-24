---
description: Bei Verwendung eines programmierten Vertex-Shaders werden die im Zielvertexpuffer aktualisierten Elemente vom Shaderfunktionsprogramm gesteuert.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Programmierbare Scheitelpunktverarbeitung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118590"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Programmierbare Scheitelpunktverarbeitung (Direct3D 9)

Bei Verwendung eines programmierten Vertex-Shaders werden die im Zielvertexpuffer aktualisierten Elemente vom Shaderfunktionsprogramm gesteuert. Wenn die Anwendung in eines der Zielvertexregister schreibt, wird das entsprechende Element innerhalb jedes Scheitelpunkts des Zielvertexpuffers aktualisiert. Elemente im Zielvertexpuffer, die nicht von der Anwendung in geschrieben werden, werden nicht geändert. [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) schlägt fehl, wenn die Anwendung in Elemente schreibt, die nicht im Zielvertexpuffer vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktpuffer](vertex-buffers.md)
</dt> </dl>

 

 
