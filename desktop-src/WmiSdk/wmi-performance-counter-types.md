---
description: Der Leistungs indikatorentyp legt eine Formel fest, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist. Dabei handelt es sich um die gleichen bei der Windows-Leistungsüberwachung verwendeten Leistungstypen.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: WMI-Leistungsdaten Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131148"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="d2b24-104">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="d2b24-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="d2b24-105">Der Leistungs [indikatorentyp](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) legt eine Formel fest, die zum Abrufen berechneter Leistungsindikatoren erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d2b24-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="d2b24-106">Dabei handelt es sich um die gleichen bei der Windows- [Leistungsüberwachung verwendeten Leistungs](/windows/desktop/PerfCtrs/performance-counters-portal)Typen.</span><span class="sxs-lookup"><span data-stu-id="d2b24-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="d2b24-107">In WMI-Leistungsklassen stammen die Rohdaten für die Counter Type-Formel aus einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse, und das berechnete Ergebnis ist in der gleichnamigen Eigenschaft einer entsprechenden [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="d2b24-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="d2b24-108">Indikator Typen werden als **CounterType** -Qualifizierer für Eigenschaften in [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klassen und als **cookingtype** -Qualifizierer für Eigenschaften in [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) -Klassen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2b24-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="d2b24-109">Beispielsweise ist die **avgdiskbytesperread** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) -Klasse die Rohdaten Quelle für die **avgdiskbytesperread** -Eigenschaft in der Klasse [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), die die gleichen Daten wie im System Monitor enthält.</span><span class="sxs-lookup"><span data-stu-id="d2b24-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="d2b24-110">In der folgenden Liste werden die zähtertyp Beschreibungen nach Funktionstyp organisiert:</span><span class="sxs-lookup"><span data-stu-id="d2b24-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="d2b24-111">Basis-Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="d2b24-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="d2b24-112">Grundlegende algorithmuscounter-Typen</span><span class="sxs-lookup"><span data-stu-id="d2b24-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="d2b24-113">Gegen Typen von Algorithmus-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="d2b24-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="d2b24-114">Nicht-Berechnungs-Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="d2b24-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="d2b24-115">Zähler Typen für Genauigkeits Geber Algorithmen</span><span class="sxs-lookup"><span data-stu-id="d2b24-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="d2b24-116">Algorithmustypen der Warteschlangen Länge</span><span class="sxs-lookup"><span data-stu-id="d2b24-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="d2b24-117">Statistische Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="d2b24-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="d2b24-118">Zähler Typen für Timer-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="d2b24-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
