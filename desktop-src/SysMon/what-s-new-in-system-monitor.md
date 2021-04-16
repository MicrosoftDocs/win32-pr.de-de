---
title: Neues im System Monitor
description: In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases von System Monitor (Sysmon) aufgeführt.
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2020
ms.locfileid: "104389985"
---
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="0db03-103">Neues im System Monitor</span><span class="sxs-lookup"><span data-stu-id="0db03-103">What's New in System Monitor</span></span>

<span data-ttu-id="0db03-104">In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases von System Monitor (Sysmon) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0db03-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="0db03-105">Version</span><span class="sxs-lookup"><span data-stu-id="0db03-105">Version</span></span>     | <span data-ttu-id="0db03-106">Beschreibung der Features</span><span class="sxs-lookup"><span data-stu-id="0db03-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db03-107">Version 3.7</span><span class="sxs-lookup"><span data-stu-id="0db03-107">Version 3.7</span></span> | <span data-ttu-id="0db03-108">Mit dieser Version werden neue Diagrammtypen hinzugefügt, die Möglichkeit zum Auswählen mehrerer Leistungsindikatoren, zum Abrufen von Indikator Werten von einem Punkt im Diagramm, zum Speichern von Diagramm Indikator Werten in einer Protokolldatei und die Option, ein Liniendiagramm fortlaufend im Diagramm Fenster zu scrollen, anstatt sich auf sich selbst zu umschließen. Enthalten in Windows Server 2008 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0db03-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="0db03-109">Version 3.7</span><span class="sxs-lookup"><span data-stu-id="0db03-109">Version 3.7</span></span>

<span data-ttu-id="0db03-110">Neue Eigenschaften und Methoden, die zu " [**ratteritem**](counteritem.md)" hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db03-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="0db03-111">**Getdataat**</span><span class="sxs-lookup"><span data-stu-id="0db03-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="0db03-112">**Ausgewählt**</span><span class="sxs-lookup"><span data-stu-id="0db03-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="0db03-113">**Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="0db03-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="0db03-114">Bereich gültiger Werte für " [ **count. Width** " geändert](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="0db03-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="0db03-115">Neue Eigenschaften und Methoden, die [**Systemmonitor**](systemmonitor.md)hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db03-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="0db03-116">**Batchinglock**</span><span class="sxs-lookup"><span data-stu-id="0db03-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="0db03-117">**Chartscroll**</span><span class="sxs-lookup"><span data-stu-id="0db03-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="0db03-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="0db03-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="0db03-119">**Datapointcount**</span><span class="sxs-lookup"><span data-stu-id="0db03-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="0db03-120">**Enabledigit-Gruppierung**</span><span class="sxs-lookup"><span data-stu-id="0db03-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="0db03-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="0db03-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="0db03-122">**Getlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="0db03-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="0db03-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="0db03-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="0db03-124">**Logsourcestarttime**</span><span class="sxs-lookup"><span data-stu-id="0db03-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="0db03-125">**Logsourcestoptime**</span><span class="sxs-lookup"><span data-stu-id="0db03-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="0db03-126">**Erneut aufzuzeichnen**</span><span class="sxs-lookup"><span data-stu-id="0db03-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="0db03-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="0db03-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="0db03-128">**Scaleum anpassen**</span><span class="sxs-lookup"><span data-stu-id="0db03-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="0db03-129">**Setlogviewrange**</span><span class="sxs-lookup"><span data-stu-id="0db03-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="0db03-130">**Showtimeaxislables**</span><span class="sxs-lookup"><span data-stu-id="0db03-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="0db03-131">Neue Enumerationen, die hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="0db03-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="0db03-132">**Sysmondatatype**</span><span class="sxs-lookup"><span data-stu-id="0db03-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="0db03-133">**Sysmonfiletype**</span><span class="sxs-lookup"><span data-stu-id="0db03-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="0db03-134">"Display [ **typeconstants** " wurden neue Werte für den Anzeigetyp hinzugefügt.](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="0db03-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





