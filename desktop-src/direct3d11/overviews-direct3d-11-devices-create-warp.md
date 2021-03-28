---
title: Erstellen eines Warp-Geräts
description: In diesem Thema wird gezeigt, wie ein Warp-Gerät erstellt wird, das einen hoch Geschwindigkeits Software-Rasterizer implementiert.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993486"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="5362c-103">Vorgehensweise: Erstellen eines Warp-Geräts</span><span class="sxs-lookup"><span data-stu-id="5362c-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="5362c-104">In diesem Thema wird gezeigt, wie ein Warp-Gerät erstellt wird, das einen hoch Geschwindigkeits Software-Rasterizer implementiert.</span><span class="sxs-lookup"><span data-stu-id="5362c-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="5362c-105">Zum Erstellen eines Warp-Geräts geben Sie einfach an, dass das Gerät, das Sie erstellen, einen Warp-Treiber verwendet.</span><span class="sxs-lookup"><span data-stu-id="5362c-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="5362c-106">In diesem Beispiel werden gleichzeitig ein Gerät und eine SwapChain erstellt.</span><span class="sxs-lookup"><span data-stu-id="5362c-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="5362c-107">**So erstellen Sie ein Warp-Gerät**</span><span class="sxs-lookup"><span data-stu-id="5362c-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="5362c-108">Definieren Sie anfängliche Parameter für eine SwapChain.</span><span class="sxs-lookup"><span data-stu-id="5362c-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="5362c-109">Fordern Sie eine Funktionsebene an, die die Features implementiert, die Ihre Anwendung benötigt.</span><span class="sxs-lookup"><span data-stu-id="5362c-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="5362c-110">Ein Warp-Gerät kann für featureebenen erfolgreich erstellt werden **D3D \_ Featureebene \_ \_ 9 \_ 1** bis **D3D \_ Funktions \_ Ebene \_ 10 \_ 1** und ab Windows 8 für alle featureebenen.</span><span class="sxs-lookup"><span data-stu-id="5362c-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="5362c-111">Weitere Informationen zu featureebenen finden Sie in der Enumeration der [**D3D- \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="5362c-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="5362c-112">Erstellen Sie das Gerät durch Aufrufen von [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="5362c-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="5362c-113">Sie müssen den API-Befehl mit dem Warp-Treibertyp aus der [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) -Enumeration bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5362c-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="5362c-114">Nachdem die Methode erfolgreich ausgeführt wurde, gibt Sie eine Austausch Ketten Schnittstelle, eine Geräteschnittstelle, einen Zeiger auf die Featureebene, die vom Treiber erteilt wurde, und eine unmittelbare Kontext Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="5362c-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="5362c-115">Informationen zu Einschränkungen bei der Erstellung eines Warp-Geräts auf bestimmten featureebenen finden Sie unter [Einschränkungen beim Erstellen von Warp-und Referenz Geräten](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="5362c-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="5362c-116">Neu für Windows 8</span><span class="sxs-lookup"><span data-stu-id="5362c-116">New for Windows 8</span></span>

<span data-ttu-id="5362c-117">Wenn der primäre Anzeige Adapter eines Computers der "Microsoft Basic Display Adapter" (Warp-Adapter) ist, verfügt dieser Computer auch über einen zweiten Adapter.</span><span class="sxs-lookup"><span data-stu-id="5362c-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="5362c-118">Bei diesem zweiten Adapter handelt es sich um das reine Rendering-Gerät ohne Anzeige Ausgaben.</span><span class="sxs-lookup"><span data-stu-id="5362c-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="5362c-119">Weitere Informationen zum reinen Rendering-Gerät finden Sie unter [neue Informationen in Windows 8 zum Auflisten von Adaptern](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="5362c-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5362c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5362c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5362c-121">Geräte</span><span class="sxs-lookup"><span data-stu-id="5362c-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="5362c-122">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5362c-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 