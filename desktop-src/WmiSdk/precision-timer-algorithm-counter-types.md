---
description: Die Zähler Typen der Genauigkeits Geber Algorithmen erhalten genauere Messwerte als systemtimer.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Zähler Typen für Genauigkeits Geber Algorithmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759769"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="2b211-103">Zähler Typen für Genauigkeits Geber Algorithmen</span><span class="sxs-lookup"><span data-stu-id="2b211-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="2b211-104">Die Zähler Typen der Genauigkeits Geber Algorithmen erhalten genauere Messwerte als systemtimer.</span><span class="sxs-lookup"><span data-stu-id="2b211-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="2b211-105">Der Dienst, der die Daten bereitstellt, stellt auch einen Zeitstempel bereit. Dadurch werden die Fehler vermieden, die aufgrund der kurzen und Variablen Zeit zwischen der Erfassung des Systemzeit Stempels und der Auflistung der Daten aus der Leistungs-dll auftreten können.</span><span class="sxs-lookup"><span data-stu-id="2b211-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="2b211-106">Dieser Basis Zeitstempel für Genauigkeits Timer ist eine perf \_ Precision- \_ Zeitstempel Eigenschaft, die unmittelbar auf die perf Precision-Zeit Geber Eigenschaft folgen muss \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2b211-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="2b211-107">CounterType-Konstante</span><span class="sxs-lookup"><span data-stu-id="2b211-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="2b211-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b211-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b211-109">Leistung [ \_ Genauigkeits \_ System- \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span><span class="sxs-lookup"><span data-stu-id="2b211-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="2b211-110">Ähnelt \_ dem Leistungs Zähler- \_ Timer, mit dem Unterschied, dass er anstelle des Systemzeit Stempels eine Zähler definierte Zeitbasis verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b211-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="2b211-111">Leistung [ \_ Genauigkeit \_ 100 NS \_ Timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span><span class="sxs-lookup"><span data-stu-id="2b211-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="2b211-112">Ähnelt dem perf-Wert von \_ 100 nsec \_ , außer dass er eine 100-ns-Zähler definierte Zeitbasis anstelle des System-100-ns-Zeitstempels verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b211-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2b211-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b211-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b211-114">WMI-Leistungsdaten Typen</span><span class="sxs-lookup"><span data-stu-id="2b211-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

