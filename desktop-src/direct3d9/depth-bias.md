---
description: Polygone, die in Ihrem 3D-Raum Coplanar sind, können so gestaltet werden, als wären Sie nicht durch Hinzufügen eines z-Bias zu jedem.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Tiefen Abweichung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481563"
---
# <a name="depth-bias-direct3d-9"></a>Tiefen Abweichung (Direct3D 9)

Polygone, die in Ihrem 3D-Raum Coplanar sind, können so gestaltet werden, als wären Sie nicht durch Hinzufügen eines z-Bias zu jedem. Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden. Beispielsweise hat ein Schatten auf einer Wand wahrscheinlich denselben tiefen Wert wie die Wand. Wenn Sie die Wand zuerst und dann den Schatten darstellen, ist der Schatten möglicherweise nicht sichtbar, oder es sind keine tiefen Artefakte sichtbar. Sie können die Reihenfolge, in der Sie die Coplanar-Objekte renden, umkehren, um den Effekt umzukehren, aber tiefe Artefakte sind immer noch wahrscheinlich.

Eine Anwendung kann sicherstellen, dass Coplanar-Polygone ordnungsgemäß gerendert werden, indem Sie den z-Werten, die das System beim Rendern der Mengen von Coplanar-Polygonen verwendet, einen Bias hinzufügen. Zum Hinzufügen eines z-Bias zu einem Satz von Polygonen Aufrufen der [**IDirect3DDevice9:: btrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode direkt vor dem Rendern, Festlegen des *State* -Parameters auf D3DRS \_ depthbias und des *value* -Parameters auf einen passenden float-Wert (z. b. kann ein geeigneter Wert von-1,0 bis 1,0 sein). um diesen Wert an "* **Trend User State**" zu übergeben, müssen Sie auch den Wert in ein **DWORD** umwandeln Ein höherer z-Bias-Wert erhöht die Wahrscheinlichkeit, dass die von Ihnen dargestellten Polygone sichtbar sind, wenn Sie mit anderen Coplanar-Polygonen angezeigt werden.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



wobei m der maximale tiefen Rand des gerenderten Dreiecks ist.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Die Einheiten für die \_ Rendering-Zustände D3DRS depthbias und D3DRS \_ slopescaledepthbias sind davon abhängig, ob z-Pufferung oder w-Pufferung aktiviert ist. Die Anwendung muss geeignete Werte bereitstellen.

Der Bias wird nicht auf Zeilen-und Punkt primitive angewendet. Dieser Bias muss jedoch auf Dreiecke angewendet werden, die im Draht Modell-Modus gezeichnet werden.


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
