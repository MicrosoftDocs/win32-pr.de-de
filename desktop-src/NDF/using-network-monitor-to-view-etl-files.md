---
title: Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien
description: Netzwerkmonitor 3,3 ermöglicht es Benutzern, eine ETL-Datei zu analysieren, zu filtern und anzuzeigen (unter Verwendung von Windows Vista oder höher).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "103961041"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="5b351-103">Verwenden von Microsoft-Netzwerkmonitor zum Anzeigen von ETL-Dateien</span><span class="sxs-lookup"><span data-stu-id="5b351-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="5b351-104">[Netzwerkmonitor 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) ermöglicht es Benutzern, eine ETL-Datei zu analysieren, zu filtern und anzuzeigen (unter Verwendung von Windows Vista oder höher).</span><span class="sxs-lookup"><span data-stu-id="5b351-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="5b351-105">(Wenn Sie Netzwerkmonitor 3,2 verwenden, müssen Sie zusätzliche Parser von [codeplex](https://www.codeplex.com/NMParsers) herunterladen und installieren, um die Netzwerk Ablauf Verfolgungs Ereignisse zu erzeugen.)</span><span class="sxs-lookup"><span data-stu-id="5b351-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="5b351-106">Korrelierte ETL-Dateien gruppieren die relevanten Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5b351-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="5b351-107">Die unten stehende ScrollBar zeigt eine korrelierte Datei, die in Netzwerkmonitor geöffnet ist</span><span class="sxs-lookup"><span data-stu-id="5b351-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Screenshot, der die Netzwerkmonitor anzeigt, wobei Korrelierte Ereignisse im linken Fenster hervorgehoben werden und utevent in der Dropdown-Dropdown-Funktion hervorgehoben ist.](images/ut-netmon1.png)

<span data-ttu-id="5b351-109">Korrelierte Ereignisse werden nach Aktivität im linken Bereich gruppiert.</span><span class="sxs-lookup"><span data-stu-id="5b351-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="5b351-110">Sie können ein Ereignis im Frame Zusammenfassungs Bereich auswählen und dann mit der rechten Maustaste klicken, um die Konversation auf der Netzwerk Ereignis Ebene auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5b351-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="5b351-111">Dadurch wird eine verwandte Aktivität im linken Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b351-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="5b351-112">Wenn Sie im linken Bereich eine bestimmte Aktivität auswählen und Sie erweitern, wird die Liste der Anbieter für die korrelierten Ereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b351-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Screenshot, der die Netzwerkmonitor mit einer Aktivität anzeigt, die im linken Bereich ausgewählt ist, sowie Ereignisse, die diesem Ereignis im rechten Bereich entsprechen.](images/ut-netmon2.png)

<span data-ttu-id="5b351-114">Wenn Sie einen bestimmten Anbieter im linken Bereich auswählen, wird eine Liste der für diesen Anbieter und jede Aktivität spezifischen Ereignisse im Frame Zusammenfassungs Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b351-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Screenshot, der einen bestimmten Anbieter anzeigt, der im linken Bereich ausgewählt ist, sowie eine Liste der für den anbieterspezifischen Ereignisse, die im oberen rechten Bereich hervorgehoben sind.](images/ut-netmon3.png)

<span data-ttu-id="5b351-116">Filter können in Netzwerkmonitor angewendet werden, um die Anzeige und Suche nach den richtigen Ereignissen oder Paketen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="5b351-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="5b351-117">Beispielsweise können Sie einen Filter auf ausgewählte Fehlerereignisse anwenden (z. b. **utevent. Header. Descriptor. Level = = 2**), um Sie in einer bestimmten Farbe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5b351-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Screenshot, der das Dialogfeld "Farb Filter bearbeiten" anzeigt.](images/ut-netmon4.png)

<span data-ttu-id="5b351-119">Filter können auch angewendet werden, um verschiedene Anbieter in unterschiedlichen Farben zu markieren, sodass die Ergebnisse leichter angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="5b351-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Screenshot, der ein Beispiel für verschiedene Anbieter anzeigt, die in unterschiedlichen Farben gekennzeichnet sind.](images/ut-netmon5.png)

<span data-ttu-id="5b351-121">Um einen Filter anzuwenden, klicken Sie im Menü **Filter** auf **colorfilters** .</span><span class="sxs-lookup"><span data-stu-id="5b351-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="5b351-122">In der folgenden Tabelle sind einige Beispiele für nützliche Filter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b351-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="5b351-123">Filtern</span><span class="sxs-lookup"><span data-stu-id="5b351-123">Filter</span></span>                                                                        | <span data-ttu-id="5b351-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b351-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="5b351-125">Utevent. Header. Descriptor. Level = = 2</span><span class="sxs-lookup"><span data-stu-id="5b351-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="5b351-126">Filtert nur Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="5b351-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="5b351-127">Utevent. Header. Descriptor. Level = = 3</span><span class="sxs-lookup"><span data-stu-id="5b351-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="5b351-128">Filtert nur Warnungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5b351-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="5b351-129">UTEvent.Header.Descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="5b351-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="5b351-130">Filtert nur Ereignisse mit der Ereignis-ID 2001.</span><span class="sxs-lookup"><span data-stu-id="5b351-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="5b351-131">WLAN \_ microsoftwindowtauscht autoConfig</span><span class="sxs-lookup"><span data-stu-id="5b351-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="5b351-132">Filtert nur Ereignisse aus dem WLAN-Dienst.</span><span class="sxs-lookup"><span data-stu-id="5b351-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="5b351-133">N802 \_ microsoftwindowsnwifi</span><span class="sxs-lookup"><span data-stu-id="5b351-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="5b351-134">Filtert nur Ereignisse des systemeigenen WiFi-Treibers.</span><span class="sxs-lookup"><span data-stu-id="5b351-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="5b351-135">WLAN \_ microsoftwindowswap-AutoConfig und UTEvent.Header.Descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="5b351-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="5b351-136">Filtert nur Ereignisse mit der vom WLAN-Dienst ausgegebenen Ereignis-ID 2001.</span><span class="sxs-lookup"><span data-stu-id="5b351-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




