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
# <a name="fog-blending-direct3d-9"></a><span data-ttu-id="13cd6-103">Nebel Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="13cd6-103">Fog Blending (Direct3D 9)</span></span>

<span data-ttu-id="13cd6-104">Nebel Mischung bezieht sich auf die Anwendung des Nebel Faktors auf den Nebel und die Objekt Farben, um die endgültige Farbe zu schaffen, die in einer Szene angezeigt wird, wie in [Nebel Formeln (Direct3D 9)](fog-formulas.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="13cd6-104">Fog blending refers to the application of the fog factor to the fog and object colors to produce the final color that appears in a scene, as discussed in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="13cd6-105">Der D3DRS \_ fogenable-Rendering-Zustand steuert die Nebel Mischung.</span><span class="sxs-lookup"><span data-stu-id="13cd6-105">The D3DRS\_FOGENABLE render state controls fog blending.</span></span> <span data-ttu-id="13cd6-106">Legen Sie diesen Rendering-Zustand auf " **true** " fest, um eine Nebel Mischung zu aktivieren, wie im folgenden Beispielcode gezeigt</span><span class="sxs-lookup"><span data-stu-id="13cd6-106">Set this render state to **TRUE** to enable fog blending as shown in the following example code.</span></span> <span data-ttu-id="13cd6-107">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="13cd6-107">The default is **FALSE**.</span></span>


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



<span data-ttu-id="13cd6-108">Sie müssen die Nebel Mischung sowohl für Pixel Nebel als auch für Scheitelpunkt Nebel aktivieren.</span><span class="sxs-lookup"><span data-stu-id="13cd6-108">You must enable fog blending for both pixel fog and vertex fog.</span></span> <span data-ttu-id="13cd6-109">Weitere Informationen zur Verwendung dieser Arten von Nebel finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md) und [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="13cd6-109">For information about using these types of fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md) and [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13cd6-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13cd6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13cd6-111">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="13cd6-111">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



