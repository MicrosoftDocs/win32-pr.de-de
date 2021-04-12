---
description: Algorithmustypen für die Warteschlangen Länge erhöhen die Anzahl der Elemente in einer Warteschlange in den einzelnen Stichproben Intervallen, wie von der entsprechenden Frequency-Eigenschaft angegeben&\# 8212; "Frequenz \_ PerfTime" usw.
ms.assetid: 514b1a79-ed9d-4ec6-a6ea-b3490291ce18
ms.tgt_platform: multiple
title: Algorithmustypen der Warteschlangen Länge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06665c2fb8fca014c7d722f0ea22cf7e86833ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215344"
---
# <a name="queue-length-algorithm-counter-types"></a><span data-ttu-id="47c30-103">Algorithmustypen der Warteschlangen Länge</span><span class="sxs-lookup"><span data-stu-id="47c30-103">Queue-length Algorithm Counter Types</span></span>

<span data-ttu-id="47c30-104">Algorithmustypen für die Warteschlangen Länge erhöhen die Anzahl der Elemente in einer Warteschlange in den einzelnen Stichproben Intervallen, wie in der entsprechenden Häufigkeit für Häufigkeits Häufigkeit \_ usw. angegeben.</span><span class="sxs-lookup"><span data-stu-id="47c30-104">Queue-length algorithm counter types increment the number of items in a queue at each sample interval as specified by the appropriate frequency property Frequency\_PerfTime, and so on.</span></span> <span data-ttu-id="47c30-105">Das verarbeitete Ergebnis dividiert durch die Anzahl von Stichproben, um die durchschnittliche Warteschlangen Länge zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="47c30-105">The cooked result divides by the number of samples to produce the average queue length.</span></span>

<span data-ttu-id="47c30-106">Ein Beispiel hierfür ist die **avgdiskqueuelength** -Eigenschaft im [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) , die den Leistungsindikator \_ \_ 100ns-Typ- \_ \_ Indikators vom Typ "Queue" verwendet.</span><span class="sxs-lookup"><span data-stu-id="47c30-106">An example is the **AvgDiskQueueLength** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) that uses the PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE counter type.</span></span>



| <span data-ttu-id="47c30-107">CounterType-Konstante</span><span class="sxs-lookup"><span data-stu-id="47c30-107">CounterType Constant</span></span>                                                                                                 | <span data-ttu-id="47c30-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47c30-108">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47c30-109">Leistung [ \_ Counter \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span><span class="sxs-lookup"><span data-stu-id="47c30-109">[PERF\_COUNTER\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523008</span></span><br/>            | <span data-ttu-id="47c30-110">Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf.</span><span class="sxs-lookup"><span data-stu-id="47c30-110">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="47c30-111">Er zeigt den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an.</span><span class="sxs-lookup"><span data-stu-id="47c30-111">It shows the difference between the queue lengths observed during the last two sample intervals divided by the duration of the interval.</span></span>                       |
| <span data-ttu-id="47c30-112">Leistung [ \_ \_Large \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span><span class="sxs-lookup"><span data-stu-id="47c30-112">[PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4523264</span></span><br/>     | <span data-ttu-id="47c30-113">Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf.</span><span class="sxs-lookup"><span data-stu-id="47c30-113">Average length of a queue to a resource over time.</span></span> <span data-ttu-id="47c30-114">Zähler dieses Typs zeigen den Quotienten aus der Differenz der während der letzten zwei Messintervalle beobachteten Warteschlangenlängen und der Dauer des Intervalls an.</span><span class="sxs-lookup"><span data-stu-id="47c30-114">Counters of this type display the difference between the queue lengths observed during the last two sample intervals, divided by the duration of the interval.</span></span> |
| <span data-ttu-id="47c30-115">Leistung [ \_ Counter \_ 100 NS \_ queuelen \_ Type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span><span class="sxs-lookup"><span data-stu-id="47c30-115">[PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 5571840</span></span><br/>     | <span data-ttu-id="47c30-116">Die durchschnittliche Länge einer Warteschlange für eine Ressource im Zeitverlauf in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="47c30-116">Average length of a queue to a resource over time in 100 nanosecond units.</span></span>                                                                                                                                        |
| <span data-ttu-id="47c30-117">Leistung [ \_ Counter- \_ obj- \_ Zeit \_ queuelen- \_ Typ](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span><span class="sxs-lookup"><span data-stu-id="47c30-117">[PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 6620416</span></span><br/> | <span data-ttu-id="47c30-118">Uhrzeit, zu der ein Objekt in einer Warteschlange ist.</span><span class="sxs-lookup"><span data-stu-id="47c30-118">Time an object is in a queue.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="47c30-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47c30-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47c30-120">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="47c30-120">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

