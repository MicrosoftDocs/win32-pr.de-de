---
title: Oberflächenfreigabe zwischen Windows-Grafik-APIs
description: Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1032cb1cf9b16280088f00e79e7e59bb7f1510b1
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343615"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="8fd69-103">Oberflächenfreigabe zwischen Windows-Grafik-APIs</span><span class="sxs-lookup"><span data-stu-id="8fd69-103">Surface sharing between Windows graphics APIs</span></span>

<span data-ttu-id="8fd69-104">Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="8fd69-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="8fd69-105">Wenn Sie bereits über fundierte Kenntnisse dieser APIs verfügen, können Sie in diesem Artikel mehrere APIs verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, auf die gleiche Oberfläche zu rendern.</span><span class="sxs-lookup"><span data-stu-id="8fd69-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="8fd69-106">Dieses Thema enthält auch Richtlinien für bewährte Methoden und Hinweise auf zusätzliche Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="8fd69-107">Für direct2D- und DirectWrite-Interoperabilität in der DirectX 11.1-Runtime können Sie [Direct2D-Geräte und Gerätekontexte](/windows/desktop/Direct2D/devices-and-device-contexts) verwenden, um direkt auf Direct3D 11-Geräten zu rendern.</span><span class="sxs-lookup"><span data-stu-id="8fd69-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="8fd69-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="8fd69-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8fd69-109">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="8fd69-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="8fd69-110">Übersicht über die API-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="8fd69-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="8fd69-111">Interoperabilitätsszenarien</span><span class="sxs-lookup"><span data-stu-id="8fd69-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="8fd69-112">Direct3D 10.1-Gerätefreigabe mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="8fd69-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="8fd69-113">DXGI 1.1 Synchronisierte freigegebene Oberflächen</span><span class="sxs-lookup"><span data-stu-id="8fd69-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="8fd69-114">Interoperabilität zwischen Direct3D 9Ex- und DXGI-basierten APIs</span><span class="sxs-lookup"><span data-stu-id="8fd69-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="8fd69-115">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8fd69-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="8fd69-116">Einführung</span><span class="sxs-lookup"><span data-stu-id="8fd69-116">Introduction</span></span>

<span data-ttu-id="8fd69-117">In diesem Dokument bezieht sich die Interoperabilität der Windows-Grafik-API auf die Gemeinsame Nutzung derselben Renderingoberfläche durch verschiedene APIs.</span><span class="sxs-lookup"><span data-stu-id="8fd69-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="8fd69-118">Diese Art von Interoperabilität ermöglicht Es Anwendungen, überzeugende Anzeigen zu erstellen, indem sie mehrere Windows-Grafik-APIs nutzen und die Migration zu neuen Technologien vereinfachen, indem die Kompatibilität mit vorhandenen APIs aufrechterhalten wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="8fd69-119">Unter Windows 7 (und Windows Vista SP2 mit Windows 7 Interop Pack, Vista 7IP) sind die Grafikrendering-APIs Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c und frühere Direct3D-APIs sowie GDI und GDI+.</span><span class="sxs-lookup"><span data-stu-id="8fd69-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="8fd69-120">Windows-Bilderstellungskomponente (WIC) und DirectWrite sind verwandte Technologien für die Bildverarbeitung, und Direct2D führt Textrendering durch.</span><span class="sxs-lookup"><span data-stu-id="8fd69-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="8fd69-121">DirectX Video Acceleration API (DXVA), basierend auf Direct3D 9c und Direct3D 9Ex, wird für die Videoverarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="8fd69-122">Mit der Weiterentwicklung von Windows-Grafik-APIs hin zu Direct3D-basierten ApIs investiert Microsoft mehr Aufwand in die Sicherstellung der APIs-übergreifenden Interoperabilität.</span><span class="sxs-lookup"><span data-stu-id="8fd69-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="8fd69-123">Neu entwickelte Direct3D-APIs und APIs auf höherer Ebene, die auf Direct3D-APIs basieren, bieten bei Bedarf auch Unterstützung für die Überbrückung der Kompatibilität mit älteren APIs.</span><span class="sxs-lookup"><span data-stu-id="8fd69-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="8fd69-124">Zur Veranschaulichung können Direct2D-Anwendungen Direct3D 10.1 verwenden, indem sie ein Direct3D 10.1-Gerät freigeben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="8fd69-125">Außerdem können Direct3D 11-, Direct2D- und Direct3D 10.1-APIs die Vorteile von DirectX Graphic Infrastructure (DXGI) 1.1 nutzen, das synchronisierte freigegebene Oberflächen ermöglicht, die die Interoperabilität zwischen diesen APIs vollständig unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="8fd69-126">DXGI 1.1-basierte APIs interoperabilität mit GDI und mit GDI+ nach Zuordnung, indem sie den GDI-Gerätekontext von einer DXGI 1.1-Oberfläche abrufen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="8fd69-127">Weitere Informationen finden Sie in der DXGI- und GDI-Interoperabilitätsdokumentation auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="8fd69-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="8fd69-128">Die nicht synchronisierte Oberflächenfreigabe wird von der Direct3D 9Ex-Runtime unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="8fd69-129">DXVA-basierte Videoanwendungen können das Direct3D 9Ex- und DXGI-Interoperabilitätshilfe für die Direct3D 9Ex-basierte DXVA-Interoperabilität mit Direct3D 11 für Compute-Shader verwenden oder mit Direct2D für 2D-Steuerelemente oder Textrendering zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="8fd69-130">WIC und DirectWrite können auch mit GDI, Direct2D und anderen Direct3D-APIs zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="8fd69-131">Direct3D 10.0, Direct3D 9c und ältere Direct3D-Runtimes unterstützen keine freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="8fd69-132">Systemspeicherkopien werden weiterhin für die Interoperabilität mit GDI- oder DXGI-basierten APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="8fd69-133">Beachten Sie, dass sich die Interoperabilitätsszenarien in diesem Dokument auf mehrere Grafik-APIs beziehen, die auf eine freigegebene Renderingoberfläche und nicht auf dasselbe Anwendungsfenster gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="8fd69-134">Die Synchronisierung für separate APIs für verschiedene Oberflächen, die dann im selben Fenster zusammengesetzt werden, liegt außerhalb des Rahmens dieses Whitepapers.</span><span class="sxs-lookup"><span data-stu-id="8fd69-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="8fd69-135">Übersicht über die API-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="8fd69-135">API Interoperability Overview</span></span>

<span data-ttu-id="8fd69-136">Die Oberflächenfreigabe-Interoperabilität von Windows-Grafik-APIs kann in Bezug auf API-zu-API-Szenarien und die entsprechende Interoperabilitätsfunktionalität beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="8fd69-137">Ab Windows 7 und ab Windows Vista SP2 mit 7IP enthalten neue APIs und zugehörige Runtimes Direct2D und zugehörige Technologien: Direct3D 11 und DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="8fd69-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="8fd69-138">Die GDI-Leistung wurde auch in Windows 7 verbessert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="8fd69-139">Direct3D 10.1 wurde in Windows Vista SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="8fd69-140">Das folgende Diagramm zeigt die Interoperabilitätsunterstützung zwischen APIs.</span><span class="sxs-lookup"><span data-stu-id="8fd69-140">The following diagram shows the interoperability support between APIs.</span></span>

![Diagramm der Interoperabilitätsunterstützung zwischen Windows-Grafik-APIs](images/surface-sharing-interoperability.png)

<span data-ttu-id="8fd69-142">In diesem Diagramm zeigen Pfeile Interoperabilitätsszenarien an, in denen die verbundenen APIs auf dieselbe Oberfläche zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="8fd69-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="8fd69-143">Blaue Pfeile zeigen Interoperabilitätsmechanismen an, die in Windows Vista eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="8fd69-144">Grüne Pfeile zeigen die Interoperabilitätsunterstützung für neue APIs oder Verbesserungen an, die älteren APIs bei der Interoperabilität mit neueren APIs helfen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="8fd69-145">Grüne Pfeile stellen beispielsweise die Gerätefreigabe, die Unterstützung der synchronisierten freigegebenen Oberfläche, das Direct3D 9Ex/DXGI-Synchronisierungshilfselement und das Abrufen eines GDI-Gerätekontexts von einer kompatiblen Oberfläche dar.</span><span class="sxs-lookup"><span data-stu-id="8fd69-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="8fd69-146">Interoperabilitätsszenarien</span><span class="sxs-lookup"><span data-stu-id="8fd69-146">Interoperability Scenarios</span></span>

<span data-ttu-id="8fd69-147">Ab Windows 7 und Windows Vista 7IP unterstützen gängige Angebote von Windows-Grafik-APIs mehrere APIs, die auf derselben DXGI 1.1-Oberfläche gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="8fd69-148">**Direct3D 11, Direct3D 10.1, Direct2D – Interoperabilität miteinander**</span><span class="sxs-lookup"><span data-stu-id="8fd69-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="8fd69-149">Direct3D 11-, Direct3D 10.1- und Direct2D-APIs (und zugehörige APIs wie DirectWrite und WIC) können über direct3D 10.1-Gerätefreigabe oder synchronisierte freigegebene Oberflächen miteinander zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="8fd69-150">Direct3D 10.1-Gerätefreigabe mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="8fd69-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="8fd69-151">Die Gerätefreigabe zwischen Direct2D und Direct3D 10.1 ermöglicht es einer Anwendung, beide APIs zu verwenden, um nahtlos und effizient auf derselben DXGI 1.1-Oberfläche zu rendern, wobei das gleiche zugrunde liegende Direct3D-Geräteobjekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="8fd69-152">Direct2D bietet die Möglichkeit, Direct2D-APIs mit einem vorhandenen Direct3D 10.1-Gerät aufzurufen. Dabei wird die Tatsache genutzt, dass Direct2D auf Direct3D 10.1- und DXGI 1.1-Runtimes basiert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="8fd69-153">Die folgenden Codeausschnitte veranschaulichen, wie Direct2D das Direct3D 10.1-Geräterenderingziel von einer DXGI 1.1-Oberfläche erhält, die dem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="8fd69-154">Das Direct3D 10.1-Geräterenderingziel kann Direct2D-Zeichnungsaufrufe zwischen BeginDraw- und EndDraw-APIs ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



<span data-ttu-id="8fd69-155">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-155">**Remarks**</span></span>

-   <span data-ttu-id="8fd69-156">Das zugeordnete Direct3D 10.1-Gerät muss das BGRA-Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="8fd69-157">Dieses Gerät wurde durch Aufrufen von D3D10CreateDevice1 mit dem Parameter D3D10 \_ CREATE \_ DEVICE \_ BGRA SUPPORT \_ erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="8fd69-158">Das BGRA-Format wird ab Direct3D 10 Featureebene 9.1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="8fd69-159">Die Anwendung sollte nicht mehrere ID2D1RenderTargets erstellen, die demselben Direct3D10.1-Gerät zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="8fd69-160">Um eine optimale Leistung zu erzielen, sollten Sie jederzeit mindestens eine Ressource verwenden, z. B. Texturen oder Oberflächen, die dem Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="8fd69-161">Die Gerätefreigabe eignet sich für die Prozess-Singlethread-Verwendung eines Renderinggeräts, das von Direct3D 10.1- und Direct2D-Rendering-APIs gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="8fd69-162">Synchronisierte freigegebene Oberflächen ermöglichen die Verwendung mehrerer Renderinggeräte, die von Direct3D 10.1-, Direct2D- und Direct3D 11-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="8fd69-163">Eine weitere Methode der Direct3D 10.1- und Direct2D-Interoperabilität ist die Verwendung von ID3D1RenderTarget::CreateSharedBitmap, die ein ID2D1Bitmap-Objekt aus IDXGISurface erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="8fd69-164">Sie können eine Direct3D10.1-Szene in die Bitmap schreiben und mit Direct2D rendern.</span><span class="sxs-lookup"><span data-stu-id="8fd69-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="8fd69-165">Weitere Informationen finden Sie unter [ID2D1RenderTarget::CreateSharedBitmap-Methode.](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)</span><span class="sxs-lookup"><span data-stu-id="8fd69-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="8fd69-166">Direct2D-Softwarerasterung</span><span class="sxs-lookup"><span data-stu-id="8fd69-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="8fd69-167">Die Gerätefreigabe mit Direct3D 10.1 wird bei Verwendung des Direct2D-Softwarerenderers nicht unterstützt, z. B. durch Angabe von D2D1 RENDER TARGET USAGE FORCE SOFTWARE RENDERING in D2D1 RENDER TARGET USAGE beim Erstellen eines \_ \_ \_ \_ \_ \_ \_ \_ \_ Direct2D-Renderziels.</span><span class="sxs-lookup"><span data-stu-id="8fd69-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="8fd69-168">Direct2D kann den WARP10-Softwareraster verwenden, um das Gerät mit Direct3D 10 oder Direct3D 11 zu teilen, aber die Leistung verringert sich erheblich.</span><span class="sxs-lookup"><span data-stu-id="8fd69-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="8fd69-169">DXGI 1.1 Synchronisierte freigegebene Oberflächen</span><span class="sxs-lookup"><span data-stu-id="8fd69-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="8fd69-170">Direct3D 11-, Direct3D 10.1- und Direct2D-APIs verwenden dxgi 1.1, das die Funktionalität bietet, das Lesen von und Schreiben von zwei oder mehr Direct3D-Geräten von derselben Videospeicheroberfläche (DXGISurface1) zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="8fd69-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="8fd69-171">Die Renderinggeräte, die synchronisierte freigegebene Oberflächen verwenden, können Direct3D 10.1- oder Direct3D 11-Geräte sein, die jeweils im gleichen Prozess oder prozessübergreifend ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="8fd69-172">Anwendungen können synchronisierte freigegebene Oberflächen verwenden, um zwischen dxgi 1.1-basierten Geräten wie Direct3D 11 und Direct3D 10.1 oder zwischen Direct3D 11 und Direct2D zu zusammenarbeiten, indem sie das Direct3D 10.1-Gerät aus dem Direct2D-Renderzielobjekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="8fd69-173">Stellen Sie in Direct3D 10.1 und höher sicher, dass das Direct3D-Gerät mit einem DXGI 1.1-Adapterobjekt erstellt wird, das aus dem DXGI 1.1-Factoryobjekt aufzählt wird, um DXGI 1.1 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="8fd69-174">Rufen Sie CreateDXGIFactory1 auf, um das IDXGIFactory1-Objekt zu erstellen, und EnumAdapters1, um das IDXGIAdapter1-Objekt aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="8fd69-175">Das IDXGIAdapter1-Objekt muss als Teil des Aufrufs D3D10CreateDevice oder D3D10CreateDeviceAndSwapChain übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="8fd69-176">Weitere Informationen zu DXGI 1.1-APIs finden Sie im [Programmierhandbuch für DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8fd69-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="8fd69-177">APIs</span><span class="sxs-lookup"><span data-stu-id="8fd69-177">APIs</span></span>

<span data-ttu-id="8fd69-178">**D3D10-RESSOURCE \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="8fd69-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="8fd69-179">Legen Sie beim Erstellen der synchronisierten freigegebenen Ressource D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX in D3D10 \_ RESOURCE \_ MISC FLAG \_ fest.</span><span class="sxs-lookup"><span data-stu-id="8fd69-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="8fd69-180">**D3D10-RESSOURCE \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**</span><span class="sxs-lookup"><span data-stu-id="8fd69-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="8fd69-181">Ermöglicht die Synchronisierung der erstellten Ressource mithilfe der APIs IDXGIKeyedMutex::AcquireSync und ReleaseSync.</span><span class="sxs-lookup"><span data-stu-id="8fd69-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="8fd69-182">Die folgenden Direct3D 10.1-APIs für die Ressourcenerstellung, die alle einen D3D10 \_ RESOURCE \_ MISC FLAG-Parameter verwenden, wurden \_ erweitert, um das neue Flag zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="8fd69-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="8fd69-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="8fd69-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="8fd69-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="8fd69-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="8fd69-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="8fd69-186">ID3D10Device1::CreateBuffer</span><span class="sxs-lookup"><span data-stu-id="8fd69-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="8fd69-187">Wenn eine der aufgelisteten Funktionen mit dem D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX-Flag aufgerufen wird, kann die zurückgegebene Schnittstelle nach einer IDXGIKeyedMutex-Schnittstelle abgefragt werden, die AcquireSync- und ReleaseSync-APIs implementiert, um den Zugriff auf die Oberfläche zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="8fd69-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="8fd69-188">Das Gerät, das die Oberfläche erstellt, und jedes andere Gerät, das die Oberfläche öffnet (mit OpenSharedResource), muss IDXGIKeyedMutex::AcquireSync vor rendering-Befehlen auf der Oberfläche und IDXGIKeyedMutex::ReleaseSync aufrufen, wenn das Rendering fertig ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="8fd69-189">WARP- und REF-Geräte unterstützen keine freigegebenen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="8fd69-190">Wenn Sie versuchen, eine Ressource mit diesem Flag auf einem WARP- oder REF-Gerät zu erstellen, gibt die create-Methode einen E \_ OUTOFMEMORY-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="8fd69-191">**IDXGIKEYEDMUTEX-SCHNITTSTELLE**</span><span class="sxs-lookup"><span data-stu-id="8fd69-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="8fd69-192">Eine neue Schnittstelle in DXGI 1.1, IDXGIKeyedMutex, stellt einen schlüsselierten Mutex dar, der exklusiven Zugriff auf eine freigegebene Ressource ermöglicht, die von mehreren Geräten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="8fd69-193">Eine Referenzdokumentation zu dieser Schnittstelle und den beiden Methoden AcquireSync und ReleaseSync finden Sie unter [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="8fd69-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="8fd69-194">Beispiel: Synchronisierte Oberflächenfreigabe zwischen zwei Direct3D 10.1-Geräten</span><span class="sxs-lookup"><span data-stu-id="8fd69-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="8fd69-195">Das folgende Beispiel veranschaulicht die Gemeinsame Nutzung einer Oberfläche zwischen zwei Direct3D 10.1-Geräten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="8fd69-196">Die synchronisierte freigegebene Oberfläche wird von einem Direct3D10.1-Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



<span data-ttu-id="8fd69-197">Das gleiche Direct3D10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem AcquireSync aufruft und dann die Oberfläche für das Rendering des anderen Geräts durch Aufrufen von ReleaseSync freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="8fd69-198">Wenn die synchronisierte freigegebene Oberfläche nicht für ein anderes Direct3D-Gerät freigegeben wird, kann der Ersteller die synchronisierte freigegebene Oberfläche (zum Starten und Beenden des Renderings) abrufen und freigeben, indem er denselben Schlüsselwert erhält und frei gibt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



<span data-ttu-id="8fd69-199">Das zweite Direct3D10.1-Gerät kann die synchronisierte freigegebene Oberfläche zum Rendern abrufen, indem AcquireSync aufruft und dann die Oberfläche für das Rendering des ersten Geräts durch Aufrufen von ReleaseSync freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="8fd69-200">Beachten Sie, dass Gerät 2 die synchronisierte freigegebene Oberfläche mit demselben Schlüsselwert wie im ReleaseSync-Aufruf von Gerät 1 erhalten kann.</span><span class="sxs-lookup"><span data-stu-id="8fd69-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



<span data-ttu-id="8fd69-201">Zusätzliche Geräte, die sich die gleiche Oberfläche teilen, können die Oberfläche mithilfe zusätzlicher Schlüssel nach und nach abrufen und freigeben, wie in den folgenden Aufrufen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



<span data-ttu-id="8fd69-202">Beachten Sie, dass eine reale Anwendung möglicherweise immer auf einer Zwischenoberfläche gerendert wird, die dann auf die freigegebene Oberfläche kopiert wird, um zu verhindern, dass ein Gerät auf ein anderes Gerät wartet, das die Oberfläche teilt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="8fd69-203">Verwenden synchronisierter freigegebener Oberflächen mit Direct2D und Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8fd69-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="8fd69-204">Auf ähnliche Weise kann für die Freigabe zwischen Direct3D 11- und Direct3D 10.1-APIs eine synchronisierte freigegebene Oberfläche entweder über ein API-Gerät erstellt und mit den anderen API-Geräten gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="8fd69-205">Anwendungen, die Direct2D verwenden, können ein Direct3D 10.1-Gerät gemeinsam nutzen und eine synchronisierte freigegebene Oberfläche verwenden, um mit Direct3D 11 oder anderen Direct3D 10.1-Geräten zu zusammenarbeiten, unabhängig davon, ob sie demselben Prozess oder verschiedenen Prozessen angehören.</span><span class="sxs-lookup"><span data-stu-id="8fd69-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="8fd69-206">Bei Singlethreadanwendungen mit nur einem Prozess ist die Gerätefreigabe jedoch die leistungsfähigste und effizienteste Methode für die Interoperabilität zwischen Direct2D und Direct3D 10 oder Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8fd69-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="8fd69-207">Softwarerasterizer</span><span class="sxs-lookup"><span data-stu-id="8fd69-207">Software Rasterizer</span></span>

<span data-ttu-id="8fd69-208">Synchronisierte freigegebene Oberflächen werden nicht unterstützt, wenn Anwendungen die Direct3D- oder Direct2D-Softwarerasterizer verwenden, einschließlich des Referenzrasterizers und WARP, anstatt die Grafikhardwarebeschleunigung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="8fd69-209">Interoperabilität zwischen Direct3D 9Ex- und DXGI-basierten APIs</span><span class="sxs-lookup"><span data-stu-id="8fd69-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="8fd69-210">Direct3D 9Ex-APIs enthielten das Konzept der Oberflächenfreigabe, damit andere APIs von der freigegebenen Oberfläche lesen können.</span><span class="sxs-lookup"><span data-stu-id="8fd69-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="8fd69-211">Um Lese- und Schreibvorgänge für eine freigegebene Direct3D 9Ex-Oberfläche freizugeben, müssen Sie der Anwendung selbst eine manuelle Synchronisierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="8fd69-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span><span class="sxs-lookup"><span data-stu-id="8fd69-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="8fd69-213">Die grundlegendste Aufgabe in der Interoperabilität von Direct3D 9Ex und Direct3D 10 oder 11 besteht darin, eine einzelne Oberfläche vom ersten Gerät (Gerät A) an das zweite Gerät (Gerät B) zu übergeben, sodass das Rendering von Gerät A garantiert abgeschlossen ist, wenn Gerät B ein Handle auf der Oberfläche erhält.</span><span class="sxs-lookup"><span data-stu-id="8fd69-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="8fd69-214">Daher kann Gerät B diese Oberfläche ohne Bedenken verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="8fd69-215">Dies ähnelt dem klassischen Producer-Consumer-Problem, und diese Diskussion modelliert das Problem auf diese Weise.</span><span class="sxs-lookup"><span data-stu-id="8fd69-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="8fd69-216">Das erste Gerät, das die Oberfläche verwendet und dann auf den Producer (Gerät A) verzichten muss, und das Gerät, das anfänglich wartet, ist der Consumer (Gerät B).</span><span class="sxs-lookup"><span data-stu-id="8fd69-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="8fd69-217">Jede reale Anwendung ist komplexer als diese und verkettet mehrere Producer-Consumer-Bausteine, um die gewünschte Funktionalität zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="8fd69-218">Die Producer-Consumer-Bausteine werden im Hilfsfeld mithilfe einer Warteschlange von Oberflächen implementiert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="8fd69-219">Oberflächen werden vom Producer in die Enqueued und vom Consumer aus der Queuing entfernt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="8fd69-220">Das Hilfsprogramm führt drei COM-Schnittstellen ein: ISurfaceQueue, ISurfaceProducer und ISurfaceConsumer.</span><span class="sxs-lookup"><span data-stu-id="8fd69-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="8fd69-221">High-Level Übersicht über Helper</span><span class="sxs-lookup"><span data-stu-id="8fd69-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="8fd69-222">Das ISurfaceQueue-Objekt ist der Baustein für die Verwendung der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="8fd69-223">Es wird mit einem initialisierten Direct3D-Gerät und einer Beschreibung erstellt, um eine feste Anzahl von freigegebenen Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="8fd69-224">Das Warteschlangenobjekt verwaltet die Erstellung von Ressourcen und das Öffnen von Code.</span><span class="sxs-lookup"><span data-stu-id="8fd69-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="8fd69-225">Anzahl und Typ der Oberflächen sind fest. Sobald die Oberflächen erstellt wurden, kann die Anwendung sie nicht hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="8fd69-226">Jede Instanz des ISurfaceQueue-Objekts bietet eine Art einwegiger Straße, die verwendet werden kann, um Oberflächen vom erzeugenden Gerät an das verbrauchende Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="8fd69-227">Es können mehrere solcher einweggeflagten Straßen verwendet werden, um Szenarien für die gemeinsame Nutzung von Oberflächen zwischen Geräten bestimmter Anwendungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="8fd69-228">**Erstellung/Objektlebensdauer**</span><span class="sxs-lookup"><span data-stu-id="8fd69-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="8fd69-229">Es gibt zwei Möglichkeiten, das Warteschlangenobjekt zu erstellen: über CreateSurfaceQueue oder über die Clone-Methode von ISurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="8fd69-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="8fd69-230">Da es sich bei den Schnittstellen um COM-Objekte handelt, gilt die standardmäßige COM-Lebensdauerverwaltung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="8fd69-231">**Producer/Consumer-Modell**</span><span class="sxs-lookup"><span data-stu-id="8fd69-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="8fd69-232">Enqueue (): Der Producer ruft diese Funktion auf, um anzugeben, dass dies mit der Oberfläche erfolgt, die nun für ein anderes Gerät verfügbar sein kann.</span><span class="sxs-lookup"><span data-stu-id="8fd69-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="8fd69-233">Nach der Rückkehr von dieser Funktion verfügt das Producergerät nicht mehr über Rechte für die Oberfläche und ist unsicher, es weiterhin zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="8fd69-234">Aus der Queue (): Das nutzende Gerät ruft diese Funktion auf, um eine freigegebene Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="8fd69-235">Die API stellt sicher, dass alle aus der Queued- Entfernten entfernten Oberflächen für die Verwendung bereit sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="8fd69-236">**Metadaten**</span><span class="sxs-lookup"><span data-stu-id="8fd69-236">**Metadata**</span></span>  
<span data-ttu-id="8fd69-237">Die API unterstützt das Zuordnen von Metadaten zu den freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="8fd69-238">Enqueue() hat die Möglichkeit, zusätzliche Metadaten anzugeben, die an das nutzende Gerät übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="8fd69-239">Die Metadaten müssen kleiner als ein maximaler Wert sein, der zum Erstellungszeitpunkt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="8fd69-240">Dequeue() kann optional einen Puffer und einen Zeiger auf die Größe des Puffers übergeben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="8fd69-241">Die Warteschlange füllt den Puffer mit den Metadaten des entsprechenden Enqueue-Aufrufs aus.</span><span class="sxs-lookup"><span data-stu-id="8fd69-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="8fd69-242">**Klonen?**</span><span class="sxs-lookup"><span data-stu-id="8fd69-242">**Cloning**</span></span>  
<span data-ttu-id="8fd69-243">Jedes ISurfaceQueue-Objekt löst eine einseitige Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="8fd69-244">Wir gehen davon aus, dass die überwiegende Mehrheit der Anwendungen, die diese API verwenden, ein geschlossenes System verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="8fd69-245">Das einfachste geschlossene System mit zwei Geräten, die Oberflächen hin und her senden, erfordert zwei Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="8fd69-246">Das ISurfaceQueue-Objekt verfügt über eine Clone()-Methode, die es ermöglicht, mehrere Warteschlangen zu erstellen, die alle Teil derselben größeren Pipeline sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="8fd69-247">Clone erstellt ein neues ISurfaceQueue-Objekt aus einem vorhandenen Objekt und teilt alle geöffneten Ressourcen zwischen ihnen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="8fd69-248">Das resultierende Objekt verfügt über genau die gleichen Oberflächen wie die Quellwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="8fd69-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="8fd69-249">Geklonte Warteschlangen können unterschiedliche Metadatengrößen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="8fd69-250">**Surface**</span><span class="sxs-lookup"><span data-stu-id="8fd69-250">**Surfaces**</span></span>  
<span data-ttu-id="8fd69-251">ISurfaceQueue übernimmt die Verantwortung für das Erstellen und Verwalten seiner Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="8fd69-252">Es ist nicht gültig, beliebige Oberflächen in die Enqueue einzudingen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="8fd69-253">Darüber hinaus sollte eine Oberfläche nur über einen aktiven "Besitzer" verfügen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="8fd69-254">Sie sollte sich entweder in einer bestimmten Warteschlange befinden oder von einem bestimmten Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="8fd69-255">Es ist nicht zulässig, sie in mehreren Warteschlangen zu speichern oder geräte die Oberfläche nach dem Einreihen in die Warteschlange weiter zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="8fd69-256">API-Details</span><span class="sxs-lookup"><span data-stu-id="8fd69-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="8fd69-257">IsurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="8fd69-257">IsurfaceQueue</span></span>

<span data-ttu-id="8fd69-258">Die Warteschlange ist für das Erstellen und Verwalten der freigegebenen Ressourcen verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="8fd69-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="8fd69-259">Sie bietet auch die Funktionalität zum Verketten mehrerer Warteschlangen mit clone.</span><span class="sxs-lookup"><span data-stu-id="8fd69-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="8fd69-260">Die Warteschlange verfügt über Methoden, mit denen das erzeugende Gerät und ein verbrauchendes Gerät geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="8fd69-261">Es kann jeweils nur eine geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="8fd69-262">Die Warteschlange macht die folgenden APIs verfügbar:</span><span class="sxs-lookup"><span data-stu-id="8fd69-262">The queue exposes the following APIs:</span></span>



| <span data-ttu-id="8fd69-263">API</span><span class="sxs-lookup"><span data-stu-id="8fd69-263">API</span></span>                            | <span data-ttu-id="8fd69-264">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fd69-264">Description</span></span>                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8fd69-265">CreateSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="8fd69-265">CreateSurfaceQueue</span></span>          | <span data-ttu-id="8fd69-266">Erstellt ein ISurfaceQueue-Objekt (die "Root"-Warteschlange).</span><span class="sxs-lookup"><span data-stu-id="8fd69-266">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="8fd69-267">ISurfaceQueue::OpenConsumer</span><span class="sxs-lookup"><span data-stu-id="8fd69-267">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="8fd69-268">Gibt eine Schnittstelle zurück, über die das verwendende Gerät aus der Queue aus der Quequeue ausrückt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-268">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="8fd69-269">ISurfaceQueue::OpenProducer</span><span class="sxs-lookup"><span data-stu-id="8fd69-269">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="8fd69-270">Gibt eine Schnittstelle zurück, die das erzeugende Gerät in die Enqueue einträgt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-270">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="8fd69-271">ISurfaceQueue::Clone</span><span class="sxs-lookup"><span data-stu-id="8fd69-271">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="8fd69-272">Erstellt ein ISurfaceQueue-Objekt, das Oberflächen mit dem Stammwarteschlangenobjekt teilt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-272">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="8fd69-273">**CreateSurfaceQueue**</span><span class="sxs-lookup"><span data-stu-id="8fd69-273">**CreateSurfaceQueue**</span></span>  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



<span data-ttu-id="8fd69-274">**Mitglieder**</span><span class="sxs-lookup"><span data-stu-id="8fd69-274">**Members**</span></span>  

<span data-ttu-id="8fd69-275">**Breite**, **Höhe**  Die Abmessungen der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-275">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="8fd69-276">Alle freigegebenen Oberflächen müssen die gleichen Dimensionen haben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-276">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="8fd69-277">**Formatieren** Das Format der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-277">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="8fd69-278">Alle freigegebenen Oberflächen müssen das gleiche Format haben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-278">All shared surfaces must have the same format.</span></span> <span data-ttu-id="8fd69-279">Die gültigen Formate hängen von den verwendeten Geräten ab, da unterschiedliche Gerätepaare unterschiedliche Formattypen gemeinsam nutzen können.</span><span class="sxs-lookup"><span data-stu-id="8fd69-279">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="8fd69-280">**NumSurfaces**  Die Anzahl der Oberflächen, die Teil der Warteschlange sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-280">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="8fd69-281">Dies ist eine feste Zahl.</span><span class="sxs-lookup"><span data-stu-id="8fd69-281">This is a fixed number.</span></span>  
 <span data-ttu-id="8fd69-282">**MetaDataSize**  Die maximale Größe des Metadatenpuffers.</span><span class="sxs-lookup"><span data-stu-id="8fd69-282">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="8fd69-283">**Flags**  Flags zum Steuern des Verhaltens der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="8fd69-283">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="8fd69-284">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8fd69-284">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="8fd69-285">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-285">**Parameters**</span></span>

 <span data-ttu-id="8fd69-286">*pDesc* \[ in \]  Die Beschreibung der zu erstellenden freigegebenen Surface-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="8fd69-286">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="8fd69-287">*pDevice* \[ in \]  Das Gerät, das zum Erstellen der freigegebenen Oberflächen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd69-287">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="8fd69-288">Dies ist ein expliziter Parameter aufgrund eines Features in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8fd69-288">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="8fd69-289">Für Oberflächen, die von Direct3D 9 und Direct3D 10 gemeinsam genutzt werden, müssen die Oberflächen mit Direct3D 9 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-289">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="8fd69-290">*ppQueue* \[ out \]  Enthält bei rückgabe einen Zeiger auf das ISurfaceQueue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-290">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="8fd69-291">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-291">**Return Values**</span></span>

<span data-ttu-id="8fd69-292">Wenn *pDevice* nicht in der Lage ist, Ressourcen gemeinsam zu nutzen, gibt diese Funktion DXGI \_ ERROR INVALID CALL \_ \_ zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-292">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="8fd69-293">Diese Funktion erstellt die Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-293">This function creates the resources.</span></span> <span data-ttu-id="8fd69-294">Wenn ein Fehler auftritt, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-294">If it fails, it returns an error.</span></span> <span data-ttu-id="8fd69-295">Wenn dies erfolgreich ist, wird S \_ OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-295">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="8fd69-296">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-296">**Remarks**</span></span>

<span data-ttu-id="8fd69-297">Beim Erstellen des Warteschlangenobjekts werden auch alle Oberflächen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-297">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="8fd69-298">Alle Oberflächen werden als 2D-Renderziele angenommen und mit den festgelegten RESSOURCENflags D3D10 \_ BIND RENDER TARGET und \_ \_ D3D10 \_ BIND \_ SHADER RESOURCE \_ (oder den entsprechenden Flags für die verschiedenen Runtimes) erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-298">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="8fd69-299">Der Entwickler kann ein Flag angeben, das angibt, ob mehrere Threads auf die Warteschlange zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-299">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="8fd69-300">Wenn keine Flags festgelegt sind **(Flags** == 0), wird die Warteschlange von mehreren Threads verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-300">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="8fd69-301">Der Entwickler kann den Singlethreadzugriff angeben, wodurch der Synchronisierungscode deaktiviert und eine Leistungsverbesserung für diese Fälle ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-301">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="8fd69-302">Jede geklonte Warteschlange verfügt über ein eigenes Flag, sodass verschiedene Warteschlangen im System über unterschiedliche Synchronisierungssteuerelemente verfügen können.</span><span class="sxs-lookup"><span data-stu-id="8fd69-302">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="8fd69-303">**Öffnen eines Producers**</span><span class="sxs-lookup"><span data-stu-id="8fd69-303">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="8fd69-304">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-304">**Parameters**</span></span>  

<span data-ttu-id="8fd69-305">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fd69-305">*pDevice* \[in\]</span></span>  

<span data-ttu-id="8fd69-306">Das Producergerät, das Oberflächen in die Warteschlange einreiht.</span><span class="sxs-lookup"><span data-stu-id="8fd69-306">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="8fd69-307">*ppProducer* \[ out \] Gibt ein -Objekt an die Producerschnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-307">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="8fd69-308">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-308">**Return Values**</span></span>

<span data-ttu-id="8fd69-309">Wenn das Gerät keine Oberflächen freigeben kann, gibt DXGI \_ ERROR \_ INVALID CALL \_ zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-309">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="8fd69-310">**Öffnen eines Consumers**</span><span class="sxs-lookup"><span data-stu-id="8fd69-310">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="8fd69-311">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-311">**Parameters**</span></span>  
 <span data-ttu-id="8fd69-312">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fd69-312">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="8fd69-313">Das Consumergerät, das Oberflächen aus der Oberflächenwarteschlange aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-313">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="8fd69-314">*ppConsumer* \[ out \]  Gibt ein Objekt an die Consumerschnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-314">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="8fd69-315">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-315">**Return Values**</span></span>

<span data-ttu-id="8fd69-316">Wenn das Gerät keine Oberflächen freigeben kann, gibt DXGI \_ ERROR \_ INVALID CALL \_ zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-316">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="8fd69-317">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-317">**Remarks**</span></span>

<span data-ttu-id="8fd69-318">Diese Funktion öffnet alle Oberflächen in der Warteschlange für das Eingabegerät und speichert sie zwischen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-318">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="8fd69-319">Nachfolgende Aufrufe von Dequeue wechseln einfach zum Cache und müssen die Oberflächen nicht jedes Mal erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-319">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="8fd69-320">Klonen einer IDXGIXSurfaceQueue</span><span class="sxs-lookup"><span data-stu-id="8fd69-320">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="8fd69-321">**Die** **Elemente MetaDataSize** **und Flags** haben das gleiche Verhalten wie für CreateSurfaceQueue.</span><span class="sxs-lookup"><span data-stu-id="8fd69-321">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="8fd69-322">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-322">**Parameters**</span></span>

<span data-ttu-id="8fd69-323">*pDesc* \[ in Einer Struktur, die eine Beschreibung des zu \] erstellenden Klonobjekts enthält.</span><span class="sxs-lookup"><span data-stu-id="8fd69-323">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="8fd69-324">Dieser Parameter sollte initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-324">This parameter should be initialized.</span></span>  
<span data-ttu-id="8fd69-325">*ppQueue* \[ out \] Gibt das initialisierte Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-325">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="8fd69-326">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-326">**Remarks**</span></span>

<span data-ttu-id="8fd69-327">Sie können aus jedem vorhandenen Warteschlangenobjekt klonen, auch wenn es sich nicht um das Stammobjekt handelt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-327">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="8fd69-328">IDXGIXSurfaceConsumer</span><span class="sxs-lookup"><span data-stu-id="8fd69-328">IDXGIXSurfaceConsumer</span></span>

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



<span data-ttu-id="8fd69-329">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-329">**Parameters**</span></span>  
<span data-ttu-id="8fd69-330">*id* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fd69-330">*id* \[in\]</span></span>  
<span data-ttu-id="8fd69-331">Die REFIID einer 2D-Oberfläche des verbrauchten Geräts.</span><span class="sxs-lookup"><span data-stu-id="8fd69-331">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="8fd69-332">Für IDirect3DDevice9 sollte die REFIID \_ \_ uuidof(IDirect3DTexture9) sein.</span><span class="sxs-lookup"><span data-stu-id="8fd69-332">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="8fd69-333">Für eine ID3D10Device sollte die REFIID \_ \_ uuidof(ID3D10Texture2D) sein.</span><span class="sxs-lookup"><span data-stu-id="8fd69-333">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="8fd69-334">Bei einem ID3D11Device muss die REFIID \_ \_ uuidof(ID3D11Texture2D) sein.</span><span class="sxs-lookup"><span data-stu-id="8fd69-334">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="8fd69-335">*ppSurface* \[ out \] Gibt einen Zeiger auf die Oberfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-335">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="8fd69-336">*pBuffer* \[ in, out \] Ein optionaler Parameter und, wenn nicht **NULL,** enthält bei der Rückgabe die Metadaten, die beim entsprechenden Enqueue-Aufruf übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-336">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="8fd69-337">*pBufferSize* \[ in, out \] Die Größe von *pBuffer* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8fd69-337">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="8fd69-338">Gibt die Anzahl der in *pBuffer* zurückgegebenen Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="8fd69-338">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="8fd69-339">Wenn der Enqueue-Aufruf keine Metadaten bereitstellte, wird *pBuffer* auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-339">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="8fd69-340">*dwTimeout* \[ in \] Gibt einen Timeoutwert an.</span><span class="sxs-lookup"><span data-stu-id="8fd69-340">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="8fd69-341">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-341">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="8fd69-342">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-342">**Return Values**</span></span>

<span data-ttu-id="8fd69-343">Diese Funktion kann WAIT \_ TIMEOUT zurückgeben, wenn ein Timeoutwert angegeben ist und die Funktion nicht vor dem Timeoutwert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-343">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="8fd69-344">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8fd69-344">See Remarks.</span></span> <span data-ttu-id="8fd69-345">Wenn keine Oberflächen verfügbar sind, gibt die Funktion zurück, wobei *ppSurface* auf **NULL** festgelegt ist, *pBufferSize* auf 0 festgelegt ist und der Rückgabewert 0x80070120 ist (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).</span><span class="sxs-lookup"><span data-stu-id="8fd69-345">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="8fd69-346">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-346">**Remarks**</span></span>

<span data-ttu-id="8fd69-347">Diese API kann blockieren, wenn die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-347">This API can block if the queue is empty.</span></span> <span data-ttu-id="8fd69-348">Der *dwTimeout-Parameter* funktioniert identisch mit den Windows-Synchronisierungs-APIs, z. B. WaitForSingleObject.</span><span class="sxs-lookup"><span data-stu-id="8fd69-348">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="8fd69-349">Verwenden Sie für nicht blockierende Verhaltensweisen ein Timeout von 0.</span><span class="sxs-lookup"><span data-stu-id="8fd69-349">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="8fd69-350">ISurfaceProducer</span><span class="sxs-lookup"><span data-stu-id="8fd69-350">ISurfaceProducer</span></span>

<span data-ttu-id="8fd69-351">Diese Schnittstelle stellt zwei Methoden bereit, die es der App ermöglichen, Oberflächen in die Quehnung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-351">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="8fd69-352">Nachdem eine Oberfläche in die Quehen eingedrunget wurde, ist der Oberflächenzeiger nicht mehr gültig und kann nicht mehr sicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-352">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="8fd69-353">Die einzige Aktion, die die Anwendung mit dem Zeiger ausführen soll, besteht darin, sie freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8fd69-353">The only action that the application should perform with the pointer is to release it.</span></span>



| <span data-ttu-id="8fd69-354">Methode</span><span class="sxs-lookup"><span data-stu-id="8fd69-354">Method</span></span>                          | <span data-ttu-id="8fd69-355">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8fd69-355">Description</span></span>                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd69-356">ISurfaceProducer::Enqueue</span><span class="sxs-lookup"><span data-stu-id="8fd69-356">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="8fd69-357">Reiht eine Oberfläche in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="8fd69-357">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="8fd69-358">Nach Abschluss dieses Aufrufs wird der Producer mit der Oberfläche fertig, und die Oberfläche ist für ein anderes Gerät bereit.</span><span class="sxs-lookup"><span data-stu-id="8fd69-358">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="8fd69-359">ISurfaceProducer::Flush</span><span class="sxs-lookup"><span data-stu-id="8fd69-359">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="8fd69-360">Wird verwendet, wenn die Anwendungen nicht blockierend sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-360">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="8fd69-361">Einzelheiten finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-361">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="8fd69-362">**Einreihen in die Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="8fd69-362">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="8fd69-363">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-363">**Parameters**</span></span>  
<span data-ttu-id="8fd69-364">*pSurface* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fd69-364">*pSurface* \[in\]</span></span>  
<span data-ttu-id="8fd69-365">Die Oberfläche des erzeugenden Geräts, das in die Queued-Enqueuing eingeändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8fd69-365">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="8fd69-366">Diese Oberfläche muss eine Oberfläche sein, die aus dem gleichen Warteschlangennetzwerk aus der Warteschlange entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-366">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="8fd69-367">*pBuffer* \[ in \] Ein optionaler Parameter, der zum Übergeben von Metadaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-367">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="8fd69-368">Er sollte auf die Daten verweisen, die an den Dequeue-Aufruf übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-368">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="8fd69-369">*BufferSize* \[ in \] Die Größe von *pBuffer* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8fd69-369">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="8fd69-370">*Flags* \[ in \] Ein optionaler Parameter, der das Verhalten dieser Funktion steuert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-370">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="8fd69-371">Das einzige Flag ist SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="8fd69-371">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="8fd69-372">Weitere Informationen finden Sie in den Anmerkungen zu Flush.</span><span class="sxs-lookup"><span data-stu-id="8fd69-372">See the Remarks for Flush.</span></span> <span data-ttu-id="8fd69-373">Wenn kein Flag übergeben wird (*Flags* == 0), wird das standardmäßige Blockierungsverhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-373">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="8fd69-374">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-374">**Return Values**</span></span>

<span data-ttu-id="8fd69-375">Diese Funktion kann DXGI \_ ERROR WAS STILL DRAWING \_ \_ \_ zurückgeben, wenn ein SURFACE QUEUE FLAG \_ DO NOT \_ \_ \_ \_ WAIT-Flag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-375">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="8fd69-376">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-376">**Remarks**</span></span>

-   <span data-ttu-id="8fd69-377">Mit dieser Funktion wird die Oberfläche in die Warteschlange gestellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-377">This function puts the surface on the queue.</span></span> <span data-ttu-id="8fd69-378">Wenn die Anwendung SURFACE QUEUE FLAG DO NOT WAIT nicht anordnt, blockiert diese Funktion und führt eine \_ \_ \_ \_ GPU-CPU-Synchronisierung durch, um sicherzustellen, dass das gesamte Rendering auf der in die Warteschlange gestellten Oberfläche \_ abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-378">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="8fd69-379">Wenn diese Funktion erfolgreich ist, steht eine Oberfläche für das Aus der Queue zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-379">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="8fd69-380">Wenn Sie nicht blockierende Verhalten wünschen, verwenden Sie das Flag DO \_ NOT \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="8fd69-380">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="8fd69-381">Weitere Informationen finden Sie unter Flush().</span><span class="sxs-lookup"><span data-stu-id="8fd69-381">See Flush() for details.</span></span>
-   <span data-ttu-id="8fd69-382">Die von Dequeue zurückgegebene Oberfläche ist nach den COM-Verweiszählungsregeln AddRef(), sodass die Anwendung dies nicht tun muss.</span><span class="sxs-lookup"><span data-stu-id="8fd69-382">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="8fd69-383">Nach dem Aufruf von Enqueue muss die Anwendung die Oberfläche wieder frei geben, da sie sie nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-383">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="8fd69-384">**Leerung**</span><span class="sxs-lookup"><span data-stu-id="8fd69-384">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="8fd69-385">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="8fd69-385">**Parameters**</span></span>  
<span data-ttu-id="8fd69-386">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8fd69-386">*Flags* \[in\]</span></span>  
<span data-ttu-id="8fd69-387">Das einzige Flag ist SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT.</span><span class="sxs-lookup"><span data-stu-id="8fd69-387">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="8fd69-388">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8fd69-388">See Remarks.</span></span> <span data-ttu-id="8fd69-389">*nSurfaces* \[ out \] Gibt die Anzahl der Oberflächen zurück, die noch ausstehend sind und nicht geleert werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-389">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="8fd69-390">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="8fd69-390">**Return Values**</span></span>

<span data-ttu-id="8fd69-391">Diese Funktion kann DXGI \_ ERROR WAS STILL DRAWING \_ \_ \_ zurückgeben, wenn das FLAG SURFACE QUEUE \_ FLAG DO NOT WAIT verwendet \_ \_ \_ \_ wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-391">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="8fd69-392">Diese Funktion gibt S \_ OK zurück, wenn Oberflächen erfolgreich geleert wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-392">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="8fd69-393">Diese Funktion gibt DXGI ERROR WAS STILL DRAWING nur dann \_ \_ \_ \_ zurück, wenn keine Oberflächen geleert wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-393">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="8fd69-394">Zusammen geben der Rückgabewert und *nSurfaces* der Anwendung an, welche Arbeit ausgeführt wurde und ob noch Arbeit übrig ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-394">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="8fd69-395">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-395">**Remarks**</span></span>

<span data-ttu-id="8fd69-396">Die Leerung ist nur sinnvoll, wenn beim vorherigen Aufruf der Enqueue das FLAG DO NOT WAIT verwendet \_ \_ wurde. Andernfalls ist dies ein No-Op-Flag.</span><span class="sxs-lookup"><span data-stu-id="8fd69-396">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="8fd69-397">Wenn beim Aufruf der Enqueue das FLAG DO NOT WAIT verwendet wurde, wird \_ \_ die Enqueue sofort zurückgegeben, und die GPU-CPU-Synchronisierung ist nicht garantiert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-397">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="8fd69-398">Die Oberfläche gilt weiterhin als in die Enqueued-Queue eingegrenzt, das erzeugende Gerät kann sie nicht mehr verwenden, ist aber nicht für das Aussetzen aus der Queue verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8fd69-398">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="8fd69-399">Um zu versuchen, die Oberfläche für die Löschung zu committen, muss Flush aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-399">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="8fd69-400">Beim Leeren wird versucht, alle Oberflächen zu committen, die derzeit in die Quehen eingedrungen sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-400">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="8fd69-401">Wenn kein Flag an Flush übergeben wird, wird die gesamte Warteschlange blockiert und gelöscht, und alle darin stehenden Oberflächen werden für die Warteschlangenlöschung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-401">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="8fd69-402">Wenn das \_ DO NOT \_ WAIT-Flag verwendet wird, überprüft die Warteschlange die Oberflächen, um festzustellen, ob eine davon bereit ist. Dieser Schritt ist nicht blockierend.</span><span class="sxs-lookup"><span data-stu-id="8fd69-402">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="8fd69-403">Oberflächen, die die GPU-CPU-Synchronisierung abgeschlossen haben, sind für das Consumergerät bereit.</span><span class="sxs-lookup"><span data-stu-id="8fd69-403">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="8fd69-404">Oberflächen, die noch ausstehen, sind davon nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-404">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="8fd69-405">Die Funktion gibt die Anzahl der Oberflächen zurück, die noch geleert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-405">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="8fd69-406">Durch die Leerung wird die Warteschlangensemantik nicht unterbricht.</span><span class="sxs-lookup"><span data-stu-id="8fd69-406">Flush will not break the queue semantics.</span></span> <span data-ttu-id="8fd69-407">Die API garantiert, dass oberflächen, die zuerst in die Quehen eingedred wurden, ein Commit ausgeführt werden, bevor Oberflächen später in die Quehen gestellt werden, unabhängig davon, wann die GPU-CPU-Synchronisierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-407">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="8fd69-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span><span class="sxs-lookup"><span data-stu-id="8fd69-408">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="8fd69-409">Wir gehen davon aus, dass die meisten Anwendungsfälle zwei Geräte umfassen, die eine Reihe von Oberflächen gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-409">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="8fd69-410">Da dies auch das einfachste Szenario ist, wird in diesem Dokument erläutert, wie sie die APIs verwenden, um dieses Ziel zu erreichen, eine nicht blockierende Variante erläutert und mit einem kurzen Abschnitt zur Initialisierung für drei Geräte endet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-410">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="8fd69-411">Zwei Geräte</span><span class="sxs-lookup"><span data-stu-id="8fd69-411">Two Devices</span></span>

<span data-ttu-id="8fd69-412">Die Beispielanwendung, die dieses Hilfs verwendet, kann Direct3D 9Ex und Direct3D 11 zusammen verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-412">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="8fd69-413">Die Anwendung kann Inhalte mit beiden Geräten verarbeiten und Inhalte mit Direct3D 9 präsentieren.</span><span class="sxs-lookup"><span data-stu-id="8fd69-413">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="8fd69-414">Die Verarbeitung kann das Rendern von Inhalten, das Decodieren von Videos, das Ausführen von Compute-Shadern und so weiter bedeuten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-414">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="8fd69-415">Für jeden Frame wird die Anwendung zuerst mit Direct3D 11, dann mit Direct3D 9 und schließlich mit Direct3D 9 verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-415">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="8fd69-416">Darüber hinaus erzeugt die Verarbeitung mit Direct3D 11 einige Metadaten, die die direct3D 9-Datei nutzen muss.</span><span class="sxs-lookup"><span data-stu-id="8fd69-416">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="8fd69-417">In diesem Abschnitt wird die Verwendung des Hilfsers in drei Teilen behandelt, die dieser Sequenz entsprechen: Initialisierung, Hauptschleife und Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-417">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="8fd69-418">**Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="8fd69-418">**Initialization**</span></span>  
<span data-ttu-id="8fd69-419">Die Initialisierung umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="8fd69-419">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="8fd69-420">Initialisieren Sie beide Geräte.</span><span class="sxs-lookup"><span data-stu-id="8fd69-420">Initialize both devices.</span></span>
2.  <span data-ttu-id="8fd69-421">Erstellen Sie die Stammwarteschlange m \_ 11to9Queue.</span><span class="sxs-lookup"><span data-stu-id="8fd69-421">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="8fd69-422">Klonen aus der Stammwarteschlange: m \_ 9to11Queue.</span><span class="sxs-lookup"><span data-stu-id="8fd69-422">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="8fd69-423">Rufen Sie OpenProducer/OpenConsumer in beiden Warteschlangen auf.</span><span class="sxs-lookup"><span data-stu-id="8fd69-423">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="8fd69-424">Die Warteschlangennamen verwenden die Zahlen 9 und 11, um anzugeben, welche API der Producer und welcher der Consumer ist: **m \_**_producer_*_to_*_consumer_*_Queue_*.</span><span class="sxs-lookup"><span data-stu-id="8fd69-424">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_**_producer_*_to_*_consumer_*_Queue_*.</span></span> <span data-ttu-id="8fd69-425">m 11to9Queue gibt entsprechend eine Warteschlange an, für die das Direct3D 11-Gerät Oberflächen erzeugt, die das \_ Direct3D 9-Gerät verbraucht.</span><span class="sxs-lookup"><span data-stu-id="8fd69-425">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="8fd69-426">Entsprechend gibt m 9to11Queue eine Warteschlange an, für die Direct3D 9 Oberflächen erzeugt, die \_ Direct3D 11 verbraucht.</span><span class="sxs-lookup"><span data-stu-id="8fd69-426">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="8fd69-427">Die Stammwarteschlange ist anfänglich voll, und alle geklonten Warteschlangen sind anfänglich leer.</span><span class="sxs-lookup"><span data-stu-id="8fd69-427">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="8fd69-428">Dies sollte kein Problem für die Anwendung sein, mit Ausnahme des ersten Zyklus der Enqueues und Dequeues und der Verfügbarkeit von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-428">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="8fd69-429">Wenn ein Aus der Enqueue nach Metadaten fragt, aber keine festgelegt wurden (entweder weil anfänglich nichts enthalten ist oder die Enqueue nichts festgelegt hat), erkennt das Aus der Enqueue, dass keine Metadaten empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-429">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="8fd69-430">**Initialisieren Sie beide Geräte.**</span><span class="sxs-lookup"><span data-stu-id="8fd69-430">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="8fd69-431">**Erstellen Sie die Stammwarteschlange.**</span><span class="sxs-lookup"><span data-stu-id="8fd69-431">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="8fd69-432">In diesem Schritt werden auch die Oberflächen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-432">This step also creates the surfaces.</span></span> <span data-ttu-id="8fd69-433">Größen- und Formateinschränkungen sind identisch mit dem Erstellen einer beliebigen freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="8fd69-433">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="8fd69-434">Die Größe des Metadatenpuffers wird zum Erstellungszeitpunkt festgelegt, und in diesem Fall übergeben wir lediglich einen UINT.</span><span class="sxs-lookup"><span data-stu-id="8fd69-434">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="8fd69-435">Die Warteschlange muss mit einer festen Anzahl von Oberflächen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-435">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="8fd69-436">Die Leistung variiert je nach Szenario.</span><span class="sxs-lookup"><span data-stu-id="8fd69-436">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="8fd69-437">Mehrere Oberflächen erhöhen die Wahrscheinlichkeit, dass Geräte ausgelastet sind.</span><span class="sxs-lookup"><span data-stu-id="8fd69-437">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="8fd69-438">Wenn es beispielsweise nur eine Oberfläche gibt, gibt es keine Parallelisierung zwischen den beiden Geräten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-438">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="8fd69-439">Andererseits erhöht die Erhöhung der Anzahl von Oberflächen den Speicherbedarf, was die Leistung beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="8fd69-439">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="8fd69-440">In diesem Beispiel werden zwei Oberflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8fd69-440">This example uses two surfaces.</span></span>  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  <span data-ttu-id="8fd69-441">**Klonen Sie die Stammwarteschlange.**</span><span class="sxs-lookup"><span data-stu-id="8fd69-441">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="8fd69-442">Jede geklonte Warteschlange muss die gleichen Oberflächen verwenden, kann jedoch unterschiedliche Metadatenpuffergrößen und unterschiedliche Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-442">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="8fd69-443">In diesem Fall sind keine Metadaten von Direct3D 9 zu Direct3D 11 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-443">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="8fd69-444">**Öffnen Sie die Producer- und Consumergeräte.**</span><span class="sxs-lookup"><span data-stu-id="8fd69-444">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="8fd69-445">Die Anwendung muss diesen Schritt ausführen, bevor Enqueue und Dequeue aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-445">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="8fd69-446">Beim Öffnen eines Producers und Consumers werden Schnittstellen zurückgegeben, die die Enqueue/Dequeue-APIs enthalten.</span><span class="sxs-lookup"><span data-stu-id="8fd69-446">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="8fd69-447">**Hauptschleife**</span><span class="sxs-lookup"><span data-stu-id="8fd69-447">**Main Loop**</span></span>  
<span data-ttu-id="8fd69-448">Die Verwendung der Warteschlange wird nach dem klassischen Producer-Consumer-Problem modelliert.</span><span class="sxs-lookup"><span data-stu-id="8fd69-448">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="8fd69-449">Stellen Sie sich dies aus Geräteperspektive vor.</span><span class="sxs-lookup"><span data-stu-id="8fd69-449">Think of this from a per-device perspective.</span></span> <span data-ttu-id="8fd69-450">Jedes Gerät muss die folgenden Schritte ausführen: aus der Warteschlange ausreihen, um eine Oberfläche aus der Warteschlange zu erhalten, auf der Oberfläche zu verarbeiten und dann in die Produktionswarteschlange einzureihen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-450">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="8fd69-451">Für das Direct3D 11-Gerät ist die Verwendung von Direct3D 9 nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="8fd69-451">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



<span data-ttu-id="8fd69-452">**Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="8fd69-452">**Cleaning Up**</span></span>  
<span data-ttu-id="8fd69-453">Dieser Schritt ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="8fd69-453">This step is very straightforward.</span></span> <span data-ttu-id="8fd69-454">Zusätzlich zu den normalen Schritten zum Bereinigen von Direct3D-APIs muss die Anwendung die rückgaben COM-Schnittstellen veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-454">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="8fd69-455">Nicht blockierende Verwendung</span><span class="sxs-lookup"><span data-stu-id="8fd69-455">Non-Blocking Use</span></span>

<span data-ttu-id="8fd69-456">Das vorherige Beispiel ist für einen Multithread-Verwendungsfall sinnvoll, bei dem jedes Gerät über einen eigenen Thread verfügt.</span><span class="sxs-lookup"><span data-stu-id="8fd69-456">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="8fd69-457">Im Beispiel werden die blockierenden Versionen der APIs verwendet: INFINITE für Timeout und kein Flag zum Einsperren in die Enqueue.</span><span class="sxs-lookup"><span data-stu-id="8fd69-457">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="8fd69-458">Wenn Sie das Hilfsfeld auf nicht blockierende Weise verwenden möchten, müssen Sie nur wenige Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-458">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="8fd69-459">In diesem Abschnitt wird die nicht blockierende Verwendung mit beiden Geräten in einem Thread veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8fd69-459">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="8fd69-460">**Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="8fd69-460">**Initialization**</span></span>  
<span data-ttu-id="8fd69-461">Die Initialisierung ist mit Ausnahme der Flags identisch.</span><span class="sxs-lookup"><span data-stu-id="8fd69-461">Initialization is identical except for the flags.</span></span> <span data-ttu-id="8fd69-462">Da die Anwendung singlethreaded ist, verwenden Sie dieses Flag für die Erstellung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-462">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="8fd69-463">Dadurch wird ein Teil des Synchronisierungscodes deaktiviert, wodurch die Leistung möglicherweise verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-463">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



<span data-ttu-id="8fd69-464">Das Öffnen der Producer- und Consumergeräte ist mit dem im Blockierungsbeispiel identisch.</span><span class="sxs-lookup"><span data-stu-id="8fd69-464">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="8fd69-465">**Verwenden der Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="8fd69-465">**Using the Queue**</span></span>  
<span data-ttu-id="8fd69-466">Es gibt viele Möglichkeiten, die Warteschlange auf nicht blockierende Weise mit verschiedenen Leistungsmerkmalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-466">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="8fd69-467">Das folgende Beispiel ist einfach, hat jedoch aufgrund übermäßiger Spin- und Abrufe eine schlechte Leistung.</span><span class="sxs-lookup"><span data-stu-id="8fd69-467">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="8fd69-468">Trotz dieser Probleme zeigt das Beispiel die Verwendung des Hilfsers.</span><span class="sxs-lookup"><span data-stu-id="8fd69-468">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="8fd69-469">Der Ansatz besteht in der kontinuierlichen Schleife und dem Aussetzen, Verarbeiten, Ein- und Leeren in die Quege.</span><span class="sxs-lookup"><span data-stu-id="8fd69-469">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="8fd69-470">Wenn einer der Schritte fehlschlägt, weil die Ressource nicht verfügbar ist, versucht die Anwendung einfach erneut, die nächste Schleife zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fd69-470">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



<span data-ttu-id="8fd69-471">Eine komplexere Lösung könnte den Rückgabewert aus der Enqueue und der Leerung überprüfen, um festzustellen, ob eine Leerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8fd69-471">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="8fd69-472">Drei Geräte</span><span class="sxs-lookup"><span data-stu-id="8fd69-472">Three Devices</span></span>

<span data-ttu-id="8fd69-473">Die Erweiterung der vorherigen Beispiele auf mehrere Geräte ist einfach.</span><span class="sxs-lookup"><span data-stu-id="8fd69-473">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="8fd69-474">Der folgende Code führt die Initialisierung aus.</span><span class="sxs-lookup"><span data-stu-id="8fd69-474">The following code performs the initialization.</span></span> <span data-ttu-id="8fd69-475">Nachdem die Producer/Consumer-Objekte erstellt wurden, ist der Code für deren Verwendung identisch.</span><span class="sxs-lookup"><span data-stu-id="8fd69-475">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="8fd69-476">Dieses Beispiel enthält drei Geräte und somit drei Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-476">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="8fd69-477">Oberflächen fließen von Direct3D 9 zu Direct3D 10 zu Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8fd69-477">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



<span data-ttu-id="8fd69-478">Wie bereits erwähnt, funktioniert das Klonen auf die gleiche Weise, unabhängig davon, welche Warteschlange geklont wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-478">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="8fd69-479">Beispielsweise könnte der zweite Clone-Aufruf aus dem m \_ 9to10Queue-Objekt entfernt worden sein.</span><span class="sxs-lookup"><span data-stu-id="8fd69-479">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a><span data-ttu-id="8fd69-480">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8fd69-480">Conclusion</span></span>

<span data-ttu-id="8fd69-481">Sie können Lösungen erstellen, die Interoperabilität verwenden, um die Leistungsfähigkeit mehrerer DirectX-APIs zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="8fd69-481">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="8fd69-482">Die Interoperabilität der Windows-Grafik-API bietet jetzt eine allgemeine Surface Management Runtime DXGI 1.1.</span><span class="sxs-lookup"><span data-stu-id="8fd69-482">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="8fd69-483">Diese Runtime ermöglicht die Unterstützung der synchronisierten Oberflächenfreigabe in neu entwickelten APIs wie Direct3D 11, Direct3D 10.1 und Direct2D.</span><span class="sxs-lookup"><span data-stu-id="8fd69-483">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="8fd69-484">Interoperabilitätsverbesserungen zwischen neuen APIs und vorhandenen APIs unterstützen die Anwendungsmigration und Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="8fd69-484">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="8fd69-485">Direct3D 9Ex- und DXGI 1.1-Consumer-APIs können zusammenarbeiten, wie mit dem Synchronisierungsmechanismus gezeigt, der über Beispielhilfscode im MSDN Code Gallery bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fd69-485">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 