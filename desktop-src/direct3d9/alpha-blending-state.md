---
description: Der Alpha-Wert einer Farbe steuert seine Transparenz. Durch das Aktivieren von Alpha Blending können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Alpha Mischungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393122"
---
# <a name="alpha-blending-state-direct3d-9"></a>Alpha Mischungs Zustand (Direct3D 9)

Der Alpha-Wert einer Farbe steuert seine Transparenz. Durch das Aktivieren von Alpha Blending können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.

Weitere Informationen finden Sie unter [Alpha Textur blending (Direct3D 9)](alpha-texture-blending.md) und [Textur blending (Direct3D 9)](texture-blending.md).

In C++ geschriebene Anwendungen verwenden den [**D3DRS \_ AlphaBlendEnable**](./d3drenderstatetype.md) -Rendering-Status, um Alpha-Transparenz-Blending zu aktivieren. Die Direct3D-API ermöglicht viele Arten von Alpha Blending. Es ist jedoch wichtig zu beachten, dass die 3D-Hardware des Benutzers möglicherweise nicht alle Mischungs Zustände unterstützt, die von Direct3D zugelassen werden.

Der Typ der durchgeführten Alpha Mischung hängt von den [**D3DRS \_ srcblend**](./d3drenderstatetype.md) -und **D3DRS \_ destblend** -Rendering-Zuständen ab. Quell-und Ziel-Blend-Zustände werden paarweise verwendet. Im folgenden Codebeispiel wird veranschaulicht, wie der Source Blend-Status auf D3DBLEND \_ srccolor und der Ziel-Blend-Zustand auf D3DBLEND \_ invsrccolor festgelegt ist.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



Das Ändern der Quell-und Ziel-Blend-Zustände kann die Darstellung von selbst leuchtendes-Objekten in einer nebligen oder Dusty-Atmosphäre aufweisen. Wenn Ihre Anwendung z. b. in einer fernen-Umgebung Flammen modelliert, Felder, Plasma Balken oder ähnlich strahlende Objekte erzwingt, legen Sie den Quell-und den Ziel-Blend-Status auf D3DBLEND \_ One fest.

Eine andere Anwendung der Alpha Mischung ist die Steuerung der Beleuchtung in einer 3D-Szene, die auch als leichte Zuordnung bezeichnet wird. Wenn Sie den Source Blend-Status auf D3DBLEND \_ Zero und den Ziel-Blend-Zustand auf D3DBLEND \_ srcalpha festlegen, wird eine Szene entsprechend den Quell-Alpha Informationen dunkel. Der Quell primitive wird als eine Licht Zuordnung verwendet, die den Inhalt des Frame Puffers skaliert, um ihn bei Bedarf zu darfiltern. Dies erzeugt eine monochrome helle Zuordnung.

Sie können die Farb Füll Zuordnung erreichen, indem Sie den Quell-Alpha-Mischungs Zustand auf D3DBLEND \_ Zero und den Ziel-Blend-Zustand auf D3DBLEND \_ srccolor festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendering-Zustände](render-states.md)
</dt> </dl>

 

 
