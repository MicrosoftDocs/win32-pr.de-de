---
description: Bei der Vertex-Optimierung werden zwei vom Benutzer bereitgestellte Positionen (oder Normalitäten) kombiniert.
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8486f53e4eb1a3a003b15255baeb50d30f0ed205f4259625d7d66ba33e8274c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519221"
---
# <a name="vertex-tweening-direct3d-9"></a>Vertex-Tweening (Direct3D 9)

Bei der Vertex-Optimierung werden zwei vom Benutzer bereitgestellte Positionen (oder Normalitäten) kombiniert. Die Optimierung schließen sich gegenseitig von Scheitelpunktmischungen mit Gewichtungen aus. Die Optimierung wird vor der Beleuchtung und dem Clipping durchgeführt und durch Festlegen von D3DRS \_ VERTEXBLEND auf D3DVBF \_ TWEENING aktiviert. Die resultierende Scheitelpunktposition wird berechnet durch:


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



Der gleiche Ansatz wird zum Berechnen von Normalitäten verwendet. Weitere Informationen finden Sie unter [Using Vertex Tweening (Direct3D 9) (Verwenden von Vertex-Tweening (Direct3D 9)).](using-vertex-tweening.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geometriemischung](geometry-blending.md)
</dt> </dl>

 

 



