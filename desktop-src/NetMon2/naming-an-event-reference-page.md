---
description: Nachdem Sie ein HTML-Quelldokument für die Ereignis Referenzseite (ERP) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor es in der Ereignisanzeige anzeigen kann.
ms.assetid: 0c668a8b-94a5-4996-8214-4629a24a8337
title: Benennen einer Ereignis Referenzseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9c82b153ce2c7086af3883bcf3c4b34a0e68a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355477"
---
# <a name="naming-an-event-reference-page"></a><span data-ttu-id="844ac-103">Benennen einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="844ac-103">Naming an Event Reference Page</span></span>

<span data-ttu-id="844ac-104">Nachdem Sie ein HTML-Quelldokument für die Ereignis Referenzseite (ERP) erstellt haben, müssen Sie es benennen, bevor Netzwerkmonitor es in der Ereignisanzeige anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="844ac-104">After you author an event reference page (ERP) source HTML document, you must name it before Network Monitor can display it in the Event Viewer.</span></span>

<span data-ttu-id="844ac-105">Namens Monitor-und expertenerp-Dateien mit dem folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="844ac-105">Name monitor and expert ERP files with this format:</span></span>

``` syntax
<ExpertName><EventIdent>.htm (or <MonitorName><EventIdent>.htm)
```

<dl> <dt>

<span data-ttu-id="844ac-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**Profilname**</span><span class="sxs-lookup"><span data-stu-id="844ac-106"><span id="ExpertName"></span><span id="expertname"></span><span id="EXPERTNAME"></span>**ExpertName**</span></span>
</dt> <dd>

<span data-ttu-id="844ac-107">Der dll-Dateiname ohne die Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="844ac-107">DLL file name, excluding the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="844ac-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**Eventident**</span><span class="sxs-lookup"><span data-stu-id="844ac-108"><span id="EventIdent"></span><span id="eventident"></span><span id="EVENTIDENT"></span>**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="844ac-109">Ereignis Bezeichner des expertenerp.</span><span class="sxs-lookup"><span data-stu-id="844ac-109">Event identifier of the expert ERP.</span></span>

<span data-ttu-id="844ac-110">Der Ereignis Bezeichner befindet sich auch im **eventident** -Member der **nmeventdata** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="844ac-110">The event identifier is also found in the **EventIdent** member of the **NMEVENTDATA** structure.</span></span>

</dd> </dl>

<span data-ttu-id="844ac-111">Weitere Informationen zum Erstellen von ERP finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="844ac-111">For more information about creating an ERP, see the following topics:</span></span>

-   [<span data-ttu-id="844ac-112">Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="844ac-112">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="844ac-113">Schreiben einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="844ac-113">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="844ac-114">Testen einer Ereignis Referenzseite</span><span class="sxs-lookup"><span data-stu-id="844ac-114">Testing an Event Reference Page</span></span>](testing-an-event-reference-page.md)

 

 



