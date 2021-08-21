---
description: Das Direct3D-Beleuchtungsmodul kann beim Durchführen der Beleuchtung scheitelpunktbezogene Farbdaten verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex Farbzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6efd227c64785f7399ae3ba56d4623342c0910d901c3cfc404fc4a37f0d233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727985"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex Farbzustand (Direct3D 9)

Das Direct3D-Beleuchtungsmodul kann beim Durchführen der Beleuchtung scheitelpunktbezogene Farbdaten verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind. Aktivieren Sie hierzu den folgenden Renderzustand:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Wenn die Farbe pro Scheitelpunkt aktiviert ist, können Anwendungen die Quelle konfigurieren, aus der das System Farbinformationen für einen Scheitelpunkt abruft. Die Renderzustände D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE und D3DRS \_ SPECULARMATERIALSOURCE steuern die Ambient-, Diffuse-, Emissive- und Specular Color-Komponentenquellen. Jeder Zustand kann auf Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps**](./d3dmaterialcolorsource.md) festgelegt werden, der Konstanten definiert, die das System anweisen, das aktuelle Material, die diffuse Farbe oder die Glanzfarbe als Quelle für die angegebene Farbkomponente zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
