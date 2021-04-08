---
title: Oberflächenfreigabe für Windows Graphics-APIs
description: Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächen Freigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730761"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a><span data-ttu-id="2dce6-103">Oberflächenfreigabe für Windows Graphics-APIs</span><span class="sxs-lookup"><span data-stu-id="2dce6-103">Surface Sharing Between Windows Graphics APIs</span></span>

<span data-ttu-id="2dce6-104">Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächen Freigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="2dce6-104">This topic provides a technical overview of interoperability using surface sharing between Windows graphics APIs, including Direct3D 11, Direct2D, DirectWrite, Direct3D 10, and Direct3D 9Ex.</span></span> <span data-ttu-id="2dce6-105">Wenn Sie bereits über Kenntnisse dieser APIs verfügen, kann dieses Whitepaper Ihnen helfen, mehrere APIs zu verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, dieselbe Oberfläche zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-105">If you already have a working knowledge of these APIs, this paper can help you use multiple APIs to render to the same surface in an application designed for the Windows 7 or Windows Vista operating systems.</span></span> <span data-ttu-id="2dce6-106">Dieses Thema enthält außerdem Richtlinien für bewährte Methoden und Zeiger auf Weitere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-106">This topic also provides best practice guidelines and pointers to additional resources.</span></span>

> [!Note]  
> <span data-ttu-id="2dce6-107">Für Direct2D-und DirectWrite-Interoperabilität in der DirectX 11,1-Laufzeit können Sie [Direct2D-Geräte und-Geräte Kontexte](/windows/desktop/Direct2D/devices-and-device-contexts) verwenden, um direkt auf Direct3D 11-Geräten zu gereinigen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-107">For Direct2D and DirectWrite interoperability on the DirectX 11.1 runtime, you can use [Direct2D devices and device contexts](/windows/desktop/Direct2D/devices-and-device-contexts) to render directly to Direct3D 11 devices.</span></span>

 

<span data-ttu-id="2dce6-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="2dce6-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2dce6-109">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="2dce6-109">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2dce6-110">Übersicht über API-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="2dce6-110">API Interoperability Overview</span></span>](#api-interoperability-overview)
-   [<span data-ttu-id="2dce6-111">Interoperabilitäts Szenarien</span><span class="sxs-lookup"><span data-stu-id="2dce6-111">Interoperability Scenarios</span></span>](#interoperability-scenarios)
    -   [<span data-ttu-id="2dce6-112">Direct3D 10,1 Geräte Freigabe mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="2dce6-112">Direct3D 10.1 Device Sharing with Direct2D</span></span>](#direct3d-101-device-sharing-with-direct2d)
    -   [<span data-ttu-id="2dce6-113">DXGI 1,1 synchronisierte freigegebene Oberflächen</span><span class="sxs-lookup"><span data-stu-id="2dce6-113">DXGI 1.1 Synchronized Shared Surfaces</span></span>](#dxgi-11-synchronized-shared-surfaces)
    -   [<span data-ttu-id="2dce6-114">Interoperabilität zwischen Direct3D 9Ex und DXGI-basierten APIs</span><span class="sxs-lookup"><span data-stu-id="2dce6-114">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [<span data-ttu-id="2dce6-115">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2dce6-115">Conclusion</span></span>](#conclusion)

## <a name="introduction"></a><span data-ttu-id="2dce6-116">Einführung</span><span class="sxs-lookup"><span data-stu-id="2dce6-116">Introduction</span></span>

<span data-ttu-id="2dce6-117">In diesem Dokument bezieht sich die Interoperabilität der Windows-Grafik-API auf die gemeinsame Nutzung derselben Renderingoberfläche durch verschiedene APIs.</span><span class="sxs-lookup"><span data-stu-id="2dce6-117">In this document, Windows graphics API interoperability refers to the sharing of the same rendering surface by different APIs.</span></span> <span data-ttu-id="2dce6-118">Diese Art von Interoperabilität ermöglicht es Anwendungen, überzeugende Anzeigen durch Nutzung mehrerer Windows-Grafik-APIs zu erstellen und die Migration zu neuen Technologien zu vereinfachen, indem die Kompatibilität mit vorhandenen APIs gewahrt bleibt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-118">This kind of interoperability enables applications to create compelling displays by leveraging multiple Windows graphics APIs, and to ease migration to new technologies by maintaining compatibility with existing APIs.</span></span>

<span data-ttu-id="2dce6-119">In Windows 7 (und Windows Vista SP2 mit Windows 7 Interop Pack, Vista 7ip) sind die Grafik Rendering-APIs Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9c und frühere Direct3D-APIs sowie GDI und GDI+.</span><span class="sxs-lookup"><span data-stu-id="2dce6-119">In Windows 7 (and Windows Vista SP2 with Windows 7 Interop Pack, Vista 7IP), the graphics rendering APIs are Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c and earlier Direct3D APIs, as well GDI and GDI+.</span></span> <span data-ttu-id="2dce6-120">Windows Imaging Component (WIC) und DirectWrite sind verwandte Technologien für die Bildverarbeitung, und Direct2D führt Text Rendering aus.</span><span class="sxs-lookup"><span data-stu-id="2dce6-120">Windows Imaging Component (WIC) and DirectWrite are related technologies for image processing, and Direct2D performs text rendering.</span></span> <span data-ttu-id="2dce6-121">Die DirectX-Videobeschleunigung-API (DXVA), die auf Direct3D 9c und Direct3D 9Ex basiert, wird für die Video Verarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-121">DirectX Video Acceleration API (DXVA), based on Direct3D 9c and Direct3D 9Ex, is used for video processing.</span></span>

<span data-ttu-id="2dce6-122">Da sich Windows-Grafik-APIs in Bezug auf Direct3D entwickeln, investiert Microsoft mehr Aufwand, um Interoperabilität über APIs hinweg zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-122">As Windows graphics APIs evolve towards being Direct3D-based, Microsoft is investing more effort in ensuring interoperability across APIs.</span></span> <span data-ttu-id="2dce6-123">Neu entwickelte Direct3D-APIs und APIs auf höherer Ebene, die auf Direct3D-APIs basieren, bieten auch Unterstützung für die Überbrückung der Kompatibilität mit älteren APIs.</span><span class="sxs-lookup"><span data-stu-id="2dce6-123">Newly developed Direct3D APIs and higher level APIs based on Direct3D APIs also provide support where needed for bridging compatibility with older APIs.</span></span> <span data-ttu-id="2dce6-124">Zur Veranschaulichung können Direct2D-Anwendungen Direct3D 10,1 verwenden, indem Sie ein Direct3D 10,1-Gerät freigeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-124">To illustrate, Direct2D applications can use Direct3D 10.1 by sharing a Direct3D 10.1 device.</span></span> <span data-ttu-id="2dce6-125">Außerdem können die APIs Direct3D 11, Direct2D und Direct3D 10,1 die DirectX Graphics Infrastructure (DXGI) 1,1 nutzen, wodurch synchronisierte freigegebene Oberflächen aktiviert werden, die die Interoperabilität zwischen diesen APIs vollständig unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-125">Also, Direct3D 11, Direct2D, and Direct3D 10.1 APIs can all take advantage of DirectX Graphics Infrastructure (DXGI) 1.1, which enables synchronized shared surfaces that fully support interoperability among these APIs.</span></span> <span data-ttu-id="2dce6-126">DXGI 1,1-basierte APIs interagieren mit GDI und mit GDI+ by Association, indem Sie den GDI-Gerätekontext von einer DXGI 1,1-Oberfläche abrufen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-126">DXGI 1.1-based APIs interoperate with GDI, and with GDI+ by association, by obtaining the GDI device context from a DXGI 1.1 surface.</span></span> <span data-ttu-id="2dce6-127">Weitere Informationen finden Sie in der DXGI-und GDI-Interoperabilitäts Dokumentation auf MSDN.</span><span class="sxs-lookup"><span data-stu-id="2dce6-127">For more information, see the DXGI and GDI interoperability documentation available on MSDN.</span></span>

<span data-ttu-id="2dce6-128">Nicht synchronisierte Oberflächen Freigabe wird von der Direct3D 9Ex-Laufzeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-128">Unsynchronized surface sharing is supported by the Direct3D 9Ex runtime.</span></span> <span data-ttu-id="2dce6-129">Auf DXVA basierende Videoanwendungen können das Direct3D 9Ex-und DXGI-Interoperabilitäts Hilfsprogramm für die Direct3D 9Ex-basierte DXVA-Interoperabilität mit Direct3D 11 für den Compute-Shader verwenden, oder Sie können mit Direct2D für 2D-Steuerelemente oder Text Rendering interagieren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-129">DXVA-based video applications can use the Direct3D 9Ex and DXGI interoperability helper for Direct3D 9Ex-based DXVA interoperability with Direct3D 11 for compute shader, or can interoperate with Direct2D for 2D controls or text rendering.</span></span> <span data-ttu-id="2dce6-130">WIC und DirectWrite interagieren auch mit GDI, Direct2D und by Association, anderen Direct3D-APIs.</span><span class="sxs-lookup"><span data-stu-id="2dce6-130">WIC and DirectWrite also interoperate with GDI, Direct2D, and by association, other Direct3D APIs.</span></span>

<span data-ttu-id="2dce6-131">Direct3D 10,0, Direct3D 9c und ältere Direct3D-Laufzeiten unterstützen keine freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-131">Direct3D 10.0, Direct3D 9c, and older Direct3D runtimes do not support shared surfaces.</span></span> <span data-ttu-id="2dce6-132">System Speicher Kopien werden weiterhin für die Interoperabilität mit GDI-oder DXGI-basierten APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-132">System memory copies will continue to be used for interoperability with GDI or DXGI-based APIs.</span></span>

<span data-ttu-id="2dce6-133">Beachten Sie, dass die Interoperabilitäts Szenarien in diesem Dokument auf mehrere Grafiken-APIs verweisen, die auf eine freigegebene Renderingoberfläche und nicht auf das gleiche Anwendungsfenster rendern.</span><span class="sxs-lookup"><span data-stu-id="2dce6-133">Note that the interoperability scenarios within this document refer to multiple graphics APIs rendering to a shared rendering surface, rather than to the same application window.</span></span> <span data-ttu-id="2dce6-134">Die Synchronisierung für separate APIs, die auf verschiedene Oberflächen abzielen, die anschließend in das gleiche Fenster zusammengesetzt werden, liegt außerhalb des Umfangs dieses Papiers.</span><span class="sxs-lookup"><span data-stu-id="2dce6-134">Synchronization for separate APIs targeting different surfaces that are then composited onto the same window is outside the scope of this paper.</span></span>

## <a name="api-interoperability-overview"></a><span data-ttu-id="2dce6-135">Übersicht über API-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="2dce6-135">API Interoperability Overview</span></span>

<span data-ttu-id="2dce6-136">Die Interoperabilität der Oberflächen Freigabe von Windows-Grafik-APIs kann in Bezug auf API-zu-API-Szenarien und die entsprechenden Interoperabilitäts Funktionen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-136">Surface sharing interoperability of Windows graphics APIs can be described in terms of API-to-API scenarios and the corresponding interoperability functionality.</span></span> <span data-ttu-id="2dce6-137">Ab Windows 7 und ab Windows Vista SP2 mit 7ip enthalten neue APIs und zugehörige Laufzeiten Direct2D und verwandte Technologien: Direct3D 11 und DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="2dce6-137">As of Windows 7 and beginning with Windows Vista SP2 with 7IP, new APIs and associated runtimes include Direct2D and related technologies: Direct3D 11 and DXGI 1.1.</span></span> <span data-ttu-id="2dce6-138">Die GDI-Leistung wurde in Windows 7 ebenfalls verbessert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-138">GDI performance was also improved in Windows 7.</span></span> <span data-ttu-id="2dce6-139">Direct3D 10,1 wurde in Windows Vista SP1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-139">Direct3D 10.1 was introduced in Windows Vista SP1.</span></span> <span data-ttu-id="2dce6-140">Das folgende Diagramm zeigt die Interoperabilitäts Unterstützung zwischen APIs.</span><span class="sxs-lookup"><span data-stu-id="2dce6-140">The following diagram shows the interoperability support between APIs.</span></span>

![Diagramm der Interoperabilitäts Unterstützung zwischen Windows-Grafik-APIs](images/surface-sharing-interoperability.png)

<span data-ttu-id="2dce6-142">In diesem Diagramm zeigen Pfeile Interoperabilitäts Szenarien, in denen die verbundenen APIs auf die gleiche Oberfläche zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2dce6-142">In this diagram, arrows show interoperability scenarios in which the same surface can be accessible by the connected APIs.</span></span> <span data-ttu-id="2dce6-143">Blaue Pfeile weisen auf die in Windows Vista eingeführten Interoperabilitäts Mechanismen hin.</span><span class="sxs-lookup"><span data-stu-id="2dce6-143">Blue arrows indicate interoperability mechanisms introduced in Windows Vista.</span></span> <span data-ttu-id="2dce6-144">Grüne Pfeile zeigen die Interoperabilitäts Unterstützung für neue APIs oder Verbesserungen an, die älteren APIs helfen, mit neueren APIs zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-144">Green arrows indicate interoperability support for new APIs or improvements that help older APIs to interoperate with newer APIs.</span></span> <span data-ttu-id="2dce6-145">Grüne Pfeile stellen z. b. die Geräte Freigabe, synchronisierte Shared Surface-Unterstützung, Direct3D 9Ex/DXGI-Synchronisierungs Hilfe und das Abrufen eines GDI-Geräte Kontexts von einer kompatiblen Oberfläche dar.</span><span class="sxs-lookup"><span data-stu-id="2dce6-145">For example, green arrows represent device sharing, synchronized shared surface support, Direct3D 9Ex/DXGI synchronization helper, and obtaining a GDI device context from a compatible surface.</span></span>

## <a name="interoperability-scenarios"></a><span data-ttu-id="2dce6-146">Interoperabilitäts Szenarien</span><span class="sxs-lookup"><span data-stu-id="2dce6-146">Interoperability Scenarios</span></span>

<span data-ttu-id="2dce6-147">Ab Windows 7 und Windows Vista 7ip unterstützen die gängigen Angebote von Windows-Grafik-APIs das Rendering mehrerer APIs zur gleichen DXGI 1,1-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2dce6-147">As of Windows 7 and Windows Vista 7IP, mainstream offerings from Windows graphics APIs support multiple APIs rendering to the same DXGI 1.1 surface.</span></span>

<span data-ttu-id="2dce6-148">**Direct3D 11, Direct3D 10,1, Direct2D – Interoperabilität untereinander**</span><span class="sxs-lookup"><span data-stu-id="2dce6-148">**Direct3D 11, Direct3D 10.1, Direct2D — Interoperability with each other**</span></span>

<span data-ttu-id="2dce6-149">Direct3D 11-, Direct3D 10,1-und Direct2D-APIs (und die zugehörigen APIs wie DirectWrite und WIC) können miteinander interagieren, indem Sie entweder die Freigabe von Direct3D 10,1-Geräten oder synchronisierte freigegebene Oberflächen verwenden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-149">Direct3D 11, Direct3D 10.1 and Direct2D APIs (and its related APIs such as DirectWrite and WIC) can interoperate with each other using either Direct3D 10.1 device sharing or synchronized shared surfaces.</span></span>

### <a name="direct3d-101-device-sharing-with-direct2d"></a><span data-ttu-id="2dce6-150">Direct3D 10,1 Geräte Freigabe mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="2dce6-150">Direct3D 10.1 Device Sharing with Direct2D</span></span>

<span data-ttu-id="2dce6-151">Die Geräte Freigabe zwischen Direct2D und Direct3D 10,1 ermöglicht es einer Anwendung, beide APIs zu verwenden, um nahtlos und effizient auf derselben DXGI 1,1-Oberfläche zu renderarbeiten, wobei dasselbe zugrunde liegende Direct3D-Geräte Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-151">Device sharing between Direct2D and Direct3D 10.1 allows an application to use both APIs to seamlessly and efficiently render onto the same DXGI 1.1 surface, using the same underlying Direct3D device object.</span></span> <span data-ttu-id="2dce6-152">Direct2D bietet die Möglichkeit, Direct2D-APIs über ein vorhandenes Direct3D 10,1-Gerät aufzurufen. dabei wird die Tatsache genutzt, dass Direct2D auf Direct3D 10,1-und DXGI 1,1-Laufzeiten aufbaut.</span><span class="sxs-lookup"><span data-stu-id="2dce6-152">Direct2D provides the ability to call Direct2D APIs using an existing Direct3D 10.1 device, leveraging the fact that Direct2D is built on top of Direct3D 10.1 and DXGI 1.1 runtimes.</span></span> <span data-ttu-id="2dce6-153">Die folgenden Code Ausschnitte veranschaulichen, wie Direct2D das Direct3D 10,1 Device-Renderziel von einer DXGI 1,1-Oberfläche erhält, die dem Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-153">The following code snippets illustrate how Direct2D obtains the Direct3D 10.1 device render target from a DXGI 1.1 surface associated with the device.</span></span> <span data-ttu-id="2dce6-154">Das Direct3D 10,1-geräterrenderziel kann Direct2D-Zeichnungs Aufrufe zwischen beginDraw-und EndDraw-APIs ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-154">The Direct3D 10.1 device render target can execute Direct2D drawing calls between BeginDraw and EndDraw APIs.</span></span>


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



<span data-ttu-id="2dce6-155">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-155">**Remarks**</span></span>

-   <span data-ttu-id="2dce6-156">Das zugehörige Direct3D 10,1-Gerät muss das BGRA-Format unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-156">The associated Direct3D 10.1 device must support BGRA format.</span></span> <span data-ttu-id="2dce6-157">Dieses Gerät wurde durch Aufrufen von D3D10CreateDevice1 mit dem Parameter \_ d3d10 \_ \_ BGRA- \_ Unterstützung für das Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-157">That device was created by calling D3D10CreateDevice1 with parameter D3D10\_CREATE\_DEVICE\_BGRA\_SUPPORT.</span></span> <span data-ttu-id="2dce6-158">Das BGRA-Format wird ab Direct3D 10-Featureebene 9,1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-158">BGRA format is supported starting with Direct3D 10 feature level 9.1.</span></span>
-   <span data-ttu-id="2dce6-159">Die Anwendung sollte nicht mehrere ID2D1RenderTargets erstellen, die demselben Direct3D 10.1-Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-159">The application should not create multiple ID2D1RenderTargets associating to the same Direct3D10.1 device.</span></span>
-   <span data-ttu-id="2dce6-160">Um eine optimale Leistung zu erzielen, sollten Sie mindestens eine Ressource jederzeit herum aufbewahren, z. b. Texturen oder Oberflächen, die dem Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-160">For optimal performance, keep at least one resource around at all times, such as textures or surfaces associated with the device.</span></span>

<span data-ttu-id="2dce6-161">Die Geräte Freigabe eignet sich für die Prozess interne, Single Thread-Verwendung eines renderinggeräts, das von den Direct3D 10,1-und Direct2D-Rendering-APIs gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-161">Device sharing is suitable for in-process, single-threaded usage of one rendering device shared by both Direct3D 10.1 and Direct2D rendering APIs.</span></span> <span data-ttu-id="2dce6-162">Synchronisierte freigegebene Oberflächen ermöglichen Multithread-, Prozess interne und prozessübergreifende Verwendung mehrerer renderinggeräte, die von Direct3D 10,1-, Direct2D-und Direct3D 11-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-162">Synchronized shared surfaces enable multi-threaded, in-process and out-of-process usage of multiple rendering devices used by Direct3D 10.1, Direct2D and Direct3D 11 APIs.</span></span>

<span data-ttu-id="2dce6-163">Eine weitere Methode der Direct3D 10,1-und Direct2D-Interoperabilität ist die Verwendung von ID3D1RenderTarget:: foatesharedbitmap, die ein ID2D1Bitmap-Objekt aus idxgisurface erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-163">Another method of Direct3D 10.1 and Direct2D interoperability is by using ID3D1RenderTarget::CreateSharedBitmap, which creates an ID2D1Bitmap object from IDXGISurface.</span></span> <span data-ttu-id="2dce6-164">Sie können eine Direct3D 10.1-Szene in die Bitmap schreiben und Sie mit Direct2D Rendering.</span><span class="sxs-lookup"><span data-stu-id="2dce6-164">You can write a Direct3D10.1 scene to the bitmap and render it with Direct2D.</span></span> <span data-ttu-id="2dce6-165">Weitere Informationen finden Sie unter [ID2D1RenderTarget:: kreatesharedbitmap-Methode](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span><span class="sxs-lookup"><span data-stu-id="2dce6-165">For more information, see [ID2D1RenderTarget::CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).</span></span>

### <a name="direct2d-software-rasterization"></a><span data-ttu-id="2dce6-166">Direct2D Software rasterization</span><span class="sxs-lookup"><span data-stu-id="2dce6-166">Direct2D Software Rasterization</span></span>

<span data-ttu-id="2dce6-167">Die Geräte Freigabe mit Direct3D 10,1 wird nicht unterstützt, wenn der Software-Renderer Direct2D verwendet wird, z. b. durch Angeben von D2D1 \_ \_ \_ \_ Renderziel-Verwendungs Erzwingen von \_ Software \_ Rendering in D2D1 \_ renderzielverwendung \_ \_ beim Erstellen eines Direct2D Renderziels.</span><span class="sxs-lookup"><span data-stu-id="2dce6-167">Device sharing with Direct3D 10.1 is not supported when using the Direct2D software renderer, for example, by specifying D2D1\_RENDER\_TARGET\_USAGE\_FORCE\_SOFTWARE\_RENDERING in D2D1\_RENDER\_TARGET\_USAGE when creating a Direct2D render target.</span></span>

<span data-ttu-id="2dce6-168">Direct2D kann das WARP10 Software Raster verwenden, um das Gerät für Direct3D 10 oder Direct3D 11 freizugeben, aber die Leistung sinkt erheblich.</span><span class="sxs-lookup"><span data-stu-id="2dce6-168">Direct2D can use the WARP10 software rasterizer to share device with Direct3D 10 or Direct3D 11, but the performance declines significantly.</span></span>

### <a name="dxgi-11-synchronized-shared-surfaces"></a><span data-ttu-id="2dce6-169">DXGI 1,1 synchronisierte freigegebene Oberflächen</span><span class="sxs-lookup"><span data-stu-id="2dce6-169">DXGI 1.1 Synchronized Shared Surfaces</span></span>

<span data-ttu-id="2dce6-170">Direct3D 11, Direct3D 10,1-und Direct2D-APIs verwenden alle DXGI 1,1, das die Funktionalität zum Synchronisieren von Lese-und Schreib vorlese-und Schreib vorschreiben auf derselben Grafikspeicher Oberfläche (DXGISurface1) durch mindestens zwei Direct3D-Geräte bietet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-170">Direct3D 11, Direct3D 10.1 and Direct2D APIs all use DXGI 1.1, which provides the functionality to synchronize reading from and writing to the same video memory surface (DXGISurface1) by two or more Direct3D devices.</span></span> <span data-ttu-id="2dce6-171">Die renderinggeräte mit synchronisierten freigegebenen Oberflächen können Direct3D 10,1-oder Direct3D 11-Geräte sein, die jeweils in demselben Prozess oder prozessübergreifenden Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-171">The rendering devices using synchronized shared surfaces can be Direct3D 10.1 or Direct3D 11 devices, each running in the same process or cross-processes.</span></span>

<span data-ttu-id="2dce6-172">Anwendungen können synchronisierte freigegebene Oberflächen verwenden, um zwischen allen DXGI 1,1-basierten Geräten, z. b. Direct3D 11 und Direct3D 10,1, oder zwischen Direct3D 11 und Direct2D zu interagieren, indem das Direct3D 10,1-Gerät vom Direct2D-Renderziel Objekt erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-172">Applications can use synchronized shared surfaces to interoperate between any DXGI 1.1-based devices, such as Direct3D 11 and Direct3D 10.1, or between Direct3D 11 and Direct2D, by obtaining the Direct3D 10.1 device from Direct2D render target object.</span></span>

<span data-ttu-id="2dce6-173">Stellen Sie in den APIs Direct3D 10,1 und höher für die Verwendung von DXGI 1,1 sicher, dass das Direct3D-Gerät mithilfe eines DXGI 1,1-Adapter Objekts erstellt wird, das aus dem DXGI 1,1 Factory-Objekt aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-173">In Direct3D 10.1 and later APIs, to use DXGI 1.1, ensure that the Direct3D device is created using a DXGI 1.1 adapter object, which is enumerated from the DXGI 1.1 factory object.</span></span> <span data-ttu-id="2dce6-174">Rufen Sie CreateDXGIFactory1 auf, um das IDXGIFactory1-Objekt zu erstellen, und EnumAdapters1, um das IDXGIAdapter1-Objekt aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-174">Call CreateDXGIFactory1 to create the IDXGIFactory1 object, and EnumAdapters1 to enumerate the IDXGIAdapter1 object.</span></span> <span data-ttu-id="2dce6-175">Das IDXGIAdapter1-Objekt muss als Teil des D3D10CreateDevice-oder D3D10CreateDeviceAndSwapChain-Aufrufes aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-175">The IDXGIAdapter1 object needs to be passed in as part of D3D10CreateDevice or D3D10CreateDeviceAndSwapChain call.</span></span> <span data-ttu-id="2dce6-176">Weitere Informationen zu DXGI 1,1-APIs finden Sie im [Programmier Handbuch für DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="2dce6-176">For more information on DXGI 1.1 APIs, please refer to the [Programming Guide for DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).</span></span>

### <a name="apis"></a><span data-ttu-id="2dce6-177">APIs</span><span class="sxs-lookup"><span data-stu-id="2dce6-177">APIs</span></span>

<span data-ttu-id="2dce6-178">**D3d10 \_ \_ ressourcenmisc \_ Shared \_ keyedmutex**</span><span class="sxs-lookup"><span data-stu-id="2dce6-178">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="2dce6-179">Wenn Sie die synchronisierte freigegebene Ressource erstellen, legen Sie d3d10 \_ Resource \_ misc \_ Shared \_ keyedmutex in das \_ Flag d3d10 Resource \_ misc fest \_ .</span><span class="sxs-lookup"><span data-stu-id="2dce6-179">When creating the synchronized shared resource, set D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX in D3D10\_RESOURCE\_MISC\_FLAG.</span></span>  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



<span data-ttu-id="2dce6-180">**D3d10 \_ \_ ressourcenmisc \_ Shared \_ keyedmutex**</span><span class="sxs-lookup"><span data-stu-id="2dce6-180">**D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX**</span></span>  
<span data-ttu-id="2dce6-181">Ermöglicht die Synchronisierung der erstellten Ressource mithilfe der idxgikeyedmutex:: acquiresync-und releasesync-APIs.</span><span class="sxs-lookup"><span data-stu-id="2dce6-181">Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs.</span></span> <span data-ttu-id="2dce6-182">Die folgende Ressourcen Erstellung Direct3D 10,1-APIs, die alle einen d3d10- \_ ressourcenmisc-Flag-Parameter annehmen, wurden \_ \_ erweitert, um das neue Flag zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-182">The following resource creation Direct3D 10.1 APIs that all take a D3D10\_RESOURCE\_MISC\_FLAG parameter have been extended to support the new flag.</span></span>  

-   <span data-ttu-id="2dce6-183">ID3D10Device1::CreateTexture1D</span><span class="sxs-lookup"><span data-stu-id="2dce6-183">ID3D10Device1::CreateTexture1D</span></span>
-   <span data-ttu-id="2dce6-184">ID3D10Device1::CreateTexture2D</span><span class="sxs-lookup"><span data-stu-id="2dce6-184">ID3D10Device1::CreateTexture2D</span></span>
-   <span data-ttu-id="2dce6-185">ID3D10Device1::CreateTexture3D</span><span class="sxs-lookup"><span data-stu-id="2dce6-185">ID3D10Device1::CreateTexture3D</span></span>
-   <span data-ttu-id="2dce6-186">ID3D10Device1:: up Buffer</span><span class="sxs-lookup"><span data-stu-id="2dce6-186">ID3D10Device1::CreateBuffer</span></span>

  
<span data-ttu-id="2dce6-187">Wenn eine der aufgelisteten Funktionen mit dem "d3d10 \_ Resource \_ misc \_ Shared \_ keyedmutex"-Flag aufgerufen wird, kann die zurückgegebene Schnittstelle für eine idxgikeyedmutex-Schnittstelle abgefragt werden, die die acquiresync-und releasesync-APIs implementiert, um den Zugriff auf die-Oberfläche zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-187">If any of the listed functions are called with the D3D10\_RESOURCE\_MISC\_SHARED\_KEYEDMUTEX flag set, the interface returned can be queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface.</span></span> <span data-ttu-id="2dce6-188">Das Gerät, das die Oberfläche erstellt, und alle anderen Geräte, die die Oberfläche öffnen (mit opensharedresource), müssen idxgikeyedmutex:: acquiresync aufrufen, bevor alle renderingbefehle auf der Oberfläche ausgeführt werden, und idxgikeyedmutex:: releasesync beim Rendering.</span><span class="sxs-lookup"><span data-stu-id="2dce6-188">The device creating the surface and any other device opening the surface (using OpenSharedResource) is required to call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.</span></span>  
<span data-ttu-id="2dce6-189">Von Warp-und ref-Geräten werden keine freigegebenen Ressourcen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-189">WARP and REF devices do not support shared resources.</span></span> <span data-ttu-id="2dce6-190">Wenn Sie versuchen, eine Ressource mit diesem Flag entweder auf einem Warp-oder ref-Gerät zu erstellen, gibt die Create-Methode einen E \_ outo fmemory-Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-190">Attempting to create a resource with this flag on either a WARP or REF device will cause the create method to return an E\_OUTOFMEMORY error code.</span></span>  
<span data-ttu-id="2dce6-191">**idxgikeyedmutex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2dce6-191">**IDXGIKEYEDMUTEX INTERFACE**</span></span>  
<span data-ttu-id="2dce6-192">Eine neue Schnittstelle in DXGI 1,1, idxgikeyedmutex, stellt einen Schlüssel gebundenen Mutex dar, der exklusiven Zugriff auf eine freigegebene Ressource ermöglicht, die von mehreren Geräten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-192">A new interface in DXGI 1.1, IDXGIKeyedMutex, represents a keyed mutex, which allows exclusive access to a shared resource that is used by multiple devices.</span></span> <span data-ttu-id="2dce6-193">Eine Referenz Dokumentation zu dieser Schnittstelle und den beiden Methoden acquiresync und releasesync finden Sie unter [idxgikeyedmutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="2dce6-193">For reference documentation about this interface and its two methods, AcquireSync and ReleaseSync, see [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).</span></span>  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a><span data-ttu-id="2dce6-194">Beispiel: synchronisierte Oberflächen Freigabe zwischen zwei Direct3D 10,1-Geräten</span><span class="sxs-lookup"><span data-stu-id="2dce6-194">Sample: Synchronized Surface Sharing Between two Direct3D 10.1 Devices</span></span>

<span data-ttu-id="2dce6-195">Im folgenden Beispiel wird die gemeinsame Nutzung einer Oberfläche zwischen zwei Direct3D 10,1-Geräten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2dce6-195">The example below illustrates sharing a surface between two Direct3D 10.1 devices.</span></span> <span data-ttu-id="2dce6-196">Die synchronisierte freigegebene Oberfläche wird von einem Direct3D 10.1-Gerät erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-196">The synchronized shared surface is created by a Direct3D10.1 device.</span></span>


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



<span data-ttu-id="2dce6-197">Das gleiche Direct3D 10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem es acquiresync aufrufen und dann die Oberfläche für das Rendering des anderen Geräts durch Aufrufen von releasesync freigibt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-197">The same Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the other device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="2dce6-198">Wenn Sie die synchronisierte freigegebene Oberfläche nicht mit einem anderen Direct3D-Gerät freigeben, kann der Ersteller die synchronisierte freigegebene Oberfläche (zum Starten und Beenden des Renderings) abrufen und freigeben, indem er den gleichen Schlüsselwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-198">When not sharing the synchronized shared surface with any other Direct3D device, the creator can obtain and release the synchronized shared surface (to start and end rendering) by acquiring and release using the same key value.</span></span>


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



<span data-ttu-id="2dce6-199">Das zweite Direct3D 10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem es acquiresync aufrufen und dann die Oberfläche für das erste Rendern des Geräts durch Aufrufen von releasesync freigibt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-199">The second Direct3D10.1 device can obtain the synchronized shared surface for rendering by calling AcquireSync, then releasing the surface for the first device's rendering by calling ReleaseSync.</span></span> <span data-ttu-id="2dce6-200">Beachten Sie, dass Gerät 2 die synchronisierte freigegebene Oberfläche mithilfe desselben Schlüssel Werts abrufen kann, der im releasesync-Aufruf von Gerät 1 angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2dce6-200">Note that device 2 is able to acquire the synchronized shared surface using the same key value as the one specified in the ReleaseSync call by device 1.</span></span>


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



<span data-ttu-id="2dce6-201">Weitere Geräte, die dieselbe Oberfläche gemeinsam nutzen, können die Oberfläche mithilfe zusätzlicher Schlüssel abrufen und freigeben, wie in den folgenden Aufrufen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-201">Additional devices sharing the same surface can take turns acquiring and releasing the surface by using additional keys, as shown in the following calls.</span></span>


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



<span data-ttu-id="2dce6-202">Beachten Sie, dass eine reale Anwendung immer auf eine zwischen Oberfläche renderierender ist, die dann auf die freigegebene Oberfläche kopiert wird, um zu verhindern, dass ein Gerät auf ein anderes Gerät wartet, das die Oberfläche nutzt</span><span class="sxs-lookup"><span data-stu-id="2dce6-202">Note that a real-world application might always render to an intermediate surface that is then copied into the shared surface to prevent any one device waiting on another device that shares the surface.</span></span>

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a><span data-ttu-id="2dce6-203">Verwenden von synchronisierten freigegebenen Oberflächen mit Direct2D und Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2dce6-203">Using Synchronized Shared Surfaces with Direct2D and Direct3D 11</span></span>

<span data-ttu-id="2dce6-204">Ebenso kann für die gemeinsame Nutzung zwischen Direct3D 11-und Direct3D 10,1-APIs eine synchronisierte freigegebene Oberfläche entweder von API-Geräten aus erstellt und für die anderen API-Geräte, in oder außerhalb des Prozesses, freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-204">Similarly, for sharing between Direct3D 11 and Direct3D 10.1 APIs, a synchronized shared surface can be created from either API device and shared with the other API device(s), in or out of process.</span></span>

<span data-ttu-id="2dce6-205">Anwendungen, die Direct2D verwenden, können ein Direct3D 10,1-Gerät freigeben und eine synchronisierte freigegebene Oberfläche verwenden, um mit Direct3D 11 oder anderen Direct3D 10,1-Geräten zusammenzuarbeiten, unabhängig davon, ob Sie zum gleichen Prozess oder zu unterschiedlichen Prozessen gehören.</span><span class="sxs-lookup"><span data-stu-id="2dce6-205">Applications that use Direct2D can share a Direct3D 10.1 device and use a synchronized shared surface to interoperate with Direct3D 11 or other Direct3D 10.1 devices, whether they belong to the same process or different processes.</span></span> <span data-ttu-id="2dce6-206">Für Single-Process-Anwendungen mit nur einem Thread ist die Geräte Freigabe jedoch die leistungsfähigsten und effizientesten Interoperabilitäts Methode zwischen Direct2D und Direct3D 10 oder Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2dce6-206">However, for single-process, single-thread applications, device sharing is the most high-performance and efficient method of interoperability between Direct2D and either Direct3D 10 or Direct3D 11.</span></span>

### <a name="software-rasterizer"></a><span data-ttu-id="2dce6-207">Software-Rasterizer</span><span class="sxs-lookup"><span data-stu-id="2dce6-207">Software Rasterizer</span></span>

<span data-ttu-id="2dce6-208">Synchronisierte freigegebene Oberflächen werden nicht unterstützt, wenn Anwendungen die Direct3D-oder Direct2D-Software-Raster verwenden, einschließlich des verweisrasterizers und des Warp, anstelle der Hardwarebeschleunigung.</span><span class="sxs-lookup"><span data-stu-id="2dce6-208">Synchronized shared surfaces are not supported when applications use the Direct3D or Direct2D software rasterizers, including the reference rasterizer and WARP, instead of using graphics hardware acceleration.</span></span>

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a><span data-ttu-id="2dce6-209">Interoperabilität zwischen Direct3D 9Ex und DXGI-basierten APIs</span><span class="sxs-lookup"><span data-stu-id="2dce6-209">Interoperability between Direct3D 9Ex and DXGI based APIs</span></span>

<span data-ttu-id="2dce6-210">Die Direct3D 9Ex-APIs enthielten das Konzept der Oberflächen Freigabe, damit andere APIs von der freigegebenen Oberfläche lesen können.</span><span class="sxs-lookup"><span data-stu-id="2dce6-210">Direct3D 9Ex APIs included the notion of surface sharing to allow other APIs to read from the shared surface.</span></span> <span data-ttu-id="2dce6-211">Um Lese-und Schreibvorgänge für eine freigegebene Direct3D 9Ex-Oberfläche zu verwenden, müssen Sie der Anwendung selbst eine manuelle Synchronisierung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-211">In order to share reading and writing to a Direct3D 9Ex shared surface, you must add manual synchronization to the application itself.</span></span>

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a><span data-ttu-id="2dce6-212">Direct3D 9Ex Shared-Oberflächen Plus Manuelles Synchronisieren-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="2dce6-212">Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper</span></span>

<span data-ttu-id="2dce6-213">Die grundlegendste Aufgabe bei der Interoperabilität von Direct3D 9Ex und Direct3D 10 oder 11 besteht darin, eine einzige Oberfläche vom ersten Gerät (Gerät a) an das zweite Gerät (Gerät b) zu übergeben, sodass das Rendering von Gerät a vollständig abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-213">The most fundamental task in Direct3D 9Ex and Direct3D 10 or 11 interoperability is passing a single surface from the first device (device A) to the second (device B) such that when device B acquires a handle on the surface, device A's rendering is guaranteed to have completed.</span></span> <span data-ttu-id="2dce6-214">Daher kann Gerät B diese Oberfläche ohne Sorgen nutzen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-214">Therefore, device B can use this surface without worry.</span></span> <span data-ttu-id="2dce6-215">Diese Vorgehensweise ähnelt dem klassischen Producer-Consumer-Problem, und dieses Problem wird auf diese Weise modelliert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-215">This is very similar to the classic producer-consumer problem and this discussion models the problem that way.</span></span> <span data-ttu-id="2dce6-216">Das erste Gerät, das die-Oberfläche verwendet und dann aufgibt, ist der Producer (Gerät A), und das Gerät, das anfänglich wartet, ist der Consumer (Gerät B).</span><span class="sxs-lookup"><span data-stu-id="2dce6-216">The first device that uses the surface and then relinquishes it is the producer (Device A), and the device that is initially waiting is the consumer (Device B).</span></span> <span data-ttu-id="2dce6-217">Alle realen Anwendungen sind komplexer als dies, und Sie verketten mehrere Producer-Consumer-Bausteine, um die gewünschte Funktionalität zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-217">Any real-world application is more sophisticated than this, and will chain together multiple producer-consumer building blocks to create the desired functionality.</span></span>

<span data-ttu-id="2dce6-218">Die Producer-Consumer-Bausteine werden mithilfe einer Warteschlange von Oberflächen in das Hilfsprogramm implementiert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-218">The producer-consumer building blocks are implemented in the helper by using a queue of surfaces.</span></span> <span data-ttu-id="2dce6-219">Oberflächen werden vom Producer in die Warteschlange eingereiht und vom Consumer aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-219">Surfaces are enqueued by the producer and dequeued by the consumer.</span></span> <span data-ttu-id="2dce6-220">Das Hilfsprogramm führt drei COM-Schnittstellen ein: isurfacequeue, isurfaceproducer und isurfaceconsumer.</span><span class="sxs-lookup"><span data-stu-id="2dce6-220">The helper introduces three COM interfaces: ISurfaceQueue, ISurfaceProducer, and ISurfaceConsumer.</span></span>

### <a name="high-level-overview-of-helper"></a><span data-ttu-id="2dce6-221">High-Level Übersicht über das Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="2dce6-221">High-Level Overview of Helper</span></span>

<span data-ttu-id="2dce6-222">Das isurfakequeue-Objekt ist der Baustein für die Verwendung der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-222">The ISurfaceQueue object is the building block for using the shared surfaces.</span></span> <span data-ttu-id="2dce6-223">Es wird mit einem initialisierten Direct3D-Gerät und einer Beschreibung erstellt, um eine Fixed-Anzahl von freigegebenen Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-223">It is created with an initialized Direct3D device and a description to create a fixed number of shared surfaces.</span></span> <span data-ttu-id="2dce6-224">Das Queue-Objekt verwaltet die Erstellung von Ressourcen und das Öffnen von Code.</span><span class="sxs-lookup"><span data-stu-id="2dce6-224">The queue object manages creation of resources and opening of code.</span></span> <span data-ttu-id="2dce6-225">Anzahl und Typ der Oberflächen werden korrigiert. Nachdem die Oberflächen erstellt wurden, kann Sie von der Anwendung nicht mehr hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-225">The number and type of surfaces are fixed; once the surfaces are created, the application cannot add or remove them.</span></span>

<span data-ttu-id="2dce6-226">Jede Instanz des isurfakequeue-Objekts stellt eine unidirektionale Straße dar, die zum Senden von Oberflächen vom produzierenden Gerät an das verarbeitende Gerät verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2dce6-226">Each instance of the ISurfaceQueue object provides a sort of one-way street that can be used to send surfaces from the producing device to the consuming device.</span></span> <span data-ttu-id="2dce6-227">Mehrere unidirektionale Straßen können verwendet werden, um Oberflächen Freigabe Szenarien zwischen Geräten spezifischer Anwendungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-227">Multiple such one-way streets can be used to enable surface sharing scenarios between devices of specific applications.</span></span>

<span data-ttu-id="2dce6-228">**Erstellung/Objekt Lebensdauer**</span><span class="sxs-lookup"><span data-stu-id="2dce6-228">**Creation/Object Lifetime**</span></span>  
<span data-ttu-id="2dce6-229">Es gibt zwei Möglichkeiten, das Warteschlangen Objekt zu erstellen: über "kreatesurfacequeue" oder über die Klon Methode von isurfacequeue.</span><span class="sxs-lookup"><span data-stu-id="2dce6-229">There are two ways to create the queue object: through CreateSurfaceQueue, or through the Clone method of ISurfaceQueue.</span></span> <span data-ttu-id="2dce6-230">Da es sich bei den Schnittstellen um COM-Objekte handelt, gilt die Standard Verwaltung von com</span><span class="sxs-lookup"><span data-stu-id="2dce6-230">Because the interfaces are COM objects, standard COM lifetime management applies.</span></span>  
<span data-ttu-id="2dce6-231">**Producer/Consumer-Modell**</span><span class="sxs-lookup"><span data-stu-id="2dce6-231">**Producer/Consumer Model**</span></span>  
<span data-ttu-id="2dce6-232">Enqueue (): der Producer ruft diese Funktion auf, um anzugeben, dass Sie mit der-Oberfläche abgeschlossen ist, die jetzt für ein anderes Gerät verfügbar sein kann.</span><span class="sxs-lookup"><span data-stu-id="2dce6-232">Enqueue (): The producer calls this function to indicate it is done with the surface, which can now become available to another device.</span></span> <span data-ttu-id="2dce6-233">Nach dem Zurückgeben dieser Funktion hat das Producer-Gerät keine Rechte mehr auf die Oberfläche, und es ist unsicher, Sie weiterhin zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-233">Upon returning from this function, the producer device no longer has rights to the surface and it is unsafe to continue using it.</span></span>  
<span data-ttu-id="2dce6-234">Dequeue (): das verarbeitende Gerät ruft diese Funktion auf, um eine freigegebene Oberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-234">Dequeue (): The consuming device calls this function to get a shared surface.</span></span> <span data-ttu-id="2dce6-235">Die API stellt sicher, dass alle aus der Warteschlange eingereihten Oberflächen zur Verwendung bereit sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-235">The API guarantees that any dequeued surfaces are ready to be used.</span></span>  
<span data-ttu-id="2dce6-236">**Metadaten**</span><span class="sxs-lookup"><span data-stu-id="2dce6-236">**Metadata**</span></span>  
<span data-ttu-id="2dce6-237">Die API unterstützt das Zuordnen von Metadaten zu den freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-237">The API supports associating metadata with the shared surfaces.</span></span>  
<span data-ttu-id="2dce6-238">In der Warteschlange () haben Sie die Möglichkeit, zusätzliche Metadaten anzugeben, die an das verarbeitende Gerät weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-238">Enqueue() has the option of specifying additional metadata that will be passed to the consuming device.</span></span> <span data-ttu-id="2dce6-239">Die Metadaten müssen kleiner als der zum Erstellungs Zeitpunkt bekannte Höchstwert sein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-239">The metadata must be less than a maximum known at creation time.</span></span>  
<span data-ttu-id="2dce6-240">Aus Queue () kann optional ein Puffer und ein Zeiger auf die Größe des Puffers übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-240">Dequeue() can optionally pass a buffer and a pointer to the size of the buffer.</span></span> <span data-ttu-id="2dce6-241">Die Warteschlange füllt den Puffer mit den Metadaten aus dem entsprechenden aufrufeschlangenbefehl.</span><span class="sxs-lookup"><span data-stu-id="2dce6-241">The queue fills in the buffer with the metadata from the corresponding Enqueue call.</span></span>  
<span data-ttu-id="2dce6-242">**Klonen?**</span><span class="sxs-lookup"><span data-stu-id="2dce6-242">**Cloning**</span></span>  
<span data-ttu-id="2dce6-243">Jedes isurfakequeue-Objekt löst eine unidirektionale Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="2dce6-243">Each ISurfaceQueue object solves a one-way synchronization.</span></span> <span data-ttu-id="2dce6-244">Wir gehen davon aus, dass die große Mehrheit der Anwendungen, die diese API verwenden, ein geschlossenes System verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-244">We assume that the vast majority of applications using this API will use a closed system.</span></span> <span data-ttu-id="2dce6-245">Das einfachste geschlossene System mit zwei Geräten, die die Oberflächen hin-und Hersenden, erfordert zwei Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-245">The simplest closed system with two devices sending surfaces back and forth requires two queues.</span></span> <span data-ttu-id="2dce6-246">Das isurfacequeue-Objekt verfügt über eine Clone ()-Methode, um das Erstellen mehrerer Warteschlangen zu ermöglichen, die alle Teil derselben größeren Pipeline sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-246">The ISurfaceQueue object has a Clone() method to make it possible to create multiple queues that are all part of the same larger pipeline.</span></span>  
<span data-ttu-id="2dce6-247">Klon erstellt ein neues isurfakequeue-Objekt aus einem vorhandenen Objekt und teilt alle geöffneten Ressourcen auf.</span><span class="sxs-lookup"><span data-stu-id="2dce6-247">Clone creates a new ISurfaceQueue object from an existing one, and shares all the opened resources between them.</span></span> <span data-ttu-id="2dce6-248">Das resultierende-Objekt verfügt über genau die gleichen Oberflächen wie die Quell Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-248">The resulting object has exactly the same surfaces as the source queue.</span></span> <span data-ttu-id="2dce6-249">Geklonte Warteschlangen können über unterschiedliche metadatengrößen verfügen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-249">Cloned queues can have different metadata sizes from each other.</span></span>  
<span data-ttu-id="2dce6-250">**Surface**</span><span class="sxs-lookup"><span data-stu-id="2dce6-250">**Surfaces**</span></span>  
<span data-ttu-id="2dce6-251">Isurfakequeue übernimmt die Verantwortung für das Erstellen und Verwalten seiner Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-251">The ISurfaceQueue takes responsibility for creating and managing its surfaces.</span></span> <span data-ttu-id="2dce6-252">Es ist nicht zulässig, beliebige Oberflächen in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-252">It is not valid to enqueue arbitrary surfaces.</span></span> <span data-ttu-id="2dce6-253">Außerdem sollte eine Oberfläche nur über einen aktiven "Besitzer" verfügen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-253">Furthermore, a surface should only have one active "owner."</span></span> <span data-ttu-id="2dce6-254">Er sollte sich entweder in einer bestimmten Warteschlange befinden oder von einem bestimmten Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-254">It should either be on a specific queue or being used by a specific device.</span></span> <span data-ttu-id="2dce6-255">Es ist nicht zulässig, es in mehreren Warteschlangen zu verwenden, oder die Oberfläche kann von Geräten weiterhin verwendet werden, nachdem Sie in die Warteschlange eingereiht wurde.</span><span class="sxs-lookup"><span data-stu-id="2dce6-255">It is not valid to have it on multiple queues or for devices to continue using the surface after it is enqueued.</span></span>  
</dl>

### <a name="api-details"></a><span data-ttu-id="2dce6-256">API-Details</span><span class="sxs-lookup"><span data-stu-id="2dce6-256">API Details</span></span>

### <a name="isurfacequeue"></a><span data-ttu-id="2dce6-257">Isurfakequeue</span><span class="sxs-lookup"><span data-stu-id="2dce6-257">IsurfaceQueue</span></span>

<span data-ttu-id="2dce6-258">Die Warteschlange ist für das Erstellen und Verwalten der freigegebenen Ressourcen zuständig.</span><span class="sxs-lookup"><span data-stu-id="2dce6-258">The queue is responsible for creating and maintaining the shared resources.</span></span> <span data-ttu-id="2dce6-259">Außerdem bietet es die Funktionalität zum Verketten mehrerer Warteschlangen mithilfe von Klonen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-259">It also provides the functionality to chain multiple queues using Clone.</span></span> <span data-ttu-id="2dce6-260">Die Warteschlange verfügt über Methoden, die das erbende Gerät und ein consumergerät öffnen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-260">The queue has methods that open the producing device and a consuming device.</span></span> <span data-ttu-id="2dce6-261">Es kann immer nur jeweils einer der beiden geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-261">Only one of each can be opened at any time.</span></span>

<span data-ttu-id="2dce6-262">Die Warteschlange stellt die folgenden APIs bereit:</span><span class="sxs-lookup"><span data-stu-id="2dce6-262">The queue exposes the following APIs:</span></span>



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2dce6-263">"Kreatesurfakequeue"</span><span class="sxs-lookup"><span data-stu-id="2dce6-263">CreateSurfaceQueue</span></span>          | <span data-ttu-id="2dce6-264">Erstellt ein isurfakequeue-Objekt (die Stamm Warteschlange).</span><span class="sxs-lookup"><span data-stu-id="2dce6-264">Creates an ISurfaceQueue object (the "root" queue).</span></span>                              |
| <span data-ttu-id="2dce6-265">Isurfakequeue:: openconsumer</span><span class="sxs-lookup"><span data-stu-id="2dce6-265">ISurfaceQueue::OpenConsumer</span></span> | <span data-ttu-id="2dce6-266">Gibt eine Schnittstelle für das zu entmittelende Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-266">Returns an interface for the consuming device to dequeue.</span></span>                        |
| <span data-ttu-id="2dce6-267">Isurfakequeue:: openproducer</span><span class="sxs-lookup"><span data-stu-id="2dce6-267">ISurfaceQueue::OpenProducer</span></span> | <span data-ttu-id="2dce6-268">Gibt eine Schnittstelle für das herzustellende Gerät in die Warteschlange zurück</span><span class="sxs-lookup"><span data-stu-id="2dce6-268">Returns an interface for the producing device to enqueue.</span></span>                        |
| <span data-ttu-id="2dce6-269">Isurfakequeue:: Clone</span><span class="sxs-lookup"><span data-stu-id="2dce6-269">ISurfaceQueue::Clone</span></span>        | <span data-ttu-id="2dce6-270">Erstellt ein isurfakequeue-Objekt, das Oberflächen mit dem Stamm Warteschlangen Objekt freigibt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-270">Creates an ISurfaceQueue object that shares surfaces with the root queue object.</span></span> |



 

<span data-ttu-id="2dce6-271">**"Kreatesurfakequeue"**</span><span class="sxs-lookup"><span data-stu-id="2dce6-271">**CreateSurfaceQueue**</span></span>  


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



<span data-ttu-id="2dce6-272">**Mitglieder**</span><span class="sxs-lookup"><span data-stu-id="2dce6-272">**Members**</span></span>  

<span data-ttu-id="2dce6-273">**Breite**, **Höhe**  der Dimensionen der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-273">**Width**, **Height**  The dimensions of the shared surfaces.</span></span> <span data-ttu-id="2dce6-274">Alle freigegebenen Oberflächen müssen die gleichen Dimensionen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-274">All shared surfaces must have the same dimensions.</span></span>  
<span data-ttu-id="2dce6-275">**Format** Das Format der freigegebenen Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-275">**Format** The format of the shared surfaces.</span></span> <span data-ttu-id="2dce6-276">Alle freigegebenen Oberflächen müssen das gleiche Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-276">All shared surfaces must have the same format.</span></span> <span data-ttu-id="2dce6-277">Die gültigen Formate sind abhängig von den Geräten, die verwendet werden, da verschiedene Geräte Paare verschiedene Format Typen gemeinsam nutzen können.</span><span class="sxs-lookup"><span data-stu-id="2dce6-277">The valid formats depend on the devices that will be used, because different pairs of devices can share different format types.</span></span>  
<span data-ttu-id="2dce6-278">**Numoberflächen**  Die Anzahl der Oberflächen, die Teil der Warteschlange sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-278">**NumSurfaces**  The number of surfaces that are part of the queue.</span></span> <span data-ttu-id="2dce6-279">Dies ist eine Fixed-Nummer.</span><span class="sxs-lookup"><span data-stu-id="2dce6-279">This is a fixed number.</span></span>  
 <span data-ttu-id="2dce6-280">**MetaDataSize**  Die maximale Größe des metadatenpuffers.</span><span class="sxs-lookup"><span data-stu-id="2dce6-280">**MetaDataSize**  The maximum size of the metadata buffer.</span></span>  
<span data-ttu-id="2dce6-281">**Flags**  Flags zum Steuern des Verhaltens der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-281">**Flags**  Flags to control the behavior of the queue.</span></span> <span data-ttu-id="2dce6-282">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2dce6-282">See Remarks.</span></span>  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="2dce6-283">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-283">**Parameters**</span></span>

 <span data-ttu-id="2dce6-284">*PDE SC* \[ in \]  der Beschreibung der zu erstellenden freigegebenen Oberflächen Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-284">*pDesc* \[in\]  The description of the shared surface queue to be created.</span></span>  

 <span data-ttu-id="2dce6-285">*pdevice* \[ auf \]  dem Gerät, das zum Erstellen der freigegebenen Oberflächen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dce6-285">*pDevice* \[in\]  The device that should be used to create the shared surfaces.</span></span> <span data-ttu-id="2dce6-286">Dies ist ein expliziter Parameter aufgrund eines Features in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2dce6-286">This is an explicit parameter because of a feature in Windows Vista.</span></span> <span data-ttu-id="2dce6-287">Für Oberflächen, die von Direct3D 9 und Direct3D 10 gemeinsam genutzt werden, müssen die Oberflächen mit Direct3D 9 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-287">For surfaces shared between Direct3D 9 and Direct3D 10, the surfaces must be created with Direct3D 9.</span></span>  

 <span data-ttu-id="2dce6-288">*ppqueue* \[ Out \]  bei der Rückgabe enthält einen Zeiger auf das isurfakequeue-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-288">*ppQueue* \[out\]  On return, contains a pointer to the ISurfaceQueue object.</span></span>  


<span data-ttu-id="2dce6-289">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-289">**Return Values**</span></span>

<span data-ttu-id="2dce6-290">Wenn *pdevice* Ressourcen nicht freigeben kann, gibt diese Funktion einen ungültigen DXGI- \_ Fehler zurück \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2dce6-290">If *pDevice* is not capable of sharing resources, this function returns DXGI\_ERROR\_INVALID\_CALL.</span></span> <span data-ttu-id="2dce6-291">Diese Funktion erstellt die Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-291">This function creates the resources.</span></span> <span data-ttu-id="2dce6-292">Wenn ein Fehler auftritt, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-292">If it fails, it returns an error.</span></span> <span data-ttu-id="2dce6-293">Wenn der Vorgang erfolgreich ist, wird S OK zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="2dce6-293">If it succeeds, it returns S\_OK.</span></span>

<span data-ttu-id="2dce6-294">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-294">**Remarks**</span></span>

<span data-ttu-id="2dce6-295">Beim Erstellen des Warteschlangen Objekts werden auch alle-Oberflächen erstellt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-295">Creating the queue object also creates all of the surfaces.</span></span> <span data-ttu-id="2dce6-296">Bei allen Oberflächen handelt es sich um 2D-Renderziele. Sie werden mit den \_ \_ \_ Ressourcenflags d3d10 BIND-Renderziel und d3d10 \_ Bind- \_ Shader erstellt \_ (oder die entsprechenden Flags für die unterschiedlichen Laufzeiten).</span><span class="sxs-lookup"><span data-stu-id="2dce6-296">All surfaces are assumed to be 2D render targets and will be created with the D3D10\_BIND\_RENDER\_TARGET and D3D10\_BIND\_SHADER\_RESOURCE flags set (or the equivalent flags for the different runtimes).</span></span>

<span data-ttu-id="2dce6-297">Der Entwickler kann ein Flag angeben, das angibt, ob mehrere Threads auf die Warteschlange zugreifen werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-297">The developer can specify a flag that indicates whether the queue will be accessed by multiple threads.</span></span> <span data-ttu-id="2dce6-298">Wenn keine Flags festgelegt sind (**Flags** = = 0), wird die Warteschlange von mehreren Threads verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-298">If no flags are set (**Flags** == 0), the queue will be used by multiple threads.</span></span> <span data-ttu-id="2dce6-299">Der Entwickler kann einen Single Thread-Zugriff angeben, der den Synchronisierungs Code deaktiviert und eine Leistungsverbesserung für diese Fälle bietet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-299">The developer can specify single threaded access, which turns off the synchronization code and provides a performance improvement for those cases.</span></span> <span data-ttu-id="2dce6-300">Jede geklonte Warteschlange verfügt über ein eigenes Flag, daher ist es möglich, dass für unterschiedliche Warteschlangen im System verschiedene Synchronisierungs Steuerungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-300">Each cloned queue has its own flag, so it is possible for different queues in the system to have different synchronization controls.</span></span>

 <span data-ttu-id="2dce6-301">**Einen Producer öffnen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-301">**Open a Producer**</span></span>  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



<span data-ttu-id="2dce6-302">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-302">**Parameters**</span></span>  

<span data-ttu-id="2dce6-303">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dce6-303">*pDevice* \[in\]</span></span>  

<span data-ttu-id="2dce6-304">Das Producer-Gerät, das in die Warteschlange für die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-304">The producer device that enqueues surfaces onto the surface queue.</span></span> 

<span data-ttu-id="2dce6-305">*ppproducer* \[ Out \] gibt ein Objekt an die Producer-Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-305">*ppProducer* \[out\] Returns an object to the producer interface.</span></span>  


<span data-ttu-id="2dce6-306">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-306">**Return Values**</span></span>

<span data-ttu-id="2dce6-307">Wenn das Gerät keine Oberflächen freigeben kann, wird der ungültige DXGI-Fehler zurückgegeben \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2dce6-307">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="2dce6-308">**Einen Consumer öffnen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-308">**Open a Consumer**</span></span>  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



<span data-ttu-id="2dce6-309">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-309">**Parameters**</span></span>  
 <span data-ttu-id="2dce6-310">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dce6-310">*pDevice* \[in\]</span></span>  
 <span data-ttu-id="2dce6-311">Das consumergerät, das die Oberfläche aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-311">The consumer device that dequeues surfaces from the surface queue.</span></span> 
 <span data-ttu-id="2dce6-312">*ppconsumer* \[ Out \]  gibt ein Objekt an die consumerschnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-312">*ppConsumer* \[out\]  Returns an object to the consumer interface.</span></span>  


<span data-ttu-id="2dce6-313">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-313">**Return Values**</span></span>

<span data-ttu-id="2dce6-314">Wenn das Gerät keine Oberflächen freigeben kann, wird der ungültige DXGI-Fehler zurückgegeben \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2dce6-314">If the device is not capable of sharing surfaces, returns DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="2dce6-315">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-315">**Remarks**</span></span>

<span data-ttu-id="2dce6-316">Diese Funktion öffnet alle Oberflächen in der Warteschlange für das Eingabegerät und speichert Sie zwischen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-316">This function opens all of the surfaces in the queue for the input device and caches them.</span></span> <span data-ttu-id="2dce6-317">Nachfolgende Aufrufe von Dequeue werden einfach in den Cache übergegangen und müssen die Oberflächen nicht jedes Mal erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-317">Subsequent calls to Dequeue will simply go to the cache and not have to reopen the surfaces each time.</span></span>



### <a name="cloning-an-idxgixsurfacequeue"></a><span data-ttu-id="2dce6-318">Klonen eines idxgixsurfakequeue</span><span class="sxs-lookup"><span data-stu-id="2dce6-318">Cloning an IDXGIXSurfaceQueue</span></span>




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



<span data-ttu-id="2dce6-319"> Member **MetaDataSize** und **Flags** haben das gleiche Verhalten wie bei "kreatesurfagequeue".</span><span class="sxs-lookup"><span data-stu-id="2dce6-319">**Members** **MetaDataSize** and **Flags** have the same behavior as they do for CreateSurfaceQueue.</span></span>  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



<span data-ttu-id="2dce6-320">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-320">**Parameters**</span></span>

<span data-ttu-id="2dce6-321">*PDE SC* \[ in \] einer Struktur, die eine Beschreibung des zu erstellenden Klon Objekts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-321">*pDesc* \[in\] A struct that provides a description of the Clone object to be created.</span></span> <span data-ttu-id="2dce6-322">Dieser Parameter muss initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-322">This parameter should be initialized.</span></span>  
<span data-ttu-id="2dce6-323">*ppqueue* \[ Out \] gibt das initialisierte Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-323">*ppQueue* \[out\] Returns the initialized object.</span></span>  
</dl>

<span data-ttu-id="2dce6-324">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-324">**Remarks**</span></span>

<span data-ttu-id="2dce6-325">Sie können aus jedem vorhandenen Warteschlangen Objekt klonen, auch wenn es nicht der Stamm ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-325">You can clone from any existing queue object, even if it is not the root.</span></span>  
</dl>

### <a name="idxgixsurfaceconsumer"></a><span data-ttu-id="2dce6-326">Idxgixsurfakeconsumer</span><span class="sxs-lookup"><span data-stu-id="2dce6-326">IDXGIXSurfaceConsumer</span></span>

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



<span data-ttu-id="2dce6-327">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-327">**Parameters**</span></span>  
<span data-ttu-id="2dce6-328">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dce6-328">*id* \[in\]</span></span>  
<span data-ttu-id="2dce6-329">Die refi-ID einer 2D-Oberfläche des nutzenden Geräts.</span><span class="sxs-lookup"><span data-stu-id="2dce6-329">The REFIID of a 2D surface of the consuming device.</span></span>  

-   <span data-ttu-id="2dce6-330">Bei einem IDirect3DDevice9 muss die refi-ID \_ \_ uuidof (IDirect3DTexture9) sein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-330">For a IDirect3DDevice9, the REFIID should be \_\_uuidof(IDirect3DTexture9).</span></span>
-   <span data-ttu-id="2dce6-331">Bei einem ID3D10Device muss die refi-ID \_ \_ uuidof (ID3D10Texture2D) sein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-331">For a ID3D10Device, the REFIID should be \_\_uuidof(ID3D10Texture2D).</span></span>
-   <span data-ttu-id="2dce6-332">Bei einem ID3D11Device muss die refi-ID \_ \_ uuidof (ID3D11Texture2D) sein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-332">For a ID3D11Device, the REFIID should be \_\_uuidof(ID3D11Texture2D).</span></span>

<span data-ttu-id="2dce6-333">*ppsurface* \[ Out \] gibt einen Zeiger auf die-Oberfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="2dce6-333">*ppSurface* \[out\] Returns a pointer to the surface.</span></span>  
<span data-ttu-id="2dce6-334">*pbuffer* \[ in, out \] ein optionaler Parameter, und wenn not **null** ist, enthält bei der Rückgabe die Metadaten, die an den entsprechenden aufruteschlangen-Befehl übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-334">*pBuffer* \[in, out\] An optional parameter and if not **NULL**, on return, contains the metadata that was passed in on the corresponding enqueue call.</span></span>  
<span data-ttu-id="2dce6-335">*pbuffersize* \[ in \] die Größe von *pbuffer* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2dce6-335">*pBufferSize* \[in, out\] The size of *pBuffer*, in bytes.</span></span> <span data-ttu-id="2dce6-336">Gibt die Anzahl von Bytes zurück, die in *pbuffer* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-336">Returns the number of bytes returned in *pBuffer*.</span></span> <span data-ttu-id="2dce6-337">Wenn der einreihen-Rückruf keine Metadaten bereitstellt, wird *pbuffer* auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-337">If the enqueue call did not provide metadata, *pBuffer* is set to 0.</span></span>  
<span data-ttu-id="2dce6-338">*dwtimeout* \[ in \] gibt einen Timeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="2dce6-338">*dwTimeout* \[in\] Specifies a timeout value.</span></span> <span data-ttu-id="2dce6-339">Weitere Details finden Sie in den hinweisen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-339">See the Remarks for more detail.</span></span>  
</dl>

<span data-ttu-id="2dce6-340">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-340">**Return Values**</span></span>

<span data-ttu-id="2dce6-341">Diese Funktion kann das Timeout Timeout zurückgeben, \_ Wenn ein Timeout Wert angegeben wird und die Funktion nicht vor dem Timeout Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-341">This function can return WAIT\_TIMEOUT if a timeout value is specified and the function does not return before the time out value.</span></span> <span data-ttu-id="2dce6-342">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2dce6-342">See Remarks.</span></span> <span data-ttu-id="2dce6-343">Wenn keine Oberflächen verfügbar sind, gibt die Funktion zurück, wobei *ppsurface* auf **null**, *pbuffersize* auf 0 und der Rückgabewert 0x80070120 (Win32 \_ zu \_ HRESULT (Wartezeit \_ Timeout)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-343">If no surfaces are available, the function returns with *ppSurface* set to **NULL**, *pBufferSize* set to 0 and the return value is 0x80070120 (WIN32\_TO\_HRESULT(WAIT\_TIMEOUT)).</span></span>  
</dl>

<span data-ttu-id="2dce6-344">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-344">**Remarks**</span></span>

<span data-ttu-id="2dce6-345">Diese API kann blockieren, wenn die Warteschlange leer ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-345">This API can block if the queue is empty.</span></span> <span data-ttu-id="2dce6-346">Der Parameter " *dwtimeout* " funktioniert identisch mit den Windows-Synchronisierungs-APIs, z. b. "WaitForSingleObject".</span><span class="sxs-lookup"><span data-stu-id="2dce6-346">The *dwTimeout* parameter works identically to the Windows synchronization APIs, such as WaitForSingleObject.</span></span> <span data-ttu-id="2dce6-347">Verwenden Sie für ein nicht blockierendes Verhalten einen Timeout Wert von 0.</span><span class="sxs-lookup"><span data-stu-id="2dce6-347">For non-blocking behavior, use a timeout of 0.</span></span>  
</dl>

### <a name="isurfaceproducer"></a><span data-ttu-id="2dce6-348">Isurfaceproducer</span><span class="sxs-lookup"><span data-stu-id="2dce6-348">ISurfaceProducer</span></span>

<span data-ttu-id="2dce6-349">Diese Schnittstelle bietet zwei Methoden, mit denen die APP Oberflächen in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="2dce6-349">This interface provides two methods that allow the app to enqueue surfaces.</span></span> <span data-ttu-id="2dce6-350">Nachdem eine Oberfläche in die Warteschlange eingereiht wurde, ist der Surface-Zeiger nicht mehr gültig und kann nicht sicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-350">After a surface is enqueued, the surface pointer is no longer valid and is not safe to use.</span></span> <span data-ttu-id="2dce6-351">Die einzige Aktion, die die Anwendung mit dem Zeiger ausführen sollte, besteht darin, Sie freizugeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-351">The only action that the application should perform with the pointer is to release it.</span></span>



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dce6-352">Isurfaceproducer:: Einreihen in Warteschlange</span><span class="sxs-lookup"><span data-stu-id="2dce6-352">ISurfaceProducer::Enqueue</span></span> | <span data-ttu-id="2dce6-353">Fügt eine Oberfläche in die Warteschlange des Warteschlangen Objekts ein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-353">Enqueues a surface to the queue object.</span></span> <span data-ttu-id="2dce6-354">Nachdem dieser Vorgang abgeschlossen wurde, erfolgt der Producer mit der Oberfläche, und die Oberfläche ist für ein anderes Gerät bereit.</span><span class="sxs-lookup"><span data-stu-id="2dce6-354">After this call completes, the producer is done with the surface and the surface is ready for another device.</span></span> |
| <span data-ttu-id="2dce6-355">Isurfaceproducer:: Flush</span><span class="sxs-lookup"><span data-stu-id="2dce6-355">ISurfaceProducer::Flush</span></span>   | <span data-ttu-id="2dce6-356">Wird verwendet, wenn die Anwendungen nicht blockierende Verhalten aufweisen sollten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-356">Used if the applications should have non-blocking behavior.</span></span> <span data-ttu-id="2dce6-357">Einzelheiten finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-357">See Remarks for details.</span></span>                                                                  |



 

<span data-ttu-id="2dce6-358">**Einreihen in die Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="2dce6-358">**Enqueue**</span></span>  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



<span data-ttu-id="2dce6-359">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-359">**Parameters**</span></span>  
<span data-ttu-id="2dce6-360">*pSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2dce6-360">*pSurface* \[in\]</span></span>  
<span data-ttu-id="2dce6-361">Die Oberfläche des produzierenden Geräts, das in die Warteschlange eingereiht werden muss.</span><span class="sxs-lookup"><span data-stu-id="2dce6-361">The surface of the producing device that needs to be enqueued.</span></span> <span data-ttu-id="2dce6-362">Dabei muss es sich um eine aus der Warteschlange entfernte Oberfläche aus demselben Warteschlangen Netzwerk handeln.</span><span class="sxs-lookup"><span data-stu-id="2dce6-362">This surface must be a dequeued surface from the same queue network.</span></span> <span data-ttu-id="2dce6-363">*pbuffer* \[ in \] einem optionalen Parameter, der verwendet wird, um Metadaten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-363">*pBuffer* \[in\] An optional parameter, which is used to pass in metadata.</span></span> <span data-ttu-id="2dce6-364">Er sollte auf die Daten zeigen, die an den Befehl zum Entfernen aus der Warteschlange weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-364">It should point to the data that will be passed on to the dequeue call.</span></span>  
<span data-ttu-id="2dce6-365">*BufferSize* \[ in \] der Größe von *pbuffer*(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="2dce6-365">*BufferSize* \[in\] The size of *pBuffer*, in bytes.</span></span>  
<span data-ttu-id="2dce6-366">*Flags* \[ in \] einem optionalen Parameter, der das Verhalten dieser Funktion steuert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-366">*Flags* \[in\] An optional parameter that controls the behavior of this function.</span></span> <span data-ttu-id="2dce6-367">Das einzige Flag ist das Surface \_ Queue- \_ Flag \_ \_ nicht \_ warten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-367">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="2dce6-368">Weitere Informationen finden Sie in den Hinweisen zum leeren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-368">See the Remarks for Flush.</span></span> <span data-ttu-id="2dce6-369">Wenn kein Flag (*Flags* = = 0) überschritten wird, wird das standardmäßige Blockierungs Verhalten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-369">If no flag is passed (*Flags* == 0), then the default blocking behavior is used.</span></span>  
</dl>

<span data-ttu-id="2dce6-370">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-370">**Return Values**</span></span>

<span data-ttu-id="2dce6-371">Diese Funktion kann den DXGI-Fehler zurückgeben, \_ \_ Wenn das \_ \_ \_ Flag für die nicht Wartezeit der Surface-Warteschlange \_ \_ \_ \_ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-371">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if a SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span>  
</dl>

<span data-ttu-id="2dce6-372">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-372">**Remarks**</span></span>

-   <span data-ttu-id="2dce6-373">Diese Funktion setzt die-Oberfläche in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-373">This function puts the surface on the queue.</span></span> <span data-ttu-id="2dce6-374">Wenn die Anwendung kein Surface \_ Queue \_ -Flag angibt \_ \_ \_ , wird diese Funktion blockiert und führt eine GPU-CPU-Synchronisierung durch, um sicherzustellen, dass das gesamte Rendering auf der in die Warteschlange eingereihten Oberfläche vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-374">If the application does not specify SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT, this function is blocking and will do a GPU-CPU synchronization to assure that all the rendering on the enqueued surface is complete.</span></span> <span data-ttu-id="2dce6-375">Wenn diese Funktion erfolgreich ausgeführt wird, steht eine Oberfläche zum Entfernen aus der Warteschlange zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2dce6-375">If this function succeeds, a surface will be available for dequeue.</span></span> <span data-ttu-id="2dce6-376">Wenn Sie ein nicht blockierendes Verhalten wünschen, verwenden Sie das \_ \_ Flag nicht warten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-376">If you want non-blocking behavior, use the DO\_NOT\_WAIT flag.</span></span> <span data-ttu-id="2dce6-377">Weitere Informationen finden Sie unter Flush ().</span><span class="sxs-lookup"><span data-stu-id="2dce6-377">See Flush() for details.</span></span>
-   <span data-ttu-id="2dce6-378">Gemäß den Regeln für die COM-Verweis Zählung wird die von "toqueue" zurückgegebene Oberfläche "adressf ()" verwendet, damit die Anwendung dies nicht tun muss.</span><span class="sxs-lookup"><span data-stu-id="2dce6-378">As per the COM reference counting rules, the surface returned by Dequeue will be AddRef() so the application does not need to do this.</span></span> <span data-ttu-id="2dce6-379">Nach dem Aufrufen von Enqueue muss die Anwendung die Oberfläche freigeben, da Sie Sie nicht mehr verwenden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-379">After calling Enqueue, the application must Release the surface because they are no longer using it.</span></span>

<span data-ttu-id="2dce6-380">**Leerung**</span><span class="sxs-lookup"><span data-stu-id="2dce6-380">**Flush**</span></span>  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



<span data-ttu-id="2dce6-381">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2dce6-381">**Parameters**</span></span>  
<span data-ttu-id="2dce6-382">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2dce6-382">*Flags* \[in\]</span></span>  
<span data-ttu-id="2dce6-383">Das einzige Flag ist das Surface \_ Queue- \_ Flag \_ \_ nicht \_ warten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-383">The only flag is SURFACE\_QUEUE\_FLAG\_ DO\_NOT\_WAIT.</span></span> <span data-ttu-id="2dce6-384">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2dce6-384">See Remarks.</span></span> <span data-ttu-id="2dce6-385">*noberflächen* \[ Out \] gibt die Anzahl der Oberflächen zurück, die noch ausstehend sind und nicht geleert werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-385">*nSurfaces* \[out\] Returns the number of surfaces that are still pending and not flushed.</span></span>  
</dl>

<span data-ttu-id="2dce6-386">**Rückgabewerte**</span><span class="sxs-lookup"><span data-stu-id="2dce6-386">**Return Values**</span></span>

<span data-ttu-id="2dce6-387">Diese Funktion kann den DXGI-Fehler zurückgeben, \_ \_ \_ \_ Wenn das Flag für die Surface- \_ Warteschlange \_ \_ \_ nicht \_ gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-387">This function can return DXGI\_ERROR\_WAS\_STILL\_DRAWING if the SURFACE\_QUEUE\_FLAG\_DO\_NOT\_WAIT flag is used.</span></span> <span data-ttu-id="2dce6-388">Diese Funktion gibt S \_ OK zurück, wenn beliebige Oberflächen erfolgreich geleert wurden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-388">This function returns S\_OK if any surfaces were successfully flushed.</span></span> <span data-ttu-id="2dce6-389">Diese Funktion gibt den DXGI-Fehler zurück, der \_ \_ \_ nur gezeichnet wurde, \_ Wenn keine Oberflächen geleert wurden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-389">This function returns DXGI\_ERROR\_WAS\_STILL\_DRAWING only if no surfaces were flushed.</span></span> <span data-ttu-id="2dce6-390">Zusammen geben der Rückgabewert und die *Oberflächen* für die Anwendung an, welche Arbeit durchgeführt wurde und ob eine beliebige Arbeit zu erledigen ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-390">Together, the return value and *nSurfaces* indicate to the application what work has been done and if any work is left to do.</span></span>  
</dl>

<span data-ttu-id="2dce6-391">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-391">**Remarks**</span></span>

<span data-ttu-id="2dce6-392">Der Löschvorgang ist nur sinnvoll, wenn der vorherige aufrubungsvorgang das Flag "nicht warten" verwendet \_ \_ hat, andernfalls ist es ein No-op.</span><span class="sxs-lookup"><span data-stu-id="2dce6-392">Flush is meaningful only if the previous call to enqueue used the DO\_NOT\_WAIT flag; otherwise, it will be a no-op.</span></span> <span data-ttu-id="2dce6-393">Wenn der aufzurufende aufrubungsvorgang das \_ \_ Flag nicht warten verwendet hat, wird der einreihen-Vorgang sofort zurückgegeben, und die GPU-CPU-Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="2dce6-393">If the call to enqueue used the DO\_NOT\_WAIT flag, enqueue returns immediately and the GPU-CPU synchronization is not guaranteed.</span></span> <span data-ttu-id="2dce6-394">Die Oberfläche wird weiterhin in die Warteschlange eingereiht, das ermittelende Gerät kann Sie jedoch nicht mehr verwenden, ist aber nicht zum Entfernen aus der Warteschlange verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2dce6-394">The surface is still considered enqueued, the producing device cannot continue using it, but it is not available for dequeue.</span></span> <span data-ttu-id="2dce6-395">Um zu versuchen, ein Commit für die-Oberfläche zum Entfernen aus der Warteschlange auszuführen, muss Flush aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-395">In order to try to commit the surface for dequeue, Flush must be called.</span></span> <span data-ttu-id="2dce6-396">"Flush" versucht, alle Oberflächen zu übertragen, die gerade in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-396">Flush attempts to commit all of the surfaces that are currently enqueued.</span></span> <span data-ttu-id="2dce6-397">Wenn kein Flag an Flush weitergegeben wird, wird die gesamte Warteschlange blockiert und gelöscht, und alle darin ausgefallenen Oberflächen werden zum Entfernen aus der Warteschlange gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2dce6-397">If no flag is passed to Flush, it will block and clear out the entire queue, readying all surfaces in it for dequeue.</span></span> <span data-ttu-id="2dce6-398">Wenn das \_ Flag nicht \_ warten verwendet wird, überprüft die Warteschlange die Oberflächen, um festzustellen, ob Sie bereit sind. dieser Schritt ist nicht blockierend.</span><span class="sxs-lookup"><span data-stu-id="2dce6-398">If the DO\_NOT\_WAIT flag is used, the queue will check the surfaces to see if any of them are ready; this step is non-blocking.</span></span> <span data-ttu-id="2dce6-399">Oberflächen, die die GPU-CPU-Synchronisierung abgeschlossen haben, sind für das consumergerät bereit.</span><span class="sxs-lookup"><span data-stu-id="2dce6-399">Surfaces that have finished the GPU-CPU sync will be ready for the consumer device.</span></span> <span data-ttu-id="2dce6-400">Noch ausstehende Oberflächen sind nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-400">Surfaces that are still pending will be unaffected.</span></span> <span data-ttu-id="2dce6-401">Die-Funktion gibt die Anzahl der Oberflächen zurück, die noch geleert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-401">The function returns the number of surfaces that still need to be flushed.</span></span>

> [!Note]  
> <span data-ttu-id="2dce6-402">Das leeren führt nicht zu einer Unterbrechung der Warteschlangen Semantik.</span><span class="sxs-lookup"><span data-stu-id="2dce6-402">Flush will not break the queue semantics.</span></span> <span data-ttu-id="2dce6-403">Die API stellt sicher, dass für in die Warteschlange eingereihte Oberflächen zuerst ein Commit ausgeführt wird, bevor die Oberflächen später in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-403">The API guarantees that surfaces enqueued first will be committed before surfaces enqueued later, regardless of when the GPU-CPU sync happens.</span></span>

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a><span data-ttu-id="2dce6-404">Direct3D 9Ex und DXGI Interop Helper: Verwendung</span><span class="sxs-lookup"><span data-stu-id="2dce6-404">Direct3D 9Ex and DXGI Interop Helper: How To Use</span></span>

<span data-ttu-id="2dce6-405">Wir gehen davon aus, dass die meisten Verwendungs Fälle zwei Geräte umfassen, die eine Reihe von Oberflächen gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-405">We expect most of the usage cases to involve two devices sharing a number of surfaces.</span></span> <span data-ttu-id="2dce6-406">Da dies auch das einfachste Szenario ist, wird in diesem Dokument ausführlich erläutert, wie die APIs verwendet werden, um dieses Ziel zu erreichen, eine nicht blockierende Variation erläutert und mit einem kurzen Abschnitt über die Initialisierung von drei Geräten endet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-406">Because this also happens to be the simplest scenario, this paper details how to use the APIs to achieve this goal, discusses a non-blocking variation, and ends with a brief section about initializing for three devices.</span></span>

### <a name="two-devices"></a><span data-ttu-id="2dce6-407">Zwei Geräte</span><span class="sxs-lookup"><span data-stu-id="2dce6-407">Two Devices</span></span>

<span data-ttu-id="2dce6-408">Die Beispielanwendung, die dieses Hilfsprogramm verwendet, kann Direct3D 9Ex und Direct3D 11 gleichzeitig verwenden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-408">The example application that uses this helper can use Direct3D 9Ex and Direct3D 11 together.</span></span> <span data-ttu-id="2dce6-409">Die Anwendung kann Inhalte mit beiden Geräten verarbeiten und Inhalte mithilfe von Direct3D 9 präsentieren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-409">The application can process content with both devices, and present content using Direct3D 9.</span></span> <span data-ttu-id="2dce6-410">Die Verarbeitung kann das Rendern von Inhalten, das Decodieren von Videos, das Ausführen von Compute-Shadern usw. bedeuten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-410">Processing could mean rendering content, decoding video, running compute shaders, and so on.</span></span> <span data-ttu-id="2dce6-411">Die Anwendung wird für jeden Frame zuerst mit Direct3D 11 verarbeitet und dann mit Direct3D 9 und schließlich mit Direct3D 9 verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-411">For every frame, the application will first process with Direct3D 11, then process with Direct3D 9, and finally present with Direct3D 9.</span></span> <span data-ttu-id="2dce6-412">Darüber hinaus werden bei der Verarbeitung mit Direct3D 11 einige Metadaten erzeugt, die der vorhandene Direct3D 9 verbrauchen muss.</span><span class="sxs-lookup"><span data-stu-id="2dce6-412">Furthermore, the processing with Direct3D 11 will produce some metadata that the Direct3D 9 present will need to consume.</span></span> <span data-ttu-id="2dce6-413">In diesem Abschnitt wird die Verwendung von Hilfsprogrammen in drei Teilen behandelt, die dieser Sequenz entsprechen: Initialisierung, Hauptschleife und Cleanup.</span><span class="sxs-lookup"><span data-stu-id="2dce6-413">This section covers the helper usage in three parts that correspond to this sequence: Initialization, Main Loop, and Cleanup.</span></span>

<span data-ttu-id="2dce6-414">**Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="2dce6-414">**Initialization**</span></span>  
<span data-ttu-id="2dce6-415">Die Initialisierung umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="2dce6-415">Initialization involves the following steps:</span></span>  

1.  <span data-ttu-id="2dce6-416">Initialisieren Sie beide Geräte.</span><span class="sxs-lookup"><span data-stu-id="2dce6-416">Initialize both devices.</span></span>
2.  <span data-ttu-id="2dce6-417">Erstellen Sie die Stamm Warteschlange: m \_ 11warte Schlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-417">Create the Root Queue: m\_11to9Queue.</span></span>
3.  <span data-ttu-id="2dce6-418">Aus der Stamm Warteschlange Klonen: m \_ 9on11queue.</span><span class="sxs-lookup"><span data-stu-id="2dce6-418">Clone from the Root Queue: m\_9to11Queue.</span></span>
4.  <span data-ttu-id="2dce6-419">Openproducer/openconsumer in beiden Warteschlangen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-419">Call OpenProducer/OpenConsumer on both queues.</span></span>

<span data-ttu-id="2dce6-420">In den Warteschlangen Namen werden die Nummern 9 und 11 verwendet, um anzugeben, welche API der Producer ist und welche der Consumer: **m \_ ***Producer*** to ***Consumer*** Queue** ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-420">The queue names use the numbers 9 and 11 to indicate which API is the producer and which is the consumer: **m\_\*\*\*producer**\* to ***consumer*** Queue\*\*.</span></span> <span data-ttu-id="2dce6-421">Entsprechend gibt m \_ 11warte Schlange eine Warteschlange an, für die das Gerät Direct3D 11 Oberflächen erzeugt, die vom Direct3D 9-Gerät genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-421">Accordingly, m\_11to9Queue indicates a queue for which the Direct3D 11 device produces surfaces that the Direct3D 9 device consumes.</span></span> <span data-ttu-id="2dce6-422">Entsprechend \_ gibt die Warteschlange "m 9to 11" eine Warteschlange an, für die Direct3D 9 Oberflächen erzeugt, die Direct3D 11 nutzt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-422">Similarly, m\_9to11Queue indicates a queue for which Direct3D 9 produces surfaces that Direct3D 11 consumes.</span></span>  
<span data-ttu-id="2dce6-423">Die Stamm Warteschlange ist anfänglich voll und alle geklonten Warteschlangen sind anfänglich leer</span><span class="sxs-lookup"><span data-stu-id="2dce6-423">The Root queue is initially full and all cloned queues are initially empty.</span></span> <span data-ttu-id="2dce6-424">Dies sollte für die Anwendung kein Problem darstellen, mit Ausnahme des ersten Durchlaufs der Enqueues und aus der Warteschlange und der Verfügbarkeit von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-424">This should not be a problem for the application except for the first cycle of the Enqueues and Dequeues and the availability of metadata.</span></span> <span data-ttu-id="2dce6-425">Wenn ein aus der Warteschlange eingereiht wird, dass keine Metadaten vorhanden sind, aber keine festgelegt wurde (weil anfänglich nichts vorhanden ist oder die einreihen nichts festgelegt hat), wird von der Warteschlange festgestellt, dass keine Metadaten</span><span class="sxs-lookup"><span data-stu-id="2dce6-425">If a dequeue asks for metadata but none was set (either because nothing is there initially or the enqueue did not set anything), dequeue sees that no metadata was received.</span></span>  

1.  <span data-ttu-id="2dce6-426">**Initialisieren Sie beide Geräte.**</span><span class="sxs-lookup"><span data-stu-id="2dce6-426">**Initialize Both Devices.**</span></span>  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  <span data-ttu-id="2dce6-427">**Erstellen Sie die Stamm Warteschlange.**</span><span class="sxs-lookup"><span data-stu-id="2dce6-427">**Create the Root Queue.**</span></span>  
    <span data-ttu-id="2dce6-428">Dieser Schritt erstellt auch die-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-428">This step also creates the surfaces.</span></span> <span data-ttu-id="2dce6-429">Größen-und Format Einschränkungen sind identisch mit der Erstellung einer freigegebenen Ressource.</span><span class="sxs-lookup"><span data-stu-id="2dce6-429">Size and format restrictions are identical to creating any shared resource.</span></span> <span data-ttu-id="2dce6-430">Die Größe des metadatenpuffers ist zur Erstellungszeit korrigiert, und in diesem Fall wird nur ein uint übergeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-430">The size of the metadata buffer is fixed at create time, and in this case, we'll just be passing a UINT.</span></span>  
    <span data-ttu-id="2dce6-431">Die Warteschlange muss mit einer bestimmten Anzahl von Oberflächen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-431">The queue must be created with a fixed number of surfaces.</span></span> <span data-ttu-id="2dce6-432">Die Leistung variiert abhängig vom jeweiligen Szenario.</span><span class="sxs-lookup"><span data-stu-id="2dce6-432">Performance will vary depending on the scenario.</span></span> <span data-ttu-id="2dce6-433">Das vorhanden sein mehrerer Oberflächen erhöht die Wahrscheinlichkeit, dass Geräte ausgelastet sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-433">Having multiple surfaces increases the chances that devices are busy.</span></span> <span data-ttu-id="2dce6-434">Wenn es z. b. nur eine Oberfläche gibt, erfolgt keine Parallelisierung zwischen den beiden Geräten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-434">For example, if there is only one surface, then there will be no parallelization between the two devices.</span></span> <span data-ttu-id="2dce6-435">Andererseits erhöht das Erhöhen der Anzahl der Oberflächen den Speicherbedarf, wodurch die Leistung beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2dce6-435">On the other hand, increasing the number of surfaces increases the memory footprint, which can degrade performance.</span></span> <span data-ttu-id="2dce6-436">In diesem Beispiel werden zwei Oberflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-436">This example uses two surfaces.</span></span>  
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

    

3.  <span data-ttu-id="2dce6-437">**Klonen Sie die Stamm Warteschlange.**</span><span class="sxs-lookup"><span data-stu-id="2dce6-437">**Clone the Root Queue.**</span></span>  
    <span data-ttu-id="2dce6-438">Jede geklonte Warteschlange muss die gleichen Oberflächen verwenden, kann jedoch unterschiedliche metadatenpuffergrößen und andere Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-438">Each cloned queue must use the same surfaces but can have different metadata buffer sizes and different flags.</span></span> <span data-ttu-id="2dce6-439">In diesem Fall sind keine Metadaten von Direct3D 9 bis Direct3D 11 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-439">In this case, there is no metadata from Direct3D 9 to Direct3D 11.</span></span>  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  <span data-ttu-id="2dce6-440">**Öffnen Sie die Geräte Producer und Consumer.**</span><span class="sxs-lookup"><span data-stu-id="2dce6-440">**Open the Producer and Consumer Devices.**</span></span>  
    <span data-ttu-id="2dce6-441">Die Anwendung muss diesen Schritt ausführen, bevor Enqueue und Dequeue aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-441">The application must perform this step before calling Enqueue and Dequeue.</span></span> <span data-ttu-id="2dce6-442">Beim Öffnen eines Producer und Consumer werden Schnittstellen zurückgegeben, die die Enqueue-/Dequeue-APIs enthalten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-442">Opening a producer and consumer returns interfaces which contain the enqueue/dequeue APIs.</span></span>  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

<span data-ttu-id="2dce6-443">**Hauptschleife**</span><span class="sxs-lookup"><span data-stu-id="2dce6-443">**Main Loop**</span></span>  
<span data-ttu-id="2dce6-444">Die Verwendung der Warteschlange wird nach dem klassischen Producer/Consumer-Problem modelliert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-444">The usage of the queue is modeled after the classical producer/consumer problem.</span></span> <span data-ttu-id="2dce6-445">Stellen Sie sich dies aus der Perspektive pro Gerät vor.</span><span class="sxs-lookup"><span data-stu-id="2dce6-445">Think of this from a per-device perspective.</span></span> <span data-ttu-id="2dce6-446">Jedes Gerät muss die folgenden Schritte ausführen: Entfernen Sie die Warteschlange, um eine Oberfläche von der Warteschlange zu erhalten, und verarbeiten Sie Sie auf der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2dce6-446">Each device must perform these steps: dequeue to get a surface from its consuming queue, process on the surface, and then enqueue onto its producing queue.</span></span> <span data-ttu-id="2dce6-447">Für das Gerät Direct3D 11 ist die Verwendung von Direct3D 9 nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="2dce6-447">For the Direct3D 11 device, the Direct3D 9 usage is almost identical.</span></span>  


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



<span data-ttu-id="2dce6-448">**Bereinigen**</span><span class="sxs-lookup"><span data-stu-id="2dce6-448">**Cleaning Up**</span></span>  
<span data-ttu-id="2dce6-449">Dieser Schritt ist sehr unkompliziert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-449">This step is very straightforward.</span></span> <span data-ttu-id="2dce6-450">Zusätzlich zu den normalen Schritten zum Bereinigen von Direct3D-APIs muss die Anwendung die Rückgabe-com-Schnittstellen freigeben.</span><span class="sxs-lookup"><span data-stu-id="2dce6-450">In addition to the normal steps for cleaning up Direct3D APIs, the application must release the return COM interfaces.</span></span>  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a><span data-ttu-id="2dce6-451">Nicht blockierende Verwendung</span><span class="sxs-lookup"><span data-stu-id="2dce6-451">Non-Blocking Use</span></span>

<span data-ttu-id="2dce6-452">Das vorherige Beispiel ist für einen multithreadnutzungsfall sinnvoll, bei dem jedes Gerät über einen eigenen Thread verfügt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-452">The previous example makes sense for a multithreaded usage case in which each device has its own thread.</span></span> <span data-ttu-id="2dce6-453">In diesem Beispiel werden die blockierenden Versionen der APIs verwendet: unendlich für Timeout und kein Flag zum Einreihen in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2dce6-453">The example uses the blocking versions of the APIs: INFINITE for timeout, and no flag to enqueue.</span></span> <span data-ttu-id="2dce6-454">Wenn Sie das Hilfsprogramm auf nicht blockierende Weise verwenden möchten, müssen Sie nur einige Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-454">If you want to use the helper in a non-blocking way, you need to make only a few changes.</span></span> <span data-ttu-id="2dce6-455">In diesem Abschnitt wird die nicht blockierende Verwendung für beide Geräte in einem Thread veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2dce6-455">This section shows non-blocking use with both devices on one thread.</span></span>

<span data-ttu-id="2dce6-456">**Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="2dce6-456">**Initialization**</span></span>  
<span data-ttu-id="2dce6-457">Die Initialisierung ist mit Ausnahme der Flags identisch.</span><span class="sxs-lookup"><span data-stu-id="2dce6-457">Initialization is identical except for the flags.</span></span> <span data-ttu-id="2dce6-458">Da es sich bei der Anwendung um einen Single Thread handelt, verwenden Sie dieses Flag für die Erstellung.</span><span class="sxs-lookup"><span data-stu-id="2dce6-458">Because the application is single-threaded, use that flag for creation.</span></span> <span data-ttu-id="2dce6-459">Dadurch wird ein Teil des Synchronisierungs Codes deaktiviert, wodurch die Leistung möglicherweise verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-459">This turns off some of the synchronization code, which potentially improves performance.</span></span>  


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



<span data-ttu-id="2dce6-460">Das Öffnen von Producer-und Consumer-Geräten ist dasselbe wie im Blockierungs Beispiel.</span><span class="sxs-lookup"><span data-stu-id="2dce6-460">Opening the producer and consumer devices are the same as in the blocking example.</span></span>  
<span data-ttu-id="2dce6-461">**Verwenden der Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="2dce6-461">**Using the Queue**</span></span>  
<span data-ttu-id="2dce6-462">Es gibt viele Möglichkeiten, die Warteschlange in einer nicht blockierenden Weise mit verschiedenen Leistungsmerkmalen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-462">There are many ways of using the queue in a non-blocking fashion with various performance characteristics.</span></span> <span data-ttu-id="2dce6-463">Das folgende Beispiel ist einfach, hat jedoch aufgrund übermäßiger Drehung und Abruf eine schlechte Leistung.</span><span class="sxs-lookup"><span data-stu-id="2dce6-463">The following example is simple but has poor performance due to excessive spinning and polling.</span></span> <span data-ttu-id="2dce6-464">Trotz dieser Probleme zeigt das Beispiel, wie das Hilfsprogramm verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2dce6-464">Despite these problems, the example shows how to use the helper.</span></span> <span data-ttu-id="2dce6-465">Der Ansatz besteht darin, ständig in einer Schleife zu sitzen und aus der Warteschlange zu entfernen, Sie zu verarbeiten, in die Warteschlange zu stellen</span><span class="sxs-lookup"><span data-stu-id="2dce6-465">The approach is to constantly sit in a loop and dequeue, process, enqueue, and flush.</span></span> <span data-ttu-id="2dce6-466">Wenn einer der Schritte fehlschlägt, weil die Ressource nicht verfügbar ist, versucht die Anwendung einfach erneut, die nächste Schleife auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-466">If any of the steps fail because the resource is not available, the application simply tries again the next loop.</span></span>  


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



<span data-ttu-id="2dce6-467">Eine komplexere Lösung könnte den Rückgabewert von einreihen und von Flush überprüfen, um zu bestimmen, ob eine Leerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2dce6-467">A more complex solution could check the return value from enqueue and from flush to determine if flushing is necessary.</span></span>  
</dl>

### <a name="three-devices"></a><span data-ttu-id="2dce6-468">Drei Geräte</span><span class="sxs-lookup"><span data-stu-id="2dce6-468">Three Devices</span></span>

<span data-ttu-id="2dce6-469">Das Erweitern der vorherigen Beispiele auf mehrere Geräte ist einfach.</span><span class="sxs-lookup"><span data-stu-id="2dce6-469">Extending the previous examples to cover multiple devices is straightforward.</span></span> <span data-ttu-id="2dce6-470">Der folgende Code führt die Initialisierung aus.</span><span class="sxs-lookup"><span data-stu-id="2dce6-470">The following code performs the initialization.</span></span> <span data-ttu-id="2dce6-471">Nachdem die Producer/Consumer-Objekte erstellt wurden, ist der Code für die Verwendung identisch.</span><span class="sxs-lookup"><span data-stu-id="2dce6-471">After the Producer/Consumer objects have been created, the code to use them is the same.</span></span> <span data-ttu-id="2dce6-472">Dieses Beispiel enthält drei Geräte und somit drei Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-472">This example has three devices and therefore three queues.</span></span> <span data-ttu-id="2dce6-473">Die Oberflächen werden von Direct3D 9 bis Direct3D 10 bis Direct3D 11 abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2dce6-473">Surfaces flow from Direct3D 9 to Direct3D 10 to Direct3D 11.</span></span>


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



<span data-ttu-id="2dce6-474">Wie bereits erwähnt, funktioniert das Klonen auf dieselbe Weise, unabhängig davon, welche Warteschlange geklont wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-474">As mentioned earlier, cloning works the same way, no matter which queue is cloned.</span></span> <span data-ttu-id="2dce6-475">Beispielsweise könnte der zweite Klon-Befehl aus dem Objekt "m \_ 9to 10queue" entfernt worden sein.</span><span class="sxs-lookup"><span data-stu-id="2dce6-475">For example, the second Clone call could have been off of the m\_9to10Queue object.</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="2dce6-476">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2dce6-476">Conclusion</span></span>

<span data-ttu-id="2dce6-477">Sie können Lösungen erstellen, die mithilfe von Interoperabilität die Leistungsfähigkeit mehrerer DirectX-APIs nutzen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-477">You can create solutions that use interoperability to employ the power of multiple DirectX APIs.</span></span> <span data-ttu-id="2dce6-478">Die Interoperabilität der Windows-Grafik-API bietet nun eine Common Surface Management Runtime DXGI 1,1.</span><span class="sxs-lookup"><span data-stu-id="2dce6-478">Windows graphics API interoperability now offers a common surface management runtime DXGI 1.1.</span></span> <span data-ttu-id="2dce6-479">Diese Laufzeit ermöglicht die Unterstützung synchroner Oberflächen Freigabe in neu entwickelten APIs, z. b. Direct3D 11, Direct3D 10,1 und Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2dce6-479">This runtime enables synchronized surface sharing support within newly developed APIs, such as Direct3D 11, Direct3D 10.1 and Direct2D.</span></span> <span data-ttu-id="2dce6-480">Die Verbesserungen der Interoperabilität zwischen neuen APIs und vorhandenen APIs unterstützen die Anwendungs Migration und Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="2dce6-480">Interoperability improvements between new APIs and existing APIs aid application migration and backward compatibility.</span></span> <span data-ttu-id="2dce6-481">Die Consumer-APIs Direct3D 9Ex und DXGI 1,1 können zusammenarbeiten, wie Sie mit dem Synchronisierungs Mechanismus veranschaulicht werden, der durch Sample Helper Code in der MSDN Code Gallery bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-481">Direct3D 9Ex and DXGI 1.1 consumer APIs can interoperate, as shown with the synchronization mechanism provided through sample helper code on MSDN Code Gallery.</span></span>

 

 