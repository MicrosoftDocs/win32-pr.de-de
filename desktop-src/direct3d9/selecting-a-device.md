---
description: Anwendungen können Hardware Abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen. Dieser Abschnitt enthält Informationen zu den Hauptaufgaben beim Auflisten von Anzeige Adaptern und Auswählen von Direct3D-Geräten.
ms.assetid: d140b90c-3a20-49f4-883b-662b6c05dcea
title: Auswählen eines Geräts (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdfa1faf38007f00959ac7263b4538954044688
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522763"
---
# <a name="selecting-a-device-direct3d-9"></a><span data-ttu-id="09b49-104">Auswählen eines Geräts (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="09b49-104">Selecting a Device (Direct3D 9)</span></span>

<span data-ttu-id="09b49-105">Anwendungen können Hardware Abfragen, um die unterstützten Direct3D-Gerätetypen zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="09b49-105">Applications can query hardware to detect the supported Direct3D device types.</span></span> <span data-ttu-id="09b49-106">Dieser Abschnitt enthält Informationen zu den Hauptaufgaben beim Auflisten von Anzeige Adaptern und Auswählen von Direct3D-Geräten.</span><span class="sxs-lookup"><span data-stu-id="09b49-106">This section contains information about the primary tasks involved in enumerating display adapters and selecting Direct3D devices.</span></span>

<span data-ttu-id="09b49-107">Eine Anwendung muss eine Reihe von Aufgaben ausführen, um ein entsprechendes Direct3D-Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="09b49-107">An application must perform a series of tasks to select an appropriate Direct3D device.</span></span> <span data-ttu-id="09b49-108">Beachten Sie, dass die folgenden Schritte für eine Vollbildanwendung vorgesehen sind und in den meisten Fällen eine Anwendung die meisten dieser Schritte überspringen kann.</span><span class="sxs-lookup"><span data-stu-id="09b49-108">Note that the following steps are intended for a full-screen application and that, in most cases, a windowed application can skip most of these steps.</span></span>

1.  <span data-ttu-id="09b49-109">Zuerst muss die Anwendung die Anzeige Adapter im System auflisten.</span><span class="sxs-lookup"><span data-stu-id="09b49-109">Initially, the application must enumerate the display adapters on the system.</span></span> <span data-ttu-id="09b49-110">Bei einem Adapter handelt es sich um eine physische Hardware.</span><span class="sxs-lookup"><span data-stu-id="09b49-110">An adapter is a physical piece of hardware.</span></span> <span data-ttu-id="09b49-111">Beachten Sie, dass die Grafikkarte möglicherweise mehr als einen Adapter enthält. Dies ist der Fall mit einer zweiköpfigen Anzeige.</span><span class="sxs-lookup"><span data-stu-id="09b49-111">Note that the graphics card might contain more than a single adapter, as is the case with a dual-headed display.</span></span> <span data-ttu-id="09b49-112">Anwendungen, die nicht die Unterstützung für mehrere Monitore betreffen, können diesen Schritt ignorieren und übergeben D3DADAPTER \_ standardmäßig an die [**IDirect3D9:: enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) -Methode in Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="09b49-112">Applications that are not concerned with multi-monitor support can disregard this step, and pass D3DADAPTER\_DEFAULT to the [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) method in step 2.</span></span>
2.  <span data-ttu-id="09b49-113">Für jeden Adapter listet die Anwendung die unterstützten Anzeigemodi durch Aufrufen von [**IDirect3D9:: enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)auf.</span><span class="sxs-lookup"><span data-stu-id="09b49-113">For each adapter, the application enumerates the supported display modes by calling [**IDirect3D9::EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>
3.  <span data-ttu-id="09b49-114">Bei Bedarf überprüft die Anwendung die Hardwarebeschleunigung in jedem enumerationsanzeigemodus durch Aufrufen von [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="09b49-114">If required, the application checks for the presence of hardware acceleration in each enumerated display mode by calling [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype), as shown in the following code example.</span></span> <span data-ttu-id="09b49-115">Beachten Sie, dass dies nur eine der möglichen Verwendungsmöglichkeiten für **IDirect3D9:: checkdebug Type** ist. Weitere Informationen finden Sie [unter Bestimmen des Hardware Supports (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="09b49-115">Note that this is only one of the possible uses for **IDirect3D9::CheckDeviceType**; for details, see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    Params.BackBufferFormat = D3DFMT_X1R5G5B5; 

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, 
                      Device.m_DevType, 
                      Params.BackBufferFormat, Params.BackBufferFormat, 
                      FALSE))) 
        return E_FAIL;
    ```

    

4.  <span data-ttu-id="09b49-116">Die Anwendung überprüft die gewünschte Funktionsebene für das Gerät auf diesem Adapter durch Aufrufen der [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) -Methode.</span><span class="sxs-lookup"><span data-stu-id="09b49-116">The application checks for the desired level of functionality for the device on this adapter by calling the [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) method.</span></span> <span data-ttu-id="09b49-117">Die Funktion, die von dieser Methode zurückgegeben wird, ist garantiert für ein Gerät über alle Anzeigemodi hinweg konstant und wird von [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)überprüft.</span><span class="sxs-lookup"><span data-stu-id="09b49-117">The capability returned by this method is guaranteed to be constant for a device across all display modes, verified by [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype).</span></span>
5.  <span data-ttu-id="09b49-118">Geräte können immer auf Oberflächen des Formats eines aufgelisteten Anzeigemodus Renderingmodus Renderingmodus, der vom Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="09b49-118">Devices can always render to surfaces of the format of an enumerated display mode that is supported by the device.</span></span> <span data-ttu-id="09b49-119">Wenn die Anwendung auf eine Oberfläche eines anderen Formats renderert werden muss, kann Sie [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="09b49-119">If the application is required to render to a surface of a different format, it can call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span> <span data-ttu-id="09b49-120">Wenn das Gerät in das Format rendern kann, ist sichergestellt, dass alle von [**IDirect3D9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) zurückgegebenen Funktionen anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="09b49-120">If the device can render to the format, then it is guaranteed that all capabilities returned by [**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps) are applicable.</span></span>
6.  <span data-ttu-id="09b49-121">Schließlich kann die Anwendung ermitteln, ob multisamplinggrad-Techniken, z. b. Vollbild-Antialiasing, mit der [**IDirect3D9:: checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) -Methode für ein Renderformat unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="09b49-121">Lastly, the application can determine if multisampling techniques, such as full-scene antialiasing, are supported for a render format by using the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method.</span></span>

<span data-ttu-id="09b49-122">Nachdem Sie die obigen Schritte ausgeführt haben, sollte die Anwendung über eine Liste der Anzeigemodi verfügen, in der Sie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="09b49-122">After completing the preceding steps, the application should have a list of display modes in which it can operate.</span></span> <span data-ttu-id="09b49-123">Der letzte Schritt besteht darin, zu überprüfen, ob ausreichend Speicherplatz für das Gerät verfügbar ist, um die erforderliche Anzahl von Puffern und Antialiasing zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="09b49-123">The final step is to verify that enough device-accessible memory is available to accommodate the required number of buffers and antialiasing.</span></span> <span data-ttu-id="09b49-124">Dieser Test ist erforderlich, da der Arbeitsspeicher Verbrauch für die Kombination aus Modus und Multisampling ohne Überprüfung nicht vorhergesagt werden kann.</span><span class="sxs-lookup"><span data-stu-id="09b49-124">This test is necessary because the memory consumption for the mode and multisample combination is impossible to predict without verifying it.</span></span> <span data-ttu-id="09b49-125">Außerdem verfügen einige Anzeige Adapter Architekturen möglicherweise nicht über eine konstante Menge an Speicherplatz, auf den Gerät zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="09b49-125">Moreover, some display adapter architectures might not have a constant amount of device-accessible memory.</span></span> <span data-ttu-id="09b49-126">Dies bedeutet, dass eine Anwendung in der Lage sein sollte, out-of-Video-Memory-Fehler zu melden, wenn Sie in den Vollbildmodus wechseln.</span><span class="sxs-lookup"><span data-stu-id="09b49-126">This means that an application should be able to report out-of-video-memory failures when going into full-screen mode.</span></span> <span data-ttu-id="09b49-127">In der Regel sollte eine Anwendung den Vollbildmodus aus der Liste der Modi entfernen, die Sie für einen Benutzer anbietet, oder es sollte versucht werden, weniger Arbeitsspeicher zu belegen, indem die Anzahl der Back Puffer reduziert wird oder eine weniger komplexe multisamplinggrad-Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09b49-127">Typically, an application should remove full-screen mode from the list of modes that it offers to a user, or it should attempt to consume less memory by reducing the number of back buffers or by using a less complex multisampling technique.</span></span>

<span data-ttu-id="09b49-128">Eine Anwendungs Anwendung führt einen ähnlichen Satz von Aufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="09b49-128">A windowed application performs a similar set of tasks.</span></span>

1.  <span data-ttu-id="09b49-129">Er bestimmt das Desktop Rechteck, das durch den Client Bereich des Fensters abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="09b49-129">It determines the desktop rectangle covered by the client area of the window.</span></span>
2.  <span data-ttu-id="09b49-130">Es listet Adapter auf und sucht den Adapter, dessen Monitor den Client Bereich abdeckt.</span><span class="sxs-lookup"><span data-stu-id="09b49-130">It enumerates adapters, looking for the adapter whose monitor covers the client area.</span></span> <span data-ttu-id="09b49-131">Wenn der Client Bereich im Besitz mehrerer Adapter ist, kann die Anwendung jeden Adapter unabhängig voneinander steuern oder einen einzelnen Adapter übertragen und Direct3D Pixel von einem Gerät zu einem anderen in der Präsentation übertragen.</span><span class="sxs-lookup"><span data-stu-id="09b49-131">If the client area is owned by more than one adapter, then the application can choose to drive each adapter independently, or to drive a single adapter and have Direct3D transfer pixels from one device to another at presentation.</span></span> <span data-ttu-id="09b49-132">Die Anwendung kann auch zwei vorangehende Schritte ignorieren und den D3DADAPTER- \_ Standard Adapter verwenden.</span><span class="sxs-lookup"><span data-stu-id="09b49-132">The application can also disregard two preceding steps and use the D3DADAPTER\_DEFAULT adapter.</span></span> <span data-ttu-id="09b49-133">Beachten Sie, dass dies zu einem langsameren Vorgang führen kann, wenn das Fenster auf einem sekundären Monitor platziert wird.</span><span class="sxs-lookup"><span data-stu-id="09b49-133">Note that this might result in slower operation when the window is placed on a secondary monitor.</span></span>
3.  <span data-ttu-id="09b49-134">Die Anwendung muss [**IDirect3D9:: CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) aufgerufen werden, um zu bestimmen, ob das Gerät das Rendering zu einem Hintergrund Puffer des angegebenen Formats im Desktop Modus unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="09b49-134">The application should call [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype) to determine if the device can support rendering to a back buffer of the specified format while in desktop mode.</span></span> <span data-ttu-id="09b49-135">[**IDirect3D9:: getadapterdisplaymode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) kann zum Bestimmen des Desktop Anzeige Formats verwendet werden, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="09b49-135">[**IDirect3D9::GetAdapterDisplayMode**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapterdisplaymode) can be used to determine the desktop display format, as shown in the following code example.</span></span>
    ```
    D3DPRESENT_PARAMETERS Params;
    // Initialize values for D3DPRESENT_PARAMETERS members. 

    // Use the current display mode.
    D3DDISPLAYMODE mode;

    if(FAILED(m_pD3D->GetAdapterDisplayMode(Device.m_uAdapter , &mode)))
        return E_FAIL;

    Params.BackBufferFormat = mode.Format;

    if(FAILED(m_pD3D->CheckDeviceType(Device.m_uAdapter, Device.m_DevType, 
    Params.BackBufferFormat, Params.BackBufferFormat, FALSE)))
        return E_FAIL;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="09b49-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09b49-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b49-137">Direct3D-Geräte</span><span class="sxs-lookup"><span data-stu-id="09b49-137">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
