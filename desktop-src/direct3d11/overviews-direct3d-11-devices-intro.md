---
title: Einführung in ein Gerät in Direct3D 11
description: Das Objektmodell Direct3D 11 trennt die Ressourcen Erstellung und Renderingfunktionalität in ein Gerät und einen oder mehrere Kontexte. Diese Trennung dient zum Vereinfachen von Multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976049"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a><span data-ttu-id="71dce-103">Einführung in ein Gerät in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="71dce-103">Introduction to a Device in Direct3D 11</span></span>

<span data-ttu-id="71dce-104">Das Objektmodell Direct3D 11 trennt die Ressourcen Erstellung und Renderingfunktionalität in ein Gerät und einen oder mehrere Kontexte. Diese Trennung dient zum Vereinfachen von Multithreading.</span><span class="sxs-lookup"><span data-stu-id="71dce-104">The Direct3D 11 object model separates resource creation and rendering functionality into a device and one or more contexts; this separation is designed to facilitate multithreading.</span></span>

-   [<span data-ttu-id="71dce-105">Device</span><span class="sxs-lookup"><span data-stu-id="71dce-105">Device</span></span>](#introduction-to-a-device-in-direct3d-11)
-   [<span data-ttu-id="71dce-106">Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="71dce-106">Device Context</span></span>](#device-context)
    -   [<span data-ttu-id="71dce-107">Sofortiger Kontext</span><span class="sxs-lookup"><span data-stu-id="71dce-107">Immediate Context</span></span>](#immediate-context)
    -   [<span data-ttu-id="71dce-108">Verzögerter Kontext</span><span class="sxs-lookup"><span data-stu-id="71dce-108">Deferred Context</span></span>](#deferred-context)
-   [<span data-ttu-id="71dce-109">Überlegungen zum Threading</span><span class="sxs-lookup"><span data-stu-id="71dce-109">Threading Considerations</span></span>](#threading-considerations)
-   [<span data-ttu-id="71dce-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71dce-110">Related topics</span></span>](#related-topics)

## <a name="device"></a><span data-ttu-id="71dce-111">Sicherungsmedium</span><span class="sxs-lookup"><span data-stu-id="71dce-111">Device</span></span>

<span data-ttu-id="71dce-112">Ein Gerät wird zum Erstellen von Ressourcen und zum Auflisten der Funktionen eines Anzeige Adapters verwendet.</span><span class="sxs-lookup"><span data-stu-id="71dce-112">A device is used to create resources and to enumerate the capabilities of a display adapter.</span></span> <span data-ttu-id="71dce-113">In Direct3D 11 wird ein Gerät mit einer [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="71dce-113">In Direct3D 11, a device is represented with an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface.</span></span>

<span data-ttu-id="71dce-114">Jede Anwendung muss mindestens ein Gerät aufweisen, die meisten Anwendungen erstellen nur ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="71dce-114">Each application must have at least one device, most applications only create one device.</span></span> <span data-ttu-id="71dce-115">Erstellen Sie ein Gerät für einen der Hardwaretreiber, die auf Ihrem Computer installiert sind, indem Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) aufrufen und den Treibertyp mit dem [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) -Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="71dce-115">Create a device for one of the hardware drivers installed on your machine by calling [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and specify the driver type with the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) flag.</span></span> <span data-ttu-id="71dce-116">Jedes Gerät kann abhängig von der gewünschten Funktionalität einen oder mehrere Geräte Kontexte verwenden.</span><span class="sxs-lookup"><span data-stu-id="71dce-116">Each device can use one or more device contexts, depending on the functionality desired.</span></span>

## <a name="device-context"></a><span data-ttu-id="71dce-117">Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="71dce-117">Device Context</span></span>

<span data-ttu-id="71dce-118">Ein Gerätekontext enthält den Umstand oder die Einstellung, in der ein Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71dce-118">A device context contains the circumstance or setting in which a device is used.</span></span> <span data-ttu-id="71dce-119">Genauer gesagt wird ein Gerätekontext verwendet, um den Pipeline Status festzulegen und renderingbefehle mithilfe der Ressourcen zu generieren, die sich im Besitz eines Geräts befinden.</span><span class="sxs-lookup"><span data-stu-id="71dce-119">More specifically, a device context is used to set pipeline state and generate rendering commands using the resources owned by a device.</span></span> <span data-ttu-id="71dce-120">Direct3D 11 implementiert zwei Arten von Geräte Kontexten, eine für sofortiges Rendering und die andere für verzögertes Rendering. Beide Kontexte werden mit einer [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="71dce-120">Direct3D 11 implements two types of device contexts, one for immediate rendering and the other for deferred rendering; both contexts are represented with an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span>

### <a name="immediate-context"></a><span data-ttu-id="71dce-121">Sofortiger Kontext</span><span class="sxs-lookup"><span data-stu-id="71dce-121">Immediate Context</span></span>

<span data-ttu-id="71dce-122">Ein unmittelbarer Kontext wird direkt in den Treiber gerendert.</span><span class="sxs-lookup"><span data-stu-id="71dce-122">An immediate context renders directly to the driver.</span></span> <span data-ttu-id="71dce-123">Jedes Gerät verfügt über einen und nur einen unmittelbaren Kontext, der Daten von der GPU abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="71dce-123">Each device has one and only one immediate context which can retrieve data from the GPU.</span></span> <span data-ttu-id="71dce-124">Ein sofortiger Kontext kann verwendet werden, um eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)sofort zu Rendering (oder wiederzugeben).</span><span class="sxs-lookup"><span data-stu-id="71dce-124">An immediate context can be used to immediately render (or play back) a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span>

<span data-ttu-id="71dce-125">Es gibt zwei Möglichkeiten, einen unmittelbaren Kontext zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="71dce-125">There are two ways to get an immediate context:</span></span>

-   <span data-ttu-id="71dce-126">Durch Aufrufen von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="71dce-126">By calling either [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>
-   <span data-ttu-id="71dce-127">Durch Aufrufen von [**ID3D11Device:: getimmediatecontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span><span class="sxs-lookup"><span data-stu-id="71dce-127">By calling [**ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).</span></span>

### <a name="deferred-context"></a><span data-ttu-id="71dce-128">Verzögerter Kontext</span><span class="sxs-lookup"><span data-stu-id="71dce-128">Deferred Context</span></span>

<span data-ttu-id="71dce-129">Ein verzögerter Kontext zeichnet GPU-Befehle in einer [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)auf.</span><span class="sxs-lookup"><span data-stu-id="71dce-129">A deferred context records GPU commands into a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="71dce-130">Ein verzögerter Kontext wird hauptsächlich für Multithreading verwendet und ist für eine Single Thread-Anwendung nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="71dce-130">A deferred context is primarily used for multithreading and is not necessary for a single-threaded application.</span></span> <span data-ttu-id="71dce-131">Ein verzögerter Kontext wird im Allgemeinen von einem Arbeits Thread anstelle des hauptrenderingthreads verwendet.</span><span class="sxs-lookup"><span data-stu-id="71dce-131">A deferred context is generally used by a worker thread instead of the main rendering thread.</span></span> <span data-ttu-id="71dce-132">Wenn Sie einen verzögerten Kontext erstellen, erben Sie keinen Zustand aus dem unmittelbaren Kontext.</span><span class="sxs-lookup"><span data-stu-id="71dce-132">When you create a deferred context, it does not inherit any state from the immediate context.</span></span>

<span data-ttu-id="71dce-133">Um einen verzögerten Kontext abzurufen, nennen Sie [**ID3D11Device:: | atedeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="71dce-133">To get a deferred context, call [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

<span data-ttu-id="71dce-134">Jeder Kontext, der unmittelbar oder verzögert ist, kann in jedem Thread verwendet werden, solange der Kontext nur in einem Thread gleichzeitig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="71dce-134">Any context -- immediate or deferred -- can be used on any thread as long as the context is only used in one thread at a time.</span></span>

## <a name="threading-considerations"></a><span data-ttu-id="71dce-135">Überlegungen zum Threading</span><span class="sxs-lookup"><span data-stu-id="71dce-135">Threading Considerations</span></span>

<span data-ttu-id="71dce-136">In dieser Tabelle werden die Unterschiede im Threading Modell in Direct3D 11 aus früheren Versionen von Direct3D hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="71dce-136">This table highlights the differences in the threading model in Direct3D 11 from prior versions of Direct3D.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71dce-137">Unterschiede zwischen Direct3D 11 und früheren Versionen von Direct3D:</span><span class="sxs-lookup"><span data-stu-id="71dce-137">Differences between Direct3D 11 and previous versions of Direct3D:</span></span><br/> <span data-ttu-id="71dce-138">Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> -Schnittstellen Methoden sind frei Thread. Dies bedeutet, dass es sicher ist, dass mehrere Threads gleichzeitig die Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="71dce-138">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> interface methods are free-threaded, which means it is safe to have multiple threads call the functions at the same time.</span></span><br/>
<ul>
<li><span data-ttu-id="71dce-139">Alle <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-abgeleiteten Schnittstellen (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>usw.) sind frei Thread.</span><span class="sxs-lookup"><span data-stu-id="71dce-139">All <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>-derived interfaces (<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) are free-threaded.</span></span></li>
<li><span data-ttu-id="71dce-140">Direct3D 11 teilt das Erstellen und Rendern von Ressourcen in zwei Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="71dce-140">Direct3D 11 splits resource creating and rendering into two interfaces.</span></span> <span data-ttu-id="71dce-141">Map, unmap, BEGIN, End und GetData werden auf <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> implementiert, da <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> die Reihenfolge der Vorgänge stark definiert.</span><span class="sxs-lookup"><span data-stu-id="71dce-141">Map, Unmap, Begin, End, and GetData are implemented on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> because <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> strongly defines the order of operations.</span></span> <span data-ttu-id="71dce-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> -und <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> -Schnittstellen implementieren auch Methoden für frei Hand Thread Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="71dce-142"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> and <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> interfaces also implement methods for free-threaded operations.</span></span></li>
<li><span data-ttu-id="71dce-143">Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> -Methoden (mit Ausnahme derjenigen, die auf <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>vorhanden sind) sind nicht freigegeben, d. h., Sie erfordern ein einzelnes Threading.</span><span class="sxs-lookup"><span data-stu-id="71dce-143">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> methods (except for those that exist on <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) are not free-threaded, that is, they require single threading.</span></span> <span data-ttu-id="71dce-144">Nur ein Thread kann auf sichere Weise eine seiner Methoden (Draw, Copy, Map usw.) gleichzeitig aufrufen.</span><span class="sxs-lookup"><span data-stu-id="71dce-144">Only one thread may safely be calling any of its methods (Draw, Copy, Map, etc.) at a time.</span></span></li>
<li><span data-ttu-id="71dce-145">Im Allgemeinen minimiert das kostenlose Threading die Anzahl der verwendeten Synchronisierungs primitiven und deren Dauer.</span><span class="sxs-lookup"><span data-stu-id="71dce-145">In general, free-threading minimizes the number of synchronization primitives used as well as their duration.</span></span> <span data-ttu-id="71dce-146">Eine Anwendung, die die Synchronisierung für einen längeren Zeitraum verwendet, kann jedoch direkt beeinflussen, wie viel Parallelität eine Anwendung erwarten kann.</span><span class="sxs-lookup"><span data-stu-id="71dce-146">However, an application that uses synchronization held for a long time can directly impact how much concurrency an application can expect to achieve.</span></span></li>
</ul>
<span data-ttu-id="71dce-147">ID3D10Device-Schnittstellen Methoden sind nicht als frei Hand Thread konzipiert.</span><span class="sxs-lookup"><span data-stu-id="71dce-147">ID3D10Device interface methods are not designed to be free-threaded.</span></span> <span data-ttu-id="71dce-148">ID3D10Device implementiert alle Erstellungs-und Renderingfunktionen (wie ID3D9Device in Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="71dce-148">ID3D10Device implements all create and rendering functionality (as does ID3D9Device in Direct3D 9).</span></span> <span data-ttu-id="71dce-149">Map und unmap werden auf ID3D10Resource-abgeleiteten Schnittstellen implementiert, BEGIN, End und GetData werden auf von ID3D10Asynchronous abgeleiteten Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="71dce-149">Map and Unmap are implemented on ID3D10Resource-derived interfaces, Begin, End, and GetData are implemented on ID3D10Asynchronous-derived interfaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="71dce-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71dce-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71dce-151">Geräte</span><span class="sxs-lookup"><span data-stu-id="71dce-151">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





