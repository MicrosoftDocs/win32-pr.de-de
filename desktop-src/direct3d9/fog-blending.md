---
description: Die Mischung von Farben bezieht sich auf die Anwendung des Füllfaktors auf die Farben für Diess und Objekte, um die endgültige Farbe zu erzeugen, die in einer Szene angezeigt wird, wie unter Formeln für Formeln (Direct3D 9) erläutert.
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Blending für Überblendung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60f3402daf71a3fce14af936334c3d96e928d3469452eafb94d139594bb0b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894020"
---
# <a name="fog-blending-direct3d-9"></a>Blending für Überblendung (Direct3D 9)

Die Kombination von Farben bezieht sich auf die Anwendung des Füllfaktors auf die Farben für Diess und Objekte, um die endgültige Farbe zu erzeugen, die in einer Szene angezeigt wird, wie unter Formeln für Formeln [(Direct3D 9)](fog-formulas.md)erläutert. Der \_ D3DRS-Renderzustand BERDEBAR steuert blending. Legen Sie diesen Renderzustand auf **TRUE fest,** um blending zu aktivieren, wie im folgenden Beispielcode gezeigt. Der Standardwert ist **FALSE.**


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



Sie müssen blending sowohl für Pixel- als auch für Scheitelpunktverblendung aktivieren. Informationen zur Verwendung dieser Typen von 2017 finden Sie unter [Pixel Pixel (Direct3D 9)](pixel-fog.md) und [Vertex- (Direct3D 9).](vertex-fog.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typen von Typen](fog-types.md)
</dt> </dl>

 

 



