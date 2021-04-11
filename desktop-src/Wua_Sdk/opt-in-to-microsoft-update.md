---
description: Sie können einen Computer in für den Microsoft Update-Dienst und dann diesen Dienst bei automatische Updates registrieren.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128272"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="d3bcb-103">Opt-In Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="d3bcb-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="d3bcb-104">Sie können einen Computer in für den Microsoft Update-Dienst und dann diesen Dienst bei automatische Updates registrieren.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="d3bcb-105">Das Skript Beispiel in diesem Thema zeigt Ihnen, wie Sie Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei automatische Updates zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="d3bcb-106">Alternativ kann der Benutzer Microsoft Update besuchen, um den Dienst zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="d3bcb-107">Vergewissern Sie sich vor dem Ausführen dieses Beispiels, dass die auf dem Computer installierte Version von WUA Version 7.0.6000 oder eine höhere Version ist.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="d3bcb-108">Weitere Informationen zum Ermitteln der installierten Version von WUA finden Sie unter [bestimmen der aktuellen WUA](determining-the-current-version-of-wua.md)-Version.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="d3bcb-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3bcb-109">Example</span></span>

<span data-ttu-id="d3bcb-110">Im folgenden Skript Beispiel wird gezeigt, wie Sie den Windows Update-Agent (WUA) verwenden, um den Microsoft Update-Dienst bei automatische Updates zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="d3bcb-111">Das Beispiel ermöglicht die verzögerte oder Offline Verarbeitung bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3bcb-112">Dieses Skript soll die Verwendung der Windows Update-Agent-APIs veranschaulichen und bietet ein Beispiel dafür, wie Entwickler diese APIs zum Lösen von Problemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="d3bcb-113">Dieses Skript ist nicht als Produktionscode gedacht, und das Skript selbst wird nicht von Microsoft unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="d3bcb-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="d3bcb-114">In früheren Versionen von WUA (mindestens eine WUA-Version von 7.0.6000) können Sie den Opt-in-Prozess vereinfachen, indem Sie eine Registrierungs Einstellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="d3bcb-115">Nachdem der Registrierungsschlüssel und die Werte konfiguriert wurden, wird der Microsoft Update Opt-in-Vorgang durchgeführt, wenn WUA das nächste Mal eine Suche durchführt.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="d3bcb-116">Der Opt-in-Prozess kann durch automatische Updates oder durch einen API-Aufrufer ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="d3bcb-117">Der vollständige Pfad des Registrierungsschlüssels und der Werte, die für den Opt-in-Prozess festgelegt werden sollen, lauten z. b. wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d3bcb-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="d3bcb-118">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **Pdingserviceregistration** \\ **7971l918-a847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="d3bcb-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="d3bcb-119">**Clientapplicationid** = meine APP</span><span class="sxs-lookup"><span data-stu-id="d3bcb-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="d3bcb-120">**Registerwithau** = 1</span><span class="sxs-lookup"><span data-stu-id="d3bcb-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="d3bcb-121">Der Registrierungsschlüssel wird nur einmal beachtet, wenn WUA von einer Version, die älter ist als Version 7.0.6000, auf Version 7.0.6000 oder eine höhere Version aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="d3bcb-122">Beim Überschreiben vorhandener Registrierungs Werte wird ein Ermessen empfohlen, da durch das Überschreiben der Werte das Ergebnis einer früheren Dienst Registrierungs Anforderung geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="d3bcb-123">Zum Erstellen dieses Registrierungsschlüssels sind administrative Anmelde Informationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="d3bcb-124">Für Windows Vista muss der Aufrufer den Registrierungsschlüssel in einem erweiterten Prozess erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3bcb-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



