---
description: Ruft die Flags ab, die beim Erstellen eines Microsoft DirectX Graphics Infrastructure (DXGI)-Objekts verwendet wurden.
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'IDXGIFactory3:: getkreationflags-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123325"
---
# <a name="idxgifactory3getcreationflags-method"></a><span data-ttu-id="a51b0-103">IDXGIFactory3:: getkreationflags-Methode</span><span class="sxs-lookup"><span data-stu-id="a51b0-103">IDXGIFactory3::GetCreationFlags method</span></span>

<span data-ttu-id="a51b0-104">Ruft die Flags ab, die beim Erstellen eines Microsoft DirectX Graphics Infrastructure (DXGI)-Objekts verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a51b0-104">Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.</span></span>

## <a name="syntax"></a><span data-ttu-id="a51b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a51b0-105">Syntax</span></span>


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a><span data-ttu-id="a51b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a51b0-106">Parameters</span></span>

<span data-ttu-id="a51b0-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a51b0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a51b0-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a51b0-108">Return value</span></span>

<span data-ttu-id="a51b0-109">Die erstellungsflags.</span><span class="sxs-lookup"><span data-stu-id="a51b0-109">The creation flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="a51b0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a51b0-110">Remarks</span></span>

<span data-ttu-id="a51b0-111">Die **getkreationflags** -Methode gibt Flags zurück, die an [**die CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) -Funktion übergeben wurden, oder wurde implizit von " [**kreatedxgifactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)", " [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)", " [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)" oder " [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a51b0-111">The **GetCreationFlags** method returns flags that were passed to the [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) function, or were implicitly constructed by [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice), or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="see-also"></a><span data-ttu-id="a51b0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a51b0-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a51b0-113">**IDXGIFactory3**</span><span class="sxs-lookup"><span data-stu-id="a51b0-113">**IDXGIFactory3**</span></span>](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
