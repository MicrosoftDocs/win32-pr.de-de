---
title: Beispiel Dienstanbieter
description: Beispiel Dienstanbieter
ms.assetid: bbdeddb5-4ddf-4a61-828c-a9ba7af307ea
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Windows Media Device Manager, Dienstanbieter Beispiel
- Beispiel für Device Manager, Dienstanbieter
- Dienstanbieter, Beispiele
- Beispiele, Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8b7e781785944ac1ca390a62303f1149d710d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337369"
---
# <a name="sample-service-provider"></a><span data-ttu-id="87141-109">Beispiel Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="87141-109">Sample Service Provider</span></span>

<span data-ttu-id="87141-110">Das Windows Media Device Manager SDK enthält einen Beispiel Dienstanbieter, den Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="87141-110">The Windows Media Device Manager SDK includes a sample service provider for you to use.</span></span> <span data-ttu-id="87141-111">Dieser Dienstanbieter enthält eine-Klasse, die jede Festplatte auf dem Computer so meldet, als ob es sich um ein angefügtes Gerät handelt.</span><span class="sxs-lookup"><span data-stu-id="87141-111">This service provider includes a class that reports each hard drive on the computer as if it were an attached device.</span></span> <span data-ttu-id="87141-112">Die einzige Anwendung, die diesen Dienstanbieter verwendet, ist die Beispielanwendung. Windows-Explorer wird die von diesem Dienstanbieter gemeldeten Geräte nicht sehen.</span><span class="sxs-lookup"><span data-stu-id="87141-112">The only application that will use this service provider is the sample application; Windows Explorer will not see the "devices" reported by this service provider.</span></span> <span data-ttu-id="87141-113">Das Dienstanbieter Beispiel ist ein COM-Objekt, das auf ATL basiert.</span><span class="sxs-lookup"><span data-stu-id="87141-113">The service provider sample is a COM object built on ATL.</span></span> <span data-ttu-id="87141-114">In den folgenden Schritten wird erläutert, wie der Beispiel Dienstanbieter verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="87141-114">The following steps explain how to use the sample service provider:</span></span>

> [!Note]  
> <span data-ttu-id="87141-115">Der Beispiel Dienstanbieter implementiert sehr wenige Features und sollte daher nicht zum Testen von Windows Media Device Manager-Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87141-115">The sample service provider implements very few features, and so it should not be used for testing Windows Media Device Manager applications.</span></span> <span data-ttu-id="87141-116">Um eine Anwendung zu testen, verwenden Sie einen vollständig implementierten Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="87141-116">To test an application, use a fully-implemented service provider.</span></span>

 

-   <span data-ttu-id="87141-117">Das Beispiel wurde mit einem Codierungsfehler ausgeliefert, der dazu führt, dass der Dienstanbieter nicht funktioniert.</span><span class="sxs-lookup"><span data-stu-id="87141-117">The sample was shipped with a coding error that will cause the service provider to malfunction.</span></span> <span data-ttu-id="87141-118">Um diesen Fehler zu beheben, öffnen Sie die Datei "mdspenumstorage. cpp", die im Ordner < *SDK-Installationspfad*  > \\ WMFSDK95 \\ WMDM \\ mdsp \\ mshdsp installiert ist, gehen Sie zu Zeile 185, und ändern Sie die folgende Zeile:</span><span class="sxs-lookup"><span data-stu-id="87141-118">To correct this error, open the MDSPEnumStorage.cpp file installed in the folder < *SDK installation path* >\\WMFSDK95\\WMDM\\mdsp\\mshdsp, go to line 185, and change the following line:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, dwLen);`

<span data-ttu-id="87141-119">Folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="87141-119">To this:</span></span>

`wcsncpy(pStg->m_wcsName, m_wcsPath, ARRAYSIZE(pStg->m_wcsName));`

1.  <span data-ttu-id="87141-120">Kompilieren Sie die MsHDSP.dll Datei.</span><span class="sxs-lookup"><span data-stu-id="87141-120">Compile the MsHDSP.dll file.</span></span> <span data-ttu-id="87141-121">Hierfür können Sie entweder NMAKE oder Visual Studio verwenden.</span><span class="sxs-lookup"><span data-stu-id="87141-121">You can do this using either NMAKE or Visual Studio.</span></span> <span data-ttu-id="87141-122">Weitere Informationen zum Kompilieren der Anwendung finden Sie unter [Kompilieren des Beispiel Dienstanbieters mithilfe von NMAKE](compiling-the-sample-service-provider-using-nmake.md) oder [Kompilieren des Beispiel Dienstanbieters mithilfe von Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) .</span><span class="sxs-lookup"><span data-stu-id="87141-122">See [Compiling the Sample Service Provider Using NMAKE](compiling-the-sample-service-provider-using-nmake.md) or [Compiling the Sample Service Provider Using Visual Studio](compiling-the-sample-service-provider-using-visual-studio.md) to learn how to compile the application.</span></span>
2.  <span data-ttu-id="87141-123">Registrieren Sie MsHDSP.dll mithilfe von regsvr32.</span><span class="sxs-lookup"><span data-stu-id="87141-123">Register MsHDSP.dll using regsvr32.</span></span> <span data-ttu-id="87141-124">Die folgende Zeile, die in ein Eingabe Aufforderungs Fenster in demselben Ordner wie MsHDSP.dll eingegeben wird, registriert den Beispiel Dienstanbieter:</span><span class="sxs-lookup"><span data-stu-id="87141-124">The following line, typed into a command-prompt window in the same folder as MsHDSP.dll, will register the sample service provider:</span></span>

    ```C++
    regsvr32 mshdsp.dll
    ```

    

    <span data-ttu-id="87141-125">Geben Sie an der Eingabeaufforderung die folgende Zeile ein, um die Identitätswechsel für ein Gerät zu verhindern:</span><span class="sxs-lookup"><span data-stu-id="87141-125">To stop impersonating a device, enter the following line at the command prompt:</span></span>

    ```C++
    regsvr32 /u mshdsp.dll
    ```

    

3.  <span data-ttu-id="87141-126">Die Wechsel Datenträger, die von dieser DLL angenommen werden, können nur von der mit diesem SDK gelieferten Beispielanwendung eingesehen werden.</span><span class="sxs-lookup"><span data-stu-id="87141-126">The removable devices impersonated by this DLL can only be seen by the sample application shipped with this SDK.</span></span> <span data-ttu-id="87141-127">Kompilieren Sie die Beispielanwendung mit einer der Methoden, die in Beispiel für eine [Desktop Anwendung](sample-desktop-application.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="87141-127">Compile the sample application using one of the methods described in [Sample Desktop Application](sample-desktop-application.md).</span></span>
4.  <span data-ttu-id="87141-128">Um den Dienstanbieter mit Visual Studio zu debuggen, öffnen Sie den Dienstanbieter in Visual Studio, und wählen Sie im Menü **Debuggen** die Option **starten** .</span><span class="sxs-lookup"><span data-stu-id="87141-128">To debug the service provider with Visual Studio, open the service provider in Visual Studio and select **Start** on the **Debug** menu.</span></span> <span data-ttu-id="87141-129">Navigieren Sie im Popup Dialogfeld zur Beispielanwendung, die Sie im vorherigen Schritt erstellt haben, und klicken Sie auf **OK**, damit der Dienstanbieter im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87141-129">In the popup dialog box, browse to the sample application you built in the preceding step, and click **OK**, and the service provider will begin running in debug mode.</span></span>

    <span data-ttu-id="87141-130">Wenn Sie den Dienstanbieter ohne Debuggen in Visual Studio ausführen möchten, registrieren Sie einfach die msdhsp.dll, und führen Sie die im Lieferumfang des SDK enthaltene Beispiel-Desktop Anwendung aus</span><span class="sxs-lookup"><span data-stu-id="87141-130">To run the service provider without debugging in Visual Studio, simply register the msdhsp.dll and run the sample desktop application that ships with the SDK.</span></span> <span data-ttu-id="87141-131">Die Beispiel-Desktop Anwendung führt den Beispiel Dienstanbieter automatisch aus.</span><span class="sxs-lookup"><span data-stu-id="87141-131">The sample desktop application runs the sample service provider automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87141-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87141-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87141-133">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="87141-133">**Samples**</span></span>](samples.md)
</dt> </dl>

 

 




