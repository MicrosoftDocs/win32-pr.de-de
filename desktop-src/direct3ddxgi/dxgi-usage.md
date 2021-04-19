---
description: Flags für Optionen zur Oberfläche und Ressourcen Erstellung.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353712"
---
# <a name="dxgi_usage"></a><span data-ttu-id="afd3c-103">DXGI- \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="afd3c-103">DXGI\_USAGE</span></span>

<span data-ttu-id="afd3c-104">Flags für Optionen zur Oberfläche und Ressourcen Erstellung.</span><span class="sxs-lookup"><span data-stu-id="afd3c-104">Flags for surface and resource creation options.</span></span>



| <span data-ttu-id="afd3c-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="afd3c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="afd3c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afd3c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <span data-ttu-id="afd3c-107"><dt>**DXGI \_ Verwendungs \_ Hintergrund \_ Puffer**</dt> <dt>1L <<  (2 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-107"><dt>**DXGI\_USAGE\_BACK\_BUFFER**</dt> <dt>1L << (2 + 4)</dt></span></span> </dl>                             | <span data-ttu-id="afd3c-108">Die-Oberfläche oder-Ressource wird als Hintergrund Puffer verwendet.</span><span class="sxs-lookup"><span data-stu-id="afd3c-108">The surface or resource is used as a back buffer.</span></span> <span data-ttu-id="afd3c-109">Sie müssen den **DXGI- \_ Verwendungs \_ Hintergrund \_ Puffer** nicht übergeben, wenn Sie eine SwapChain erstellen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-109">You don’t need to pass **DXGI\_USAGE\_BACK\_BUFFER** when you create a swap chain.</span></span> <span data-ttu-id="afd3c-110">Sie können jedoch ermitteln, ob eine Ressource zu einer Swapkette gehört, wenn Sie [**idxgiresource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) aufrufen und den **DXGI- \_ Verwendungs-Back- \_ \_ Puffer** abrufen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-110">But you can determine whether a resource belongs to a swap chain when you call [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) and get **DXGI\_USAGE\_BACK\_BUFFER**.</span></span><br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <span data-ttu-id="afd3c-111"><dt>**DXGI \_ Verwendungs \_ verwerfen \_ bei der \_ aktuellen**</dt> <dt>1L- <<  (5 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-111"><dt>**DXGI\_USAGE\_DISCARD\_ON\_PRESENT**</dt> <dt>1L << (5 + 4)</dt></span></span> </dl>       | <span data-ttu-id="afd3c-112">Dieses Flag ist nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-112">This flag is for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <span data-ttu-id="afd3c-113"><dt>**DXGI \_ Verwendung \_ \_**</dt> Schreib geschützter <dt>1L- <<  (4 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-113"><dt>**DXGI\_USAGE\_READ\_ONLY**</dt> <dt>1L << (4 + 4)</dt></span></span> </dl>                                   | <span data-ttu-id="afd3c-114">Verwenden Sie die-Oberfläche oder-Ressource nur zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-114">Use the surface or resource for reading only.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <span data-ttu-id="afd3c-115"><dt>**DXGI \_ \_Ausgabe- \_ Renderziel \_ Ausgabe**</dt> <dt>1L <<  (1 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-115"><dt>**DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT**</dt> <dt>1L << (1 + 4)</dt></span></span> </dl> | <span data-ttu-id="afd3c-116">Verwenden Sie die-Oberfläche oder-Ressource als Ausgabe Renderziel.</span><span class="sxs-lookup"><span data-stu-id="afd3c-116">Use the surface or resource as an output render target.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <span data-ttu-id="afd3c-117"><dt>**DXGI \_ Usage- \_ \_ Shadereingabe**</dt> <dt>1L <<  (0 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-117"><dt>**DXGI\_USAGE\_SHADER\_INPUT**</dt> <dt>1L << (0 + 4)</dt></span></span> </dl>                          | <span data-ttu-id="afd3c-118">Verwenden Sie die-Oberfläche oder-Ressource als Eingabe für einen Shader.</span><span class="sxs-lookup"><span data-stu-id="afd3c-118">Use the surface or resource as an input to a shader.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <span data-ttu-id="afd3c-119"><dt>**DXGI \_ Verwendungs frei \_ gegebene**</dt> <dt>1L- <<  (3 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-119"><dt>**DXGI\_USAGE\_SHARED**</dt> <dt>1L << (3 + 4)</dt></span></span> </dl>                                             | <span data-ttu-id="afd3c-120">Freigeben der-Oberfläche oder-Ressource.</span><span class="sxs-lookup"><span data-stu-id="afd3c-120">Share the surface or resource.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <span data-ttu-id="afd3c-121"><dt>**DXGI \_ \_Ungeordneter \_ Zugriff**</dt> in der Verwendung von <dt>1L <<  (6 + 4)</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-121"><dt>**DXGI\_USAGE\_UNORDERED\_ACCESS**</dt> <dt>1L << (6 + 4)</dt></span></span> </dl>              | <span data-ttu-id="afd3c-122">Verwenden Sie die-Oberfläche oder-Ressource für den ungeordneten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="afd3c-122">Use the surface or resource for unordered access.</span></span><br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="afd3c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afd3c-123">Remarks</span></span>

<span data-ttu-id="afd3c-124">Jedes Flag wird als Ganzzahl ohne Vorzeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="afd3c-124">Each flag is defined as an unsigned integer.</span></span>

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

<span data-ttu-id="afd3c-125">Diese Flagoptionen werden bei einem aufzurufenden [**idxgifactory-Befehl verwendet: die Methoden "anateswapchain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain)", " [**IDXGIFactory2:: | ateswapchadetailhwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)", " [**IDXGIFactory2::**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)" und " [**IDXGIFactory2:: foateswapchadetailcomposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) ", um die Optionen für die Oberflächen Verwendung und den CPU-Zugriff für den Hintergrund Puffer einer Swapkette zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="afd3c-125">These flag options are used in a call to the [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) method to describe the surface usage and CPU access options for the back buffer of a swap chain.</span></span> <span data-ttu-id="afd3c-126">Es ist nicht möglich, die **\_ \_ gemeinsame Verwendung der DXGI-Verwendung**, die **DXGI- \_ Verwendung \_ verwerfen \_ \_** und die **DXGI- \_ Verwendung \_ \_** als Eingabe für die Erstellung einer SwapChain zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="afd3c-126">You can't use the **DXGI\_USAGE\_SHARED**, **DXGI\_USAGE\_DISCARD\_ON\_PRESENT**, and **DXGI\_USAGE\_READ\_ONLY** values as input to create a swap chain.</span></span> <span data-ttu-id="afd3c-127">DXGI kann jedoch die **DXGI- \_ Verwendungs \_ Verwerfungs \_ \_** -und **DXGI \_ - \_ Verwendung \_** für einige der Hintergrund Puffer der Swapkette im Auftrag der Anwendung festlegen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-127">However, DXGI can set **DXGI\_USAGE\_DISCARD\_ON\_PRESENT** and **DXGI\_USAGE\_READ\_ONLY** for some of the swap chain's back buffers on the application's behalf.</span></span> <span data-ttu-id="afd3c-128">Sie können die [**idxgiresource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) -Methode aufrufen, um die Verwendung dieser Hintergrund Puffer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="afd3c-128">You can call the [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) method to retrieve the usage of these back buffers.</span></span> <span data-ttu-id="afd3c-129">Die SwapChain unterstützt nur den **DXGI- \_ CPU- \_ Zugriff \_ None** -Wert im **Feld DXGI- \_ CPU- \_ Zugriff \_** auf die **DXGI- \_ Verwendung**.</span><span class="sxs-lookup"><span data-stu-id="afd3c-129">Swap chain's only support the **DXGI\_CPU\_ACCESS\_NONE** value in the **DXGI\_CPU\_ACCESS\_FIELD** part of **DXGI\_USAGE**.</span></span>

<span data-ttu-id="afd3c-130">Diese Flagoptionen werden auch von der [**idxgidevice:: kreatesurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="afd3c-130">These flag options are also used by the [**IDXGIDevice::CreateSurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="afd3c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afd3c-131">Requirements</span></span>



| <span data-ttu-id="afd3c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afd3c-132">Requirement</span></span> | <span data-ttu-id="afd3c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="afd3c-133">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="afd3c-134">Header</span><span class="sxs-lookup"><span data-stu-id="afd3c-134">Header</span></span><br/> | <dl> <span data-ttu-id="afd3c-135"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="afd3c-135"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afd3c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afd3c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afd3c-137">DXGI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="afd3c-137">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




