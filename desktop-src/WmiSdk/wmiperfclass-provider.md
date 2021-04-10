---
description: Ab Windows Vista erstellt dieser Anbieter die WMI-Leistungs Leistungs Ereignis Klassen.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Wmiperfclass-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042362"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="237c9-103">Wmiperfclass-Anbieter</span><span class="sxs-lookup"><span data-stu-id="237c9-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="237c9-104">Ab Windows Vista erstellt dieser Anbieter die WMI- [Leistungs Leistungs Ereignis Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="237c9-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="237c9-105">Daten werden vom [wmiperfinst](wmiperfinst-provider.md) -Anbieter dynamisch für diese WMI-Leistungsklassen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="237c9-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="237c9-106">Der AutoDiscovery/AUTOPURGE-Prozess (ADAP) überträgt Leistungs Objekt Objekte nicht mehr in WMI-Leistungsklassen im WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="237c9-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="237c9-107">Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="237c9-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="237c9-108">Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="237c9-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="237c9-109">Es wird zwar nicht empfohlen, neue Leistungs Objekte zu entwickeln, indem Sie einen leistungsfähigen WMI-Anbieter erstellen und vom [*ADAP-Reverse-Adapter*](gloss-r.md) -Prozess abhängig sind, um die Daten in die Leistungs Bibliotheken zu übertragen. die Ausnahme bildet die Entwicklung eines Windows-Treibermodell Treibers, der Leistungsdaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="237c9-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="237c9-110">Während der reverseadapterprozess weiterhin aus Gründen der Abwärtskompatibilität funktioniert, empfiehlt es sich, die [Leistungsindikatoren Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="237c9-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="237c9-111">Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname dieses Anbieters lautet "wmiperfclass".</span><span class="sxs-lookup"><span data-stu-id="237c9-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="237c9-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="237c9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="237c9-113">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="237c9-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="237c9-114">Leistungs Bibliotheken und WMI</span><span class="sxs-lookup"><span data-stu-id="237c9-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="237c9-115">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="237c9-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
