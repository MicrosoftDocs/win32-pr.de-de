---
description: Polygone, die in Ihrem 3D-Raum koplanar sind, können so dargestellt werden, als wären sie nicht koplanar, indem sie jeweils einen Z-Bias hinzufügen.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Tiefenabweichung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc99d606a561fd6f4eec412774ce53d9b5dd5e62c7f50b118a4e90a88664a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523810"
---
# <a name="depth-bias-direct3d-9"></a>Tiefenabweichung (Direct3D 9)

Polygone, die in Ihrem 3D-Raum koplanar sind, können so dargestellt werden, als wären sie nicht koplanar, indem sie jeweils einen Z-Bias hinzufügen. Dies ist eine Technik, die häufig verwendet wird, um sicherzustellen, dass Schatten in einer Szene ordnungsgemäß angezeigt werden. Beispielsweise hat ein Schatten auf einer Wand wahrscheinlich den gleichen Tiefenwert wie die Wand. Wenn Sie zuerst die Wand und dann den Schatten rendern, ist der Schatten möglicherweise nicht sichtbar, oder Tiefenartefakte sind möglicherweise sichtbar. Sie können die Reihenfolge umkehren, in der Sie die coplanaren Objekte rendern, um den Effekt umzukehren. Tiefenartefakte sind jedoch weiterhin wahrscheinlich.

Eine Anwendung kann sicherstellen, dass koplanare Polygone ordnungsgemäß gerendert werden, indem den Z-Werten, die das System beim Rendern der Sätze von coplanaren Polygonen verwendet, ein Voreingenommenheit hinzugefügt wird. Um einer Gruppe von Polygonen einen Z-Bias hinzuzufügen, rufen Sie die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) unmittelbar vor dem Rendern auf, legen Sie den *State-Parameter* auf D3DRS \_ DEPTHBIAS und den *Value-Parameter* auf einen geeigneten float-Wert fest (ein geeigneter Wert kann z. B. von -1.0 bis 1.0 sein). Um diesen Wert an **SetRenderState** zu übergeben, müssen Sie auch den Wert in ein **DWORD-Wert** umbenennen. Ein höherer Z-Bias-Wert erhöht die Wahrscheinlichkeit, dass die von Ihnen gerenderten Polygone sichtbar sind, wenn sie mit anderen koplanaren Polygonen angezeigt werden.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



dabei ist m die maximale Tiefenpiste des gerenderten Dreiecks.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Die Einheiten für den \_ D3DRS DEPTHBIAS- und D3DRS-RENDERzuständeN \_ VOMCALEDEPTHBIAS hängen davon ab, ob Z-Pufferung oder W-Pufferung aktiviert ist. Die Anwendung muss geeignete Werte bereitstellen.

Die Voreingenommenheit wird auf keine Linie und keinen Punktprimitiven angewendet. Diese Voreingenommenheit muss jedoch auf Dreiecke angewendet werden, die im Wireframe-Modus gezeichnet werden.


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

[Pixelpipeline](pixel-pipeline.md)
</dt> </dl>

 

 
