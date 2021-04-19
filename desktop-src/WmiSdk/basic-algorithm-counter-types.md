---
description: Stellt Unterschiede zwischen Beispielen im Zeitverlauf dar und verwendet häufig einen Basiswert für die Berechnung.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Grundlegende algorithmuscounter-Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364156"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="b090b-103">Grundlegende algorithmuscounter-Typen</span><span class="sxs-lookup"><span data-stu-id="b090b-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="b090b-104">Grundlegende algorithmuszähtertypen stellen im allgemeinen Unterschiede zwischen den Beispielen im Zeitverlauf dar und verwenden häufig einen Basiswert für die Berechnung.</span><span class="sxs-lookup"><span data-stu-id="b090b-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="b090b-105">Die Eigenschaft " **komponfreespace** " der Klasse " [**Win32 \_ perfformatteddata \_ perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) " gibt z. b. das Verhältnis des freien Speicherplatzes, der auf der physischen Datenträger Einheit verfügbar ist, zum gesamten nutzbaren Speicherplatz des ausgewählten physischen Laufwerks an.</span><span class="sxs-lookup"><span data-stu-id="b090b-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="b090b-106">Diese Klasse enthält auch den Basiswert, " **prozentufreespace \_ Base**".</span><span class="sxs-lookup"><span data-stu-id="b090b-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="b090b-107">Der prozentuale Anteil des freien Speicherplatzes wird durch Aufteilen von **prozentualer FreeSpace** durch die **\_ Basis** von Prozent und multipliziert mit 100% erreicht.</span><span class="sxs-lookup"><span data-stu-id="b090b-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="b090b-108">Die grundlegenden Algorithmen in der folgenden Tabelle werden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b090b-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="b090b-109">CounterType-Konstante</span><span class="sxs-lookup"><span data-stu-id="b090b-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="b090b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b090b-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b090b-111">Leistung [ \_ \_](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Unformatierte Bruch Dezimalzahl 537003008</span><span class="sxs-lookup"><span data-stu-id="b090b-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="b090b-112">Das Verhältnis einer Teilmenge zu dem Satz als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="b090b-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="b090b-113">Dieser zähtertyp zeigt nur den aktuellen Prozentsatz an, nicht den Durchschnitt im Zeitverlauf.</span><span class="sxs-lookup"><span data-stu-id="b090b-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="b090b-114">Leistung [ \_ Stichproben \_ Bruch](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Dezimaltrennzeichen 549585920</span><span class="sxs-lookup"><span data-stu-id="b090b-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="b090b-115">Das durchschnittliche Verhältnis von Treffern zu allen Vorgängen während der letzten beiden Stichproben Intervalle.</span><span class="sxs-lookup"><span data-stu-id="b090b-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="b090b-116">Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Leistungs \_ Proben- \_ Basis zähtertyp.</span><span class="sxs-lookup"><span data-stu-id="b090b-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="b090b-117">Leistung [ \_ Gegen \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimaltrennzeichen 4195328</span><span class="sxs-lookup"><span data-stu-id="b090b-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="b090b-118">Dieser Indikatortyp zeigt die Änderung des gemessenen Attributs zwischen den beiden letzten Messintervallen an.</span><span class="sxs-lookup"><span data-stu-id="b090b-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="b090b-119">Leistung [ \_ \_Großer \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimaltrennzeichen 4195584</span><span class="sxs-lookup"><span data-stu-id="b090b-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="b090b-120">Identisch mit dem perf \_ -Leistungs Leistungs-gegen \_ Delta, aber eine 64-Bit-Darstellung für größere Werte.</span><span class="sxs-lookup"><span data-stu-id="b090b-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="b090b-121">Leistung [ \_ Verstrichene \_ Zeit](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span><span class="sxs-lookup"><span data-stu-id="b090b-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="b090b-122">Gesamtzeit zwischen dem Start des Prozesses und dem Zeitpunkt, zu dem dieser Wert berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b090b-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="b090b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b090b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b090b-124">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="b090b-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

