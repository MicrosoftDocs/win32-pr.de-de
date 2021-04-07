---
title: D1112 Gerät muss DX11 sein
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: Das der DXGI-Oberfläche zugeordnete Gerät muss ein D3D11-Gerät sein.
keywords:
- D1112 Gerät muss DX11 sein Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104038700"
---
# <a name="d1112-device-must-be-dx11"></a><span data-ttu-id="59df1-104">D1112: das Gerät muss DX11 sein.</span><span class="sxs-lookup"><span data-stu-id="59df1-104">D1112: Device Must Be DX11</span></span>

<span data-ttu-id="59df1-105">Das der DXGI-Oberfläche zugeordnete Gerät muss ein D3D11-Gerät sein.</span><span class="sxs-lookup"><span data-stu-id="59df1-105">The device associated with the DXGI surface must be a D3D11 device.</span></span>



|             |         |
|-------------|---------|
| <span data-ttu-id="59df1-106">Fehlerstufe</span><span class="sxs-lookup"><span data-stu-id="59df1-106">Error Level</span></span> | <span data-ttu-id="59df1-107">Warnung</span><span class="sxs-lookup"><span data-stu-id="59df1-107">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="59df1-108">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="59df1-108">Possible Causes</span></span>

<span data-ttu-id="59df1-109">Es wurde versucht, das " [**featedxgisurfacerendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) " mit einer DXGI-Oberfläche zu verwenden, die von einem nicht-Direct3D11-Gerät erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="59df1-109">There was an attempt to use the [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) with a DXGI surface created by a non-Direct3D11 device.</span></span>

 

 




