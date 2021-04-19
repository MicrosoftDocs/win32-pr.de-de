---
description: Der wmiperfclass-Anbieter und der WMIPerfInst-Anbieter stellen dynamische Leistungsdaten für die WMI-Leistungs Leistungs Leistungsgruppen bereit.
ms.assetid: 8bf6d218-9a31-4efd-a809-222aca364138
ms.tgt_platform: multiple
title: Leistungs Bibliotheken und WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dedc9b98f492b3ab57e22cd1507f9e3651980a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359923"
---
# <a name="performance-libraries-and-wmi"></a><span data-ttu-id="7230c-103">Leistungs Bibliotheken und WMI</span><span class="sxs-lookup"><span data-stu-id="7230c-103">Performance Libraries and WMI</span></span>

<span data-ttu-id="7230c-104">Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) und der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellen dynamische Leistungsdaten für die WMI- [Leistungs Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Gruppen bereit.</span><span class="sxs-lookup"><span data-stu-id="7230c-104">The [WMIPerfClass Provider](wmiperfclass-provider.md) and the [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provide performance counter data for the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span>

## <a name="wmiperfclass-and-wmiperfinst-providers"></a><span data-ttu-id="7230c-105">Wmiperfclass-und WMIPerfInst-Anbieter</span><span class="sxs-lookup"><span data-stu-id="7230c-105">WMIPerfClass and WMIPerfInst Providers</span></span>

<span data-ttu-id="7230c-106">Der [wmiperfclass-Anbieter](wmiperfclass-provider.md) erstellt bei der Systeminitialisierung WMI- [Leistungs Leistungs Zählers](/windows/desktop/CIMWin32Prov/performance-counter-classes) .</span><span class="sxs-lookup"><span data-stu-id="7230c-106">[WMIPerfClass Provider](wmiperfclass-provider.md) creates WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) at system initialization.</span></span> <span data-ttu-id="7230c-107">Der [WMIPerfInst-Anbieter](wmiperfinst-provider.md) stellt dynamisch Leistungsdaten für diese Klassen bereit.</span><span class="sxs-lookup"><span data-stu-id="7230c-107">The [WMIPerfInst Provider](wmiperfinst-provider.md) dynamically provides performance counter data for these classes.</span></span> <span data-ttu-id="7230c-108">Der Anbieter des wmiperfclass-Anbieters liefert Klassen für [Leistungsindikatoren](/windows/desktop/PerfCtrs/performance-counters-portal)der Versionen 1 und Version 2.</span><span class="sxs-lookup"><span data-stu-id="7230c-108">The WMIPerfClass Provider provider supplies classes for both version 1 and version 2 [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="7230c-109">Leistungsindikatoren der Version 1 finden Sie in der Registrierung unter **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.</span><span class="sxs-lookup"><span data-stu-id="7230c-109">Version 1 counters are found in the registry under **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span> <span data-ttu-id="7230c-110">Dienste, die Leistungsdaten bereitstellen, verfügen über einen **Leistungs** Unterschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7230c-110">Services that provide performance data have a **Performance** subkey.</span></span> <span data-ttu-id="7230c-111">WMI-Leistungsklassen, die aus den Leistungsindikatoren der Version 1 erstellt wurden, haben nicht als Teil Ihres Namens "Indikatoren".</span><span class="sxs-lookup"><span data-stu-id="7230c-111">WMI performance classes created from version 1 counters do not have "Counters" as part of their name.</span></span>

<span data-ttu-id="7230c-112">Die **GUID** s, die einen Leistungs Anbieter für die Version 2 identifizieren, finden Sie in der Registrierung unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Perflib \\ \_ V2Providers**.</span><span class="sxs-lookup"><span data-stu-id="7230c-112">The **GUID** s identifying a version 2 performance counter provider are found in the registry under **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib\\\_V2Providers**.</span></span>

<span data-ttu-id="7230c-113">Wmiperfclass ist als normaler WMI-Klassen Anbieter registriert.</span><span class="sxs-lookup"><span data-stu-id="7230c-113">WMIPerfClass is registered as a normal WMI class provider.</span></span> <span data-ttu-id="7230c-114">Wmiperfinst ist ein WMI-Instanzanbieter, der Daten aus dem Leistungsdaten-Hilfsprogramm (PDH) für die Leistungsindikatoren Version 1 und Version 2 bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="7230c-114">WMIPerfInst is a WMI instance provider that supplies data from Performance Data Helper (PDH) for both version 1 and version 2 counters.</span></span> <span data-ttu-id="7230c-115">Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)verarbeiten von Counter-Daten.</span><span class="sxs-lookup"><span data-stu-id="7230c-115">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7230c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7230c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7230c-117">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="7230c-117">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="7230c-118">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="7230c-118">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
