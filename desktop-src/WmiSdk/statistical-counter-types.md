---
description: Die Leistungs Datenanbieter für die leistungsstarke WMI-Leistung berechnet die statistischen Leistungs Zählers für eine angegebene Anzahl von Rohdaten-Leistungs Beispielen.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Statistische Counter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042587"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="aa221-103">Statistische Counter-Typen</span><span class="sxs-lookup"><span data-stu-id="aa221-103">Statistical Counter Types</span></span>

<span data-ttu-id="aa221-104">Die [Leistungs Datenanbieter](formatted-performance-data-provider.md) für die leistungsstarke WMI-Leistung berechnet die statistischen Leistungs Zählers für eine angegebene Anzahl von Rohdaten-Leistungs Beispielen.</span><span class="sxs-lookup"><span data-stu-id="aa221-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="aa221-105">Die Algorithmen für die Counter-Typen erfordern keine geerbten Zeitstempel-oder Häufigkeits Eigenschaften (z. b. " **Zeitstempel \_ PerfTime** " oder " **Frequency \_ PerfTime**"), die für andere Leistungstypen erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="aa221-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="aa221-106">Stattdessen unterstützen die statistischen Counter-Typen einen **Qualifizierer** , der die Anzahl der zu verwendenden Beispiele identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aa221-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="aa221-107">Ein Beispiel wird gesammelt, wenn die [**Aktualisierungs**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) Methode für das Leistungs Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="aa221-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="aa221-108">Verwenden Sie für Skripts die Methode " [**Swap. Refresh**](swbemrefresher-refresh.md) ".</span><span class="sxs-lookup"><span data-stu-id="aa221-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="aa221-109">Die berechneten Daten enthalten das Ergebnis der Berechnung, die für die **samplewindow** -Anzahl von Stichproben aus der Rohdaten-Eigenschaft ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa221-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="aa221-110">Die Rohdaten für die Berechnung sind frm der im **Counter** -Qualifizierer angegebene Eigenschaftsname.</span><span class="sxs-lookup"><span data-stu-id="aa221-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="aa221-111">Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md) und [zugreifen auf vorinstallierte WMI-Leistungsklassen](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="aa221-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="aa221-112">CounterType-Konstante</span><span class="sxs-lookup"><span data-stu-id="aa221-112">CounterType Constant</span></span>                    | <span data-ttu-id="aa221-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa221-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa221-114">\_kochmittel Wert</span><span class="sxs-lookup"><span data-stu-id="aa221-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="aa221-115">Fasst wiederholte Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse zusammen und dividiert die Summe durch die Anzahl von Beobachtungen.</span><span class="sxs-lookup"><span data-stu-id="aa221-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="aa221-116">Maximaler kochwert \_</span><span class="sxs-lookup"><span data-stu-id="aa221-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="aa221-117">Größter Wert aus einem Satz von Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="aa221-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="aa221-118">Koch \_ Min.</span><span class="sxs-lookup"><span data-stu-id="aa221-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="aa221-119">Der kleinste Wert aus einem Satz von Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="aa221-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="aa221-120">Koch \_ Bereich</span><span class="sxs-lookup"><span data-stu-id="aa221-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="aa221-121">Der Unterschied [zwischen den minimalen](cooker-min.md) und [maximalen](cooker-max.md) Werten für einen Satz von unformatierten Beobachtungen einer Eigenschaft in einer [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="aa221-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="aa221-122">Koch \_ Varianz</span><span class="sxs-lookup"><span data-stu-id="aa221-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="aa221-123">Das Maß der Varianz, das verwendet werden kann, um die Dispersion für eine Reihe von unformatierten Beobachtungen einer Eigenschaft in einer " [**\_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) "-Klasse zu charakterisieren.</span><span class="sxs-lookup"><span data-stu-id="aa221-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="aa221-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa221-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa221-125">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="aa221-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="aa221-126">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="aa221-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="aa221-127">Aktualisieren von WMI-Daten in Skripts</span><span class="sxs-lookup"><span data-stu-id="aa221-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="aa221-128">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="aa221-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="aa221-129">Zugreifen auf Leistungsdaten in C++</span><span class="sxs-lookup"><span data-stu-id="aa221-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
