---
description: Ab Windows Vista liefert der WMIPerfInst-Anbieter Rohdaten und formatierte Leistungsdaten von Leistungsdaten dynamisch in WMI-Leistungs Leistungsdaten-Klassen, die von Win32 \_ perf abgeleitet werden.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: WMIPerfInst-Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343431"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="00b8d-103">WMIPerfInst-Anbieter</span><span class="sxs-lookup"><span data-stu-id="00b8d-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="00b8d-104">Ab Windows Vista liefert der WMIPerfInst-Anbieter Rohdaten und formatierte Leistungsdaten von Leistungsdaten dynamisch in WMI- [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen, die von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf)abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="00b8d-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="00b8d-105">Dieser Anbieter ersetzt das [formatierte Leistungs Datenanbieter](formatted-performance-data-provider.md), das auch als "gekochte Leistungs Anbieter" bezeichnet wird, und den [Leistungsindikatorenanbieter](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="00b8d-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="00b8d-106">Der WMIPerfInst-Anbieter liefert Daten für die WMI-Klassen, die vom [wmiperfclass](wmiperfclass-provider.md) -Anbieter bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="00b8d-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="00b8d-107">Bei diesem Anbieter handelt es sich um eine Brücke zwischen den PDH-Instanzen (Performance Data Helper) und den vom wmiperfclass-Anbieter bereitgestellten WMI-Leistungsklassen.</span><span class="sxs-lookup"><span data-stu-id="00b8d-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="00b8d-108">Wenn wmiperfinst eine Abfrage für Daten empfängt, lädt es die-Klasse und verwendet die Klassen-und Eigenschafts [Qualifizierer](qualifiers-specific-to-wmi-performance-classes.md) , um die PDH-Instanzen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="00b8d-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="00b8d-109">Weitere Informationen finden Sie unter [Verwenden der PDH-Funktionen zum](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data)verarbeiten von Counter-Daten.</span><span class="sxs-lookup"><span data-stu-id="00b8d-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="00b8d-110">Es wird nicht empfohlen, neue Leistungs Objekte zu entwickeln, indem Sie einen leistungsfähigen WMI-Anbieter erstellen und vom [*ADAP-Reverse-Adapter*](gloss-r.md) -Prozess abhängig sind, um die Daten in die Leistungs Bibliotheken zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="00b8d-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="00b8d-111">Die Ausnahme ist, wenn Sie einen Windows-Treibermodell Treiber entwickeln und Leistungsdaten bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="00b8d-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="00b8d-112">Während der reverseadapterprozess weiterhin aus Gründen der Abwärtskompatibilität funktioniert, empfiehlt es sich, die [Leistungsindikatoren Version 6,0](/windows/desktop/PerfCtrs/performance-counters-portal)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="00b8d-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="00b8d-113">Der [**\_ \_ Win32Provider**](--win32provider.md) -Instanzname dieses Anbieters lautet "wmiperfinst".</span><span class="sxs-lookup"><span data-stu-id="00b8d-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b8d-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00b8d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b8d-115">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="00b8d-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="00b8d-116">Leistungs Bibliotheken und WMI</span><span class="sxs-lookup"><span data-stu-id="00b8d-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="00b8d-117">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="00b8d-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
