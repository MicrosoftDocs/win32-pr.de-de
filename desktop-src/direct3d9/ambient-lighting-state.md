---
description: Ambient Light umgibt Licht, das von allen Richtungen ausstrahlt. Informationen dazu, wie Direct3D Ambient Light verwendet, finden Sie unter Mathematik der Beleuchtung (Direct3D 9).
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: Umgebungs Beleuchtungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bd604941961f5b4abdb301d5c23efba9980791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127236"
---
# <a name="ambient-lighting-state-direct3d-9"></a><span data-ttu-id="69f8e-104">Umgebungs Beleuchtungs Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="69f8e-104">Ambient Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="69f8e-105">Ambient Light umgibt Licht, das von allen Richtungen ausstrahlt.</span><span class="sxs-lookup"><span data-stu-id="69f8e-105">Ambient light is surrounding light that radiates from all directions.</span></span> <span data-ttu-id="69f8e-106">Informationen dazu, wie Direct3D Ambient Light verwendet, finden Sie unter [Mathematik der Beleuchtung (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="69f8e-106">For information about how Direct3D uses ambient light, see [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="69f8e-107">Eine C++-Anwendung legt die Farbe der Umgebungsbeleuchtung fest, indem Sie die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode aufruft und den Enumerationswert D3DRS \_ Ambient als ersten Parameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="69f8e-107">A C++ application sets the color of ambient lighting by invoking the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and passing the enumerated value D3DRS\_AMBIENT as the first parameter.</span></span> <span data-ttu-id="69f8e-108">Der zweite Parameter ist ein Farbwert.</span><span class="sxs-lookup"><span data-stu-id="69f8e-108">The second parameter is a color value.</span></span> <span data-ttu-id="69f8e-109">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="69f8e-109">The default value is zero.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a><span data-ttu-id="69f8e-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69f8e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f8e-111">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="69f8e-111">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
