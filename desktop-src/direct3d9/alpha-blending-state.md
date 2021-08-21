---
description: Der Alphawert einer Farbe steuert die Transparenz. Durch aktivieren des Alphablendings können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Alphablendingzustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4bd012340fae9e7597479d846d18db37c32d6f95a42118ba7444ad63a2e1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045208"
---
# <a name="alpha-blending-state-direct3d-9"></a>Alphablendingzustand (Direct3D 9)

Der Alphawert einer Farbe steuert die Transparenz. Durch aktivieren des Alphablendings können Farben, Materialien und Texturen auf einer Oberfläche mit Transparenz auf eine andere Oberfläche gemischt werden.

Weitere Informationen finden Sie unter [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) und [Texture Blending (Direct3D 9).](texture-blending.md)

In C++ geschriebene Anwendungen verwenden den [**D3DRS \_ ALPHABLENDENABLE-Renderzustand,**](./d3drenderstatetype.md) um alpha-Transparenzblending zu ermöglichen. Die Direct3D-API lässt viele Arten von Alphablending zu. Beachten Sie jedoch, dass die 3D-Hardware des Benutzers möglicherweise nicht alle blending-Zustände unterstützt, die von Direct3D zugelassen werden.

Die Art der Alphamischung hängt von den [**Renderzuständen D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) und **D3DRS \_ DESTBLEND** ab. Quell- und Zielblendzustände werden paarweise verwendet. Im folgenden Codebeispiel wird veranschaulicht, wie der Quellblendzustand auf D3DBLEND SRCCOLOR und der Zielmischungszustand auf \_ D3DBLEND \_ INVSRCCOLOR festgelegt ist.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



Das Ändern des Quell- und Zielmischungszuständes kann das Erscheinungsbild von Füllobjekten in einer versauenden oder verfeinerten Zustände verleihen. Wenn Ihre Anwendungsmodelle z. B. In einer komischen Umgebung Zustände für Quell- und Zielmischungen auf D3DBLEND ONE festlegen, wenn Ihre Anwendungsmodelle Z. B. Feldern, Feldern, Balken oder ähnlichen Bogenobjekten \_ ähneln.

Eine weitere Anwendung des Alphablendings ist die Steuerung der Beleuchtung in einer 3D-Szene, die auch als Lichtzuordnung bezeichnet wird. Wenn Sie den Quellmischungszustand auf D3DBLEND ZERO und den Zielmischungszustand auf \_ D3DBLEND SRCALPHA festlegen, wird eine Szene gemäß den Alphainformationen der \_ Quelle dunkler. Das Quellprimitive wird als Lichtkarte verwendet, die den Inhalt des Framepuffers skaliert, um ihn gegebenenfalls zu dunkler zu machen. Dies erzeugt eine monotone Lichtzuordnung.

Sie können eine Farblichtzuordnung erreichen, indem Sie den Alphablendingzustand der Quelle auf D3DBLEND ZERO und den Zielblendzustand auf \_ D3DBLEND \_ SRCCOLOR festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Renderzustände](render-states.md)
</dt> </dl>

 

 
