---
description: Anbieter, es sei denn, Sie sind entkoppelte Anbieter, die in einer Anwendung ausgeführt werden, werden in einen Wmiprvse.exe Prozess geladen, nicht durch Svchost.exe mit einem Winmgmt.exe Prozess. Weitere Informationen finden Sie unter Anbieter Hosting und-Sicherheit.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Debuganbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959378"
---
# <a name="debugging-providers"></a><span data-ttu-id="0718b-104">Debuganbieter</span><span class="sxs-lookup"><span data-stu-id="0718b-104">Debugging Providers</span></span>

<span data-ttu-id="0718b-105">Anbieter, es sei denn, Sie sind [*entkoppelte Anbieter*](gloss-d.md) , die in einer Anwendung ausgeführt werden, werden in einen Wmiprvse.exe Prozess geladen, nicht durch Svchost.exe mit einem Winmgmt.exe Prozess.</span><span class="sxs-lookup"><span data-stu-id="0718b-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="0718b-106">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="0718b-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="0718b-107">Beim Anhalten an einem Haltepunkt friert der Visual Studio-Debugger den gesamten Anbieter Host Prozess, der in der Regel der freigegebene Host Wmiprvse.exe ist.</span><span class="sxs-lookup"><span data-stu-id="0718b-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="0718b-108">Dies verhindert den Betrieb anderer in diesem Prozess gehosteter Komponenten, einschließlich der WMI-Server-Explorer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="0718b-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="0718b-109">Client Anwendungen, die den Anbieter aufzurufen, werden ebenfalls blockiert.</span><span class="sxs-lookup"><span data-stu-id="0718b-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="0718b-110">Die Probleme, die sich auf Windows 2000 und früher ergeben, sind schlimmer, da der Anbieter in den WMI-Dienst Prozess (Winmgmt.exe) geladen wird.</span><span class="sxs-lookup"><span data-stu-id="0718b-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="0718b-111">Wenn Sie WMI-Server-Explorer in einer anderen-Instanz ausführen, wird die Visual Studio-IDE nicht fixiert, und Sie können den Breakpoint freigeben.</span><span class="sxs-lookup"><span data-stu-id="0718b-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="0718b-112">Es wird empfohlen, dass Sie den Anbieter während der Entwicklungsphase in einem separaten Hostingprozess ausführen, sodass der Prozess, der an einem Haltepunkt angehalten wird, nur den Prozess, der den Anbieter gehostet, abstürzt.</span><span class="sxs-lookup"><span data-stu-id="0718b-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="0718b-113">Die anderen Funktionen in WMI sind auch für WMI-Server-Explorer und alle anderen WMI-basierten Anwendungen oder Skripts zugänglich.</span><span class="sxs-lookup"><span data-stu-id="0718b-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="0718b-114">Wenn der Anbieter abstürzt, wirkt sich dies auch nicht auf den Betrieb anderer Anbieter aus, die in denselben Host Prozess geladen werden.</span><span class="sxs-lookup"><span data-stu-id="0718b-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="0718b-115">Damit der Anbieter in einem eigenen Host Prozess geladen wird, ändern Sie die Anbieter Registrierung so, dass die [**\_ \_ Win32Provider. hostingmodel**](--win32provider.md) -Eigenschaft auf festgelegt `NetworkServiceHost:[MyProvider]` wird, wobei MyProvider eine beliebige Zeichenfolge sein kann, die Ihren Anbieter eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0718b-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="0718b-116">Verwenden Sie z. b. den Wert **\_ \_ Win32Provider. CLSID** .</span><span class="sxs-lookup"><span data-stu-id="0718b-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="0718b-117">Wenn Ihr Anbieter bereit für das Versenden ist, geben Sie **\_ \_ Win32Provider. hostingmodel** an den beabsichtigten Wert zurück, z. b. **networkservicehost**.</span><span class="sxs-lookup"><span data-stu-id="0718b-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="0718b-118">Wenn Sie das Laden von Anbietern nicht debuggen, können Sie die [**Load-Methode der \_ Klasse der MSFT-Anbieter**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) aufzurufen, um das Laden des Anbieters zu erzwingen, dann an den Wmiprvse.exe Prozess anzufügen, der die dll geladen hat, und nach Bedarf Debuggen.</span><span class="sxs-lookup"><span data-stu-id="0718b-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0718b-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0718b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0718b-120">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="0718b-120">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="0718b-121">WMI-Fehler Behebungs Klassen</span><span class="sxs-lookup"><span data-stu-id="0718b-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
