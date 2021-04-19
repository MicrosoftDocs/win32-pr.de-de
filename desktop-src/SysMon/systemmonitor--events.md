---
title: Systemmonitor-Ereignisse
description: 'Die Systemmonitor-Klasse weist die folgenden Ereignisse auf:'
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337136"
---
# <a name="systemmonitor-events"></a><span data-ttu-id="1581d-103">Systemmonitor-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="1581d-103">SystemMonitor Events</span></span>

<span data-ttu-id="1581d-104">Die [**Systemmonitor**](systemmonitor.md) -Klasse weist die folgenden Ereignisse auf:</span><span class="sxs-lookup"><span data-stu-id="1581d-104">The [**SystemMonitor**](systemmonitor.md) class has the following events:</span></span>

-   [<span data-ttu-id="1581d-105">**Oncounteradded**</span><span class="sxs-lookup"><span data-stu-id="1581d-105">**OnCounterAdded**</span></span>](systemmonitor-oncounteradded.md)
-   [<span data-ttu-id="1581d-106">**Oncounterdeleted**</span><span class="sxs-lookup"><span data-stu-id="1581d-106">**OnCounterDeleted**</span></span>](-systemmonitor-oncounterdeleted.md)
-   [<span data-ttu-id="1581d-107">**Oncounterselected**</span><span class="sxs-lookup"><span data-stu-id="1581d-107">**OnCounterSelected**</span></span>](-systemmonitor-oncounterselected.md)
-   [<span data-ttu-id="1581d-108">**Ondblclick**</span><span class="sxs-lookup"><span data-stu-id="1581d-108">**OnDblClick**</span></span>](-systemmonitor-ondblclick.md)
-   [<span data-ttu-id="1581d-109">**Onsamplecollected**</span><span class="sxs-lookup"><span data-stu-id="1581d-109">**OnSampleCollected**</span></span>](-systemmonitor-onsamplecollected.md)

> [!Note]  
> <span data-ttu-id="1581d-110">Sie müssen den Ereignishandler zurückgeben, bevor das [**Aktualisierungs Intervall**](systemmonitor-updateinterval.md) abläuft. Andernfalls zeigt sysmon ein Meldungs Feld an, das dem Benutzer anzeigt, dass es für das vorherige Aktualisierungs Intervall keine Stichproben von zählungs Werten gibt.</span><span class="sxs-lookup"><span data-stu-id="1581d-110">You must return from the event handler before the [**update interval**](systemmonitor-updateinterval.md) expires; otherwise, SYSMON displays a message box indicating to the user that it was unable to sample counter values for the previous update interval.</span></span>

 

 

 




