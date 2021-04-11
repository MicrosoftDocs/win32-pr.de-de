---
description: Nebel Mischung bezieht sich auf die Anwendung des Nebel Faktors auf den Nebel und die Objekt Farben, um die endgültige Farbe zu schaffen, die in einer Szene angezeigt wird, wie in Nebel Formeln (Direct3D 9) erläutert.
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: Nebel Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa918715a7bbe37b200568a0a9098135c5558b0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123350"
---
# <a name="fog-blending-direct3d-9"></a>Nebel Mischung (Direct3D 9)

Nebel Mischung bezieht sich auf die Anwendung des Nebel Faktors auf den Nebel und die Objekt Farben, um die endgültige Farbe zu schaffen, die in einer Szene angezeigt wird, wie in [Nebel Formeln (Direct3D 9)](fog-formulas.md)erläutert. Der D3DRS \_ fogenable-Rendering-Zustand steuert die Nebel Mischung. Legen Sie diesen Rendering-Zustand auf " **true** " fest, um eine Nebel Mischung zu aktivieren, wie im folgenden Beispielcode gezeigt Der Standardwert ist **false**.


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



Sie müssen die Nebel Mischung sowohl für Pixel Nebel als auch für Scheitelpunkt Nebel aktivieren. Weitere Informationen zur Verwendung dieser Arten von Nebel finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md) und [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 



