---
description: Vertex-Tweening kombiniert zwei vom Benutzer bereitgestellte Positionen (oder normale).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213925"
---
# <a name="vertex-tweening-direct3d-9"></a>Vertex-Tweening (Direct3D 9)

Vertex-Tweening kombiniert zwei vom Benutzer bereitgestellte Positionen (oder normale). Das twiening schließt sich gegenseitig aus der Vertex-Mischung mit Gewichtungen aus. Das twipping erfolgt vor Beleuchtung und Clipping und wird durch Festlegen von D3DRS \_ vertexblend auf D3DVBF \_ Tweening ermöglicht. Die resultierende Scheitelpunkt Position wird berechnet durch:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Der gleiche Ansatz wird für die Berechnung von normalen verwendet. Weitere Informationen finden Sie unter [Verwenden der Vertex-Tweening (Direct3D 9)](using-vertex-tweening.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometrie Mischung](geometry-blending.md)
</dt> </dl>

 

 



