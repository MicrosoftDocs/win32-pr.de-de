---
title: Debuggen von apps mithilfe der Debugebene
description: Hier wird erläutert, wie Sie die debugschicht und einige der Probleme, die Sie mithilfe der debugschicht verhindern können, aktivieren.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708177"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="35ad8-103">Debuggen von apps mithilfe der Debugebene</span><span class="sxs-lookup"><span data-stu-id="35ad8-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="35ad8-104">Es wird empfohlen, dass Sie die [Debugebene](overviews-direct3d-11-devices-layers.md) verwenden, um Ihre apps zu debuggen, um sicherzustellen, dass Sie Fehler und Warnungen bereinigen.</span><span class="sxs-lookup"><span data-stu-id="35ad8-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="35ad8-105">Die Debug-Ebene hilft Ihnen beim Schreiben von Direct3D-Code.</span><span class="sxs-lookup"><span data-stu-id="35ad8-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="35ad8-106">Außerdem kann sich die Produktivität erhöhen, wenn Sie die debugschicht verwenden, da Sie sofort die Ursache für Fehler beim Rendern oder sogar schwarze Bildschirme an ihrer Quelle sehen können.</span><span class="sxs-lookup"><span data-stu-id="35ad8-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="35ad8-107">Die Debug-Ebene bietet Warnungen für viele Probleme.</span><span class="sxs-lookup"><span data-stu-id="35ad8-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="35ad8-108">Beispielsweise bietet die Debug-Ebene Warnungen für diese Probleme:</span><span class="sxs-lookup"><span data-stu-id="35ad8-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="35ad8-109">Es wurde vergessen, eine Textur festzulegen, aber aus ihr in ihren Pixelshader zu lesen.</span><span class="sxs-lookup"><span data-stu-id="35ad8-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="35ad8-110">Ausgabe Tiefe, aber keinen tiefen Schablone-Status gebunden</span><span class="sxs-lookup"><span data-stu-id="35ad8-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="35ad8-111">Fehler beim Erstellen der Textur mit invalidArg.</span><span class="sxs-lookup"><span data-stu-id="35ad8-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="35ad8-112">Hier wird erläutert, wie Sie die [debugschicht](overviews-direct3d-11-devices-layers.md) und einige der Probleme, die Sie mithilfe der debugschicht verhindern können, aktivieren.</span><span class="sxs-lookup"><span data-stu-id="35ad8-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="35ad8-113">Aktivieren der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="35ad8-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="35ad8-114">Verhindern von Fehlern in Ihrer APP mit der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="35ad8-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="35ad8-115">NULL-Zeiger nicht an die Karte übergeben</span><span class="sxs-lookup"><span data-stu-id="35ad8-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="35ad8-116">Quellfeld in Quell-und Ziel Ressourcen einschränken</span><span class="sxs-lookup"><span data-stu-id="35ad8-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="35ad8-117">Verwerfen Sie "verwerfen" oder "verwerfen" nicht.</span><span class="sxs-lookup"><span data-stu-id="35ad8-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="35ad8-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35ad8-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="35ad8-119">Aktivieren der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="35ad8-119">Enabling the debug layer</span></span>

<span data-ttu-id="35ad8-120">Zum Aktivieren der [Debug-Ebene](overviews-direct3d-11-devices-layers.md)geben Sie [**das D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) -Flag im *Flags* -Parameter an, wenn Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion aufrufen, um das renderinggerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="35ad8-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="35ad8-121">Dieser Beispielcode zeigt, wie Sie die Debugebene aktivieren, wenn sich das Microsoft Visual Studio Projekt in einem Debugbuild befindet:</span><span class="sxs-lookup"><span data-stu-id="35ad8-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="35ad8-122">Verhindern von Fehlern in Ihrer APP mit der Debug-Ebene</span><span class="sxs-lookup"><span data-stu-id="35ad8-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="35ad8-123">Wenn Sie die Direct3D 11-API missbrauchen oder ungültige Parameter übergeben, meldet die Debugausgabe der [debugschicht](overviews-direct3d-11-devices-layers.md) einen Fehler oder eine Warnung.</span><span class="sxs-lookup"><span data-stu-id="35ad8-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="35ad8-124">Anschließend können Sie den Fehler beheben.</span><span class="sxs-lookup"><span data-stu-id="35ad8-124">You can then correct your mistake.</span></span> <span data-ttu-id="35ad8-125">Als nächstes betrachten wir einige Codierungs Probleme, die zu nicht definiertem Verhalten oder sogar zum Absturz des Betriebssystems führen können.</span><span class="sxs-lookup"><span data-stu-id="35ad8-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="35ad8-126">Sie können diese Probleme mithilfe der debugschicht erfassen und verhindern.</span><span class="sxs-lookup"><span data-stu-id="35ad8-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="35ad8-127">NULL-Zeiger nicht an die Karte übergeben</span><span class="sxs-lookup"><span data-stu-id="35ad8-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="35ad8-128">Wenn Sie **null** an den *presource* -oder *pmappedresource* -Parameter der [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) -Methode übergeben, ist das Verhalten von **map** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="35ad8-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="35ad8-129">Wenn Sie ein Gerät erstellt haben, das nur die [Kern Ebene](overviews-direct3d-11-devices-layers.md)unterstützt, **können** ungültige Parameter für die Zuordnung das Betriebssystemabstürzen.</span><span class="sxs-lookup"><span data-stu-id="35ad8-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="35ad8-130">Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler in **diesem ungültigen** Zuordnungs Befehl.</span><span class="sxs-lookup"><span data-stu-id="35ad8-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="35ad8-131">Quellfeld in Quell-und Ziel Ressourcen einschränken</span><span class="sxs-lookup"><span data-stu-id="35ad8-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="35ad8-132">Beim Abrufen der [**Verknüpfung id3d11devicecontext aus:: copysubresourceregion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) -Methode muss sich das Quellfeld in der Quell Ressource befinden.</span><span class="sxs-lookup"><span data-stu-id="35ad8-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="35ad8-133">Durch die Ziel Offsets (x, y und z) kann das Quellfeld beim Schreiben in die Ziel Ressource versetzt werden, aber die Abmessungen des Quellfelds und der Offsets müssen sich innerhalb der Größe der Ressource befinden.</span><span class="sxs-lookup"><span data-stu-id="35ad8-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="35ad8-134">Wenn Sie versuchen, eine Kopie außerhalb der Ziel Ressource zu kopieren oder ein Quellfeld anzugeben, das größer ist als die Quell Ressource, ist das Verhalten von **copysubresourceregion** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="35ad8-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="35ad8-135">Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler für diesen ungültigen **copysubresourceregion** -Befehl.</span><span class="sxs-lookup"><span data-stu-id="35ad8-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="35ad8-136">Ungültige Parameter für **copysubresourceregion** verursachen nicht definiertes Verhalten und können zu einem falschen Rendering, Clipping, ohne Kopie oder sogar zum Entfernen des renderinggeräts führen.</span><span class="sxs-lookup"><span data-stu-id="35ad8-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="35ad8-137">Verwerfen Sie "verwerfen" oder "verwerfen" nicht.</span><span class="sxs-lookup"><span data-stu-id="35ad8-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="35ad8-138">Die Laufzeit löscht einen [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) oder [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , es sei denn, Sie erstellen die Ressource ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="35ad8-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="35ad8-139">Die Ressource, die Sie an [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) übergeben, muss mithilfe von [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ Usage \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein. andernfalls löscht die Laufzeit den Rückruf von " **verwerfen**".</span><span class="sxs-lookup"><span data-stu-id="35ad8-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="35ad8-140">Die Ressource, die der Ansicht zugrunde liegt, die Sie an [**ID3D11DeviceContext1 übergeben::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) muss mit der [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) oder [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)erstellt worden sein. andernfalls löscht die Laufzeit den Rückruf von " **verwerfen View**".</span><span class="sxs-lookup"><span data-stu-id="35ad8-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="35ad8-141">Wenn Sie ein Gerät erstellt haben, das die [debugschicht](overviews-direct3d-11-devices-layers.md)unterstützt, meldet die Debugausgabe einen Fehler bezüglich des gelöschten Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="35ad8-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35ad8-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35ad8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ad8-143">Software Ebenen</span><span class="sxs-lookup"><span data-stu-id="35ad8-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




