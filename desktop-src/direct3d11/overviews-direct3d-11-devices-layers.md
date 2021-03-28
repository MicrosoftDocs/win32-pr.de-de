---
title: Software Ebenen
description: Die Direct3D 11-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten. In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516805"
---
# <a name="software-layers"></a><span data-ttu-id="3b9b4-104">Software Ebenen</span><span class="sxs-lookup"><span data-stu-id="3b9b4-104">Software Layers</span></span>

<span data-ttu-id="3b9b4-105">Die Direct3D 11-Laufzeit wird mit Ebenen erstellt, beginnend mit den grundlegenden Funktionen im Kern und der Erstellung Optionaler und Entwickler-Assist-Funktionen in äußeren Schichten.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="3b9b4-106">In diesem Abschnitt werden die Funktionen der einzelnen Ebenen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="3b9b4-107">Als allgemeine Regel fügen Ebenen Funktionen hinzu, ändern jedoch das vorhandene Verhalten nicht.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="3b9b4-108">Beispielsweise haben die Kernfunktionen die gleichen Rückgabewerte, die unabhängig von der instanziierten debugschicht sind, obwohl eine zusätzliche Debugausgabe bereitgestellt werden kann, wenn die debugschicht instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="3b9b4-109">Um Ebenen zu erstellen, wenn ein Gerät erstellt wird, rufen Sie [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) auf, und geben Sie mindestens ein [**D3D11 \_ Flag zum Erstellen des \_ Geräts \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) an.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="3b9b4-110">Direct3D 11 stellt die folgenden Lauf Zeitebenen bereit:</span><span class="sxs-lookup"><span data-stu-id="3b9b4-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="3b9b4-111">Kern Ebene</span><span class="sxs-lookup"><span data-stu-id="3b9b4-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="3b9b4-112">Ebene Debuggen</span><span class="sxs-lookup"><span data-stu-id="3b9b4-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="3b9b4-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b9b4-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="3b9b4-114">Kern Ebene</span><span class="sxs-lookup"><span data-stu-id="3b9b4-114">Core Layer</span></span>

<span data-ttu-id="3b9b4-115">Standardmäßig ist die Kern Ebene vorhanden. Bereitstellung einer sehr dünnen Zuordnung zwischen der API und dem Gerätetreiber, wodurch der Aufwand für hochfrequenzaufrufe minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="3b9b4-116">Da die Kern Ebene für die Leistung wichtig ist, wird nur eine kritische Validierung durchführt.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="3b9b4-117">Die übrigen Ebenen sind optional.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="3b9b4-118">Ebene Debuggen</span><span class="sxs-lookup"><span data-stu-id="3b9b4-118">Debug Layer</span></span>

<span data-ttu-id="3b9b4-119">Die Debug-Ebene bietet umfassende zusätzliche Parameter-und Konsistenz Validierung (z. b. das Überprüfen der shaderverknüpfung und Ressourcen Bindung, das Überprüfen der Parameter Konsistenz und das Melden von Fehlerbeschreibungen).</span><span class="sxs-lookup"><span data-stu-id="3b9b4-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="3b9b4-120">Um ein Gerät zu erstellen, das die debugschicht unterstützt, müssen Sie das DirectX SDK (zum Abrufen D3D11SDKLayers.dll) installieren und dann das **D3D11 \_ Create \_ Device \_ Debug** -Flag angeben, wenn Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion oder die [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="3b9b4-121">Wenn Sie die Anwendung mit aktivierter debugschicht ausführen, wird die Anwendung wesentlich langsamer.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="3b9b4-122">Um jedoch sicherzustellen, dass Ihre Anwendung Fehler und Warnungen vor dem Versenden bereinigt, verwenden Sie die Debug-Ebene.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="3b9b4-123">Weitere Informationen finden Sie unter [Verwenden der Debug-Ebene zum Debuggen von apps](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="3b9b4-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="3b9b4-124">Installieren Sie das Windows Software Development Kit (SDK) für Windows 7 (KB2670838) oder Windows 8. x, um ein Gerät zu erstellen, das die debugschicht unterstützt, und installieren Sie das Windows Software Development Kit (SDK) für Windows 8. x, um D3D111SDKLayers.dll zu erhalten \_ .</span><span class="sxs-lookup"><span data-stu-id="3b9b4-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="3b9b4-125">Aktivieren Sie für Windows 10 das optionale Feature "Graphics Tools", um ein Gerät zu erstellen, das die debugschicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="3b9b4-126">Wechseln Sie zum Bereich "Einstellungen" unter "System", "Apps & Features", "optionale Features verwalten", "Features hinzufügen", und suchen Sie nach "Grafik Tools".</span><span class="sxs-lookup"><span data-stu-id="3b9b4-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="3b9b4-127">Informationen zum Remote Debuggen von DirectX-apps finden Sie unter [Remote Debuggen von DirectX-apps](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="3b9b4-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="3b9b4-128">Alternativ können Sie das Debugflag mithilfe der [DirectX-Systemsteuerung](/previous-versions//bb219725(v=vs.85)) aktivieren bzw. deaktivieren, die als Teil des DirectX SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="3b9b4-129">Wenn die debugschicht Speicher Verluste auflistet, gibt Sie eine Liste von Objekt Schnittstellen Zeigern zusammen mit ihren anzeigen Amen aus.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="3b9b4-130">Der standardmäßige Anzeige Name ist " &lt; unbenannt &gt; ".</span><span class="sxs-lookup"><span data-stu-id="3b9b4-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="3b9b4-131">Sie können den anzeigen Amen mithilfe der [**ID3D11DeviceChild:: setprivatedata**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) -Methode und der **wkpdid \_ D3DDebugObjectName** GUID in D3Dcommon. h festlegen.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="3b9b4-132">Verwenden Sie z. b. den folgenden Code, um ptexture mit dem Namen des sdgers mytexture.jpg zu benennen:</span><span class="sxs-lookup"><span data-stu-id="3b9b4-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="3b9b4-133">In der Regel sollten Sie diese Aufrufe aus der Produktionsversion kompilieren.</span><span class="sxs-lookup"><span data-stu-id="3b9b4-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b9b4-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b9b4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b9b4-135">Geräte</span><span class="sxs-lookup"><span data-stu-id="3b9b4-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 