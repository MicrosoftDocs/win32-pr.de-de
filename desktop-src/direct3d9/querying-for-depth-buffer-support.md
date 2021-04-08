---
description: Wie bei allen Features unterstützt der Treiber, den Ihre Anwendung verwendet, möglicherweise nicht alle Arten der tiefen Pufferung.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Abfragen der Tiefe Puffer Unterstützung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745521"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a><span data-ttu-id="2fb77-103">Abfragen der Tiefe Puffer Unterstützung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2fb77-103">Querying for Depth Buffer Support (Direct3D 9)</span></span>

<span data-ttu-id="2fb77-104">Wie bei allen Features unterstützt der Treiber, den Ihre Anwendung verwendet, möglicherweise nicht alle Arten der tiefen Pufferung.</span><span class="sxs-lookup"><span data-stu-id="2fb77-104">As with any feature, the driver that your application uses might not support all types of depth buffering.</span></span> <span data-ttu-id="2fb77-105">Überprüfen Sie immer die Funktionen des Treibers.</span><span class="sxs-lookup"><span data-stu-id="2fb77-105">Always check the driver's capabilities.</span></span> <span data-ttu-id="2fb77-106">Obwohl die meisten Treiber z-basierte tiefen Pufferung unterstützen, unterstützen nicht alle die w-basierte tiefen Pufferung.</span><span class="sxs-lookup"><span data-stu-id="2fb77-106">Although most drivers support z-based depth buffering, not all will support w-based depth buffering.</span></span> <span data-ttu-id="2fb77-107">Treiber schlagen nicht fehl, wenn Sie versuchen, ein nicht unterstütztes Schema zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2fb77-107">Drivers do not fail if you attempt to enable an unsupported scheme.</span></span> <span data-ttu-id="2fb77-108">Sie werden stattdessen auf eine andere tiefen Puffer Methode zurückgreifen, oder Sie deaktivieren manchmal die Tiefe Pufferung, was dazu führen kann, dass Szenen mit extrem tiefen Sortier Artefakten gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="2fb77-108">They fall back on another depth buffering method instead, or sometimes disable depth buffering altogether, which can result in scenes rendered with extreme depth-sorting artifacts.</span></span>

<span data-ttu-id="2fb77-109">Sie können die allgemeine Unterstützung von tiefen Puffern überprüfen, indem Sie Direct3D für das Anzeigegerät Abfragen, das von der Anwendung verwendet wird, bevor Sie ein Direct3D-Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="2fb77-109">You can check for general support for depth buffers by querying Direct3D for the display device that your application will use before you create a Direct3D device.</span></span> <span data-ttu-id="2fb77-110">Wenn das Direct3D-Objekt meldet, dass die tiefen Pufferung unterstützt wird, unterstützen alle Hardware Geräte, die Sie aus diesem Direct3D-Objekt erstellen, z-Pufferung.</span><span class="sxs-lookup"><span data-stu-id="2fb77-110">If the Direct3D object reports that it supports depth buffering, any hardware devices you create from this Direct3D object will support z-buffering.</span></span>

<span data-ttu-id="2fb77-111">Um die Unterstützung der tiefen Pufferung abzufragen, können Sie die [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) -Methode verwenden, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fb77-111">To query for depth buffering support, you can use the [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) method, as shown in the following code example.</span></span>


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



<span data-ttu-id="2fb77-112">[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) ermöglicht Ihnen die Auswahl eines zu erstellenden Geräts basierend auf den Funktionen dieses Geräts.</span><span class="sxs-lookup"><span data-stu-id="2fb77-112">[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="2fb77-113">In diesem Fall werden Geräte, die 16-Bit-Tiefen Puffer nicht unterstützen, zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="2fb77-113">In this case, devices that do not support 16-bit depth buffers are rejected.</span></span>

<span data-ttu-id="2fb77-114">Die Verwendung von [**IDirect3D9:: checkdepthstencilmatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) zum Ermitteln der tiefen Schablone-Kompatibilität mit einem Renderziel wird im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2fb77-114">Using [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) to determine depth-stencil compatibility with a render target is illustrated in the following code example.</span></span>


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



<span data-ttu-id="2fb77-115">Wenn Sie wissen, dass der Treiber Tiefe Puffer unterstützt, können Sie die Unterstützung für den w-Puffer überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2fb77-115">When you know that the driver supports depth buffers, you can verify w-buffer support.</span></span> <span data-ttu-id="2fb77-116">Obwohl tiefen Puffer für alle Software Rasterizer unterstützt werden, werden w-Puffer nur vom Verweis Raster unterstützt, der nicht für die Verwendung durch reale Anwendungen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="2fb77-116">Although depth buffers are supported for all software rasterizers, w-buffers are supported only by the reference rasterizer, which is not suited for use by real-world applications.</span></span> <span data-ttu-id="2fb77-117">Überprüfen Sie unabhängig vom Gerätetyp, der von der Anwendung verwendet wird, die Unterstützung für w-Puffer, bevor Sie versuchen, die w-basierte tiefen Pufferung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2fb77-117">Regardless of the type of device your application uses, verify support for w-buffers before you attempt to enable w-based depth buffering.</span></span>

1.  <span data-ttu-id="2fb77-118">Nachdem Sie Ihr Gerät erstellt haben, können Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) -Methode aufrufen und dabei eine initialisierte [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur übergeben.</span><span class="sxs-lookup"><span data-stu-id="2fb77-118">After creating your device, call the [**IDirect3DDevice9::GetDeviceCaps**](/windows/desktop/api) method, passing an initialized [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>
2.  <span data-ttu-id="2fb77-119">Nach dem-Befehl enthält das LineCaps-Element Informationen über die Unterstützung des Treibers für das Rendern von primitiven.</span><span class="sxs-lookup"><span data-stu-id="2fb77-119">After the call, the LineCaps member contains information about the driver's support for rendering primitives.</span></span>
3.  <span data-ttu-id="2fb77-120">Wenn das RasterCaps-Element dieser Struktur das D3DPRASTERCAPS \_ wbuffer-Flag enthält, unterstützt der Treiber die w-basierte tiefen Pufferung für diesen primitiven Typ.</span><span class="sxs-lookup"><span data-stu-id="2fb77-120">If the RasterCaps member of this structure contains the D3DPRASTERCAPS\_WBUFFER flag, then the driver supports w-based depth buffering for that primitive type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fb77-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fb77-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fb77-122">Tiefen Puffer</span><span class="sxs-lookup"><span data-stu-id="2fb77-122">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
