---
description: Gibt an, wie der Monitor, der zum Anzeigen einer Vollbildanwendung verwendet wird, gedreht wird.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: D3DDISPLAYROTATION-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363964"
---
# <a name="d3ddisplayrotation-enumeration"></a><span data-ttu-id="c9d68-103">D3DDISPLAYROTATION-Enumeration</span><span class="sxs-lookup"><span data-stu-id="c9d68-103">D3DDISPLAYROTATION enumeration</span></span>

<span data-ttu-id="c9d68-104">Gibt an, wie der Monitor, der zum Anzeigen einer Vollbildanwendung verwendet wird, gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="c9d68-104">Specifies how the monitor being used to display a full-screen application is rotated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9d68-105">Syntax</span></span>


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a><span data-ttu-id="c9d68-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="c9d68-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9d68-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION- \_ Identität**</span><span class="sxs-lookup"><span data-stu-id="c9d68-107"><span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION\_IDENTITY**</span></span>
</dt> <dd>

<span data-ttu-id="c9d68-108">Die Anzeige wird nicht gedreht.</span><span class="sxs-lookup"><span data-stu-id="c9d68-108">Display is not rotated.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**</span><span class="sxs-lookup"><span data-stu-id="c9d68-109"><span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION\_90**</span></span>
</dt> <dd>

<span data-ttu-id="c9d68-110">Die Anzeige wird um 90 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="c9d68-110">Display is rotated 90 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**</span><span class="sxs-lookup"><span data-stu-id="c9d68-111"><span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION\_180**</span></span>
</dt> <dd>

<span data-ttu-id="c9d68-112">Die Anzeige wird um 180 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="c9d68-112">Display is rotated 180 degrees.</span></span>

</dd> <dt>

<span data-ttu-id="c9d68-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**</span><span class="sxs-lookup"><span data-stu-id="c9d68-113"><span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION\_270**</span></span>
</dt> <dd>

<span data-ttu-id="c9d68-114">Die Anzeige wird um 270 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="c9d68-114">Display is rotated 270 degrees.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9d68-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9d68-115">Remarks</span></span>

<span data-ttu-id="c9d68-116">Diese Enumeration wird in " [**IDirect3D9Ex:: getadapterdisplaymodeex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex)", " [**IDirect3DDevice9Ex:: getdisplaymodeex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)" und " [**IDirect3DSwapChain9Ex:: getdisplaymodeex**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9d68-116">This enumeration is used in [**IDirect3D9Ex::GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex), and [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).</span></span>

<span data-ttu-id="c9d68-117">Anwendungen können die Monitor Drehung selbst mithilfe von [D3DPRESENTFLAG \_ noautorotate](d3dpresentflag.md)verarbeiten. in diesem Fall muss die Anwendung wissen, wie der Monitor gedreht wird, damit er das Rendering entsprechend anpassen kann.</span><span class="sxs-lookup"><span data-stu-id="c9d68-117">Applications may choose to handle monitor rotation themselves by using the [D3DPRESENTFLAG\_NOAUTOROTATE](d3dpresentflag.md), in which case, the application will need to know how the monitor is rotated so that it may adjust its rendering accordingly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d68-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9d68-118">Requirements</span></span>



| <span data-ttu-id="c9d68-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9d68-119">Requirement</span></span> | <span data-ttu-id="c9d68-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c9d68-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d68-121">Header</span><span class="sxs-lookup"><span data-stu-id="c9d68-121">Header</span></span><br/> | <dl> <span data-ttu-id="c9d68-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d68-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d68-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9d68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d68-124">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="c9d68-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




