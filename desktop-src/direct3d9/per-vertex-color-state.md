---
description: Die Direct3D-Beleuchtungs-Engine kann bei der Durchführung der Beleuchtung Daten pro Scheitelpunkt Farbe verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex Farben Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392347"
---
# <a name="per-vertex-color-state-direct3d-9"></a>Per-Vertex Farben Zustand (Direct3D 9)

Die Direct3D-Beleuchtungs-Engine kann bei der Durchführung der Beleuchtung Daten pro Scheitelpunkt Farbe verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind. Dies erfolgt durch Aktivieren des folgenden Rendering-Status:


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



Wenn die pro-Vertex-Farbe aktiviert ist, können Anwendungen die Quelle konfigurieren, von der das System Farbinformationen für einen Scheitelpunkt abruft. Die "D3DRS \_ AmbientMaterialSource"-, "D3DRS \_ DiffuseMaterialSource"-, "D3DRS \_ emissivematerialsource"-und "D3DRS \_ SpecularMaterialSource"-Darstellung steuern die Umgebungs-, diffusen, emissive-bzw. Glanz Farben-Komponenten Quellen. Jeder Status kann auf Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -enumerierten Typs festgelegt werden, der Konstanten definiert, die das System anweisen, das aktuelle Material, die diffuse Farbe oder die Glanz Farbe als Quelle für die angegebene Farbkomponente zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 
