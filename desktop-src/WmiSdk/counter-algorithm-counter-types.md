---
description: Gegen Typen von Counter-Algorithmus-Algorithmen können Raten oder Durchschnittswerte für ein Beispiel oder über einen Zeitraum für einen bestimmten Vorgang berechnen.
ms.assetid: 4423e35e-2a93-4f68-8494-89df05268cc9
ms.tgt_platform: multiple
title: Gegen Typen von Algorithmus-Algorithmus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bd55a2a9cc9cc9193a86ffe740ebfa856c0ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346748"
---
# <a name="counter-algorithm-counter-types"></a><span data-ttu-id="42f50-103">Gegen Typen von Algorithmus-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="42f50-103">Counter Algorithm Counter Types</span></span>

<span data-ttu-id="42f50-104">Gegen Typen von Counter-Algorithmus-Algorithmen können Raten oder Durchschnittswerte für ein Beispiel oder über einen Zeitraum für einen bestimmten Vorgang berechnen.</span><span class="sxs-lookup"><span data-stu-id="42f50-104">Counter algorithm counter types may calculate rates or averages bytes for a sample or over a time period for a particular operation.</span></span>

<span data-ttu-id="42f50-105">Die **avgdiskbytespertransfer** -Eigenschaft in der [**Win32 \_ perfrawdata \_ perfdisk \_ PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) -Klasse verwendet den durchschnittlichen perf- \_ \_ Massen CounterType.</span><span class="sxs-lookup"><span data-stu-id="42f50-105">The **AvgDiskBytesPerTransfer** property in the [**Win32\_PerfRawData\_PerfDisk\_PhysicalDisk**](/previous-versions//aa394308(v=vs.85)) class uses the PERF\_AVERAGE\_BULK countertype.</span></span> <span data-ttu-id="42f50-106">In diesem Fall ist die Übertragung der Vorgang, und die kumulierte Anzahl von Bytes, die gesendet werden, sind die Daten des Zählers.</span><span class="sxs-lookup"><span data-stu-id="42f50-106">In this case, the transfer is the operation, and the accumulating number of bytes that are sent is the counter data.</span></span> <span data-ttu-id="42f50-107">Bei zwei Beispielen führt das Aufteilen der Differenz von akkumulierten Bytes durch den Unterschied in der Anhäufung von Übertragungen zur durchschnittlichen Anzahl von Bytes pro Übertragung während des Zeitraums zwischen den Stichproben.</span><span class="sxs-lookup"><span data-stu-id="42f50-107">For any two samples, dividing the difference of accumulated bytes by the difference in accumulating transfers will produce the average number of bytes per transfer during the period between the samples.</span></span>

<span data-ttu-id="42f50-108">Die folgenden gegen Algorithmen werden bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="42f50-108">The following counter algorithms are provided:</span></span>



| <span data-ttu-id="42f50-109">Counter Type</span><span class="sxs-lookup"><span data-stu-id="42f50-109">CounterType</span></span>                                                                                              | <span data-ttu-id="42f50-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42f50-110">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f50-111">Leistung [ \_ Durchschnittlicher \_ Massen](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Wert 1073874176</span><span class="sxs-lookup"><span data-stu-id="42f50-111">[PERF\_AVERAGE\_BULK](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 1073874176</span></span><br/>       | <span data-ttu-id="42f50-112">Die durchschnittliche Anzahl der verarbeiteten Elemente während eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="42f50-112">Number of items processed, on average, during an operation.</span></span> <span data-ttu-id="42f50-113">Dieser zähtertyp zeigt das Verhältnis der verarbeiteten Elemente (z. b. gesendete Bytes) an die Anzahl der abgeschlossenen Vorgänge an und erfordert eine Basis Eigenschaft mit der durchschnittlichen perf- \_ \_ Basis als zähtertyp.</span><span class="sxs-lookup"><span data-stu-id="42f50-113">This counter type displays a ratio of the items processed (such as bytes sent) to the number of operations completed, and requires a base property with PERF\_AVERAGE\_BASE as the counter type.</span></span> |
| <span data-ttu-id="42f50-114">Leistung [ \_ Counter- \_ Counter](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))-Dezimalwert 272696320</span><span class="sxs-lookup"><span data-stu-id="42f50-114">[PERF\_COUNTER\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696320</span></span><br/>     | <span data-ttu-id="42f50-115">Die durchschnittliche Anzahl der Vorgänge, die während der einzelnen Sekunden des Stichproben Intervalls abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="42f50-115">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="42f50-116">.</span><span class="sxs-lookup"><span data-stu-id="42f50-116">.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="42f50-117">Leistung [ \_ Sample \_ Counter](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span><span class="sxs-lookup"><span data-stu-id="42f50-117">[PERF\_SAMPLE\_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4260864</span></span><br/>        | <span data-ttu-id="42f50-118">Die durchschnittliche Anzahl von Vorgängen, die in einer Sekunde abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="42f50-118">Average number of operations completed in one second.</span></span> <span data-ttu-id="42f50-119">Dieser zähtertyp erfordert eine Basis Eigenschaft mit dem Counter Type perf \_ Sample \_ base.</span><span class="sxs-lookup"><span data-stu-id="42f50-119">This counter type requires a base property with the counter type PERF\_SAMPLE\_BASE.</span></span>                                                                                                                   |
| <span data-ttu-id="42f50-120">Leistung [ \_ Zähler für die \_ Massen \_ Zählung](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))in Dezimal 272696576</span><span class="sxs-lookup"><span data-stu-id="42f50-120">[PERF\_COUNTER\_BULK\_COUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 272696576</span></span><br/> | <span data-ttu-id="42f50-121">Die durchschnittliche Anzahl der Vorgänge, die während der einzelnen Sekunden des Stichproben Intervalls abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="42f50-121">Average number of operations completed during each second of the sample interval.</span></span> <span data-ttu-id="42f50-122">Dieser zähtertyp ist mit dem Leistungs \_ Zählers des Leistungs Zählers identisch \_ , aber er verwendet größere Felder, um größere Werte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="42f50-122">This counter type is the same as the PERF\_COUNTER\_COUNTER type, but it uses larger fields to accommodate larger values.</span></span>                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="42f50-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42f50-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42f50-124">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="42f50-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

