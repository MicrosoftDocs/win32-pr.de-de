---
description: Das Windows-Betriebssystem sammelt eine Reihe von Betriebs Statistiken für Arbeitsstationen und Server ab dem Zeitpunkt, zu dem die Arbeitsstation oder der Server Dienst gestartet wurde.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Statistikfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352451"
---
# <a name="statistics-functions"></a><span data-ttu-id="a509a-103">Statistikfunktionen</span><span class="sxs-lookup"><span data-stu-id="a509a-103">Statistics Functions</span></span>

<span data-ttu-id="a509a-104">Das Windows-Betriebssystem sammelt eine Reihe von Betriebs Statistiken für Arbeitsstationen und Server ab dem Zeitpunkt, zu dem die Arbeitsstation oder der Server Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a509a-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="a509a-105">Zum Abrufen dieser Statistiken können Sie die folgende Funktion zur Netzwerk Verwaltungs Statistik aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a509a-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="a509a-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="a509a-106">Function</span></span>                                     | <span data-ttu-id="a509a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a509a-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a509a-108">**Netstatisticsget**</span><span class="sxs-lookup"><span data-stu-id="a509a-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="a509a-109">Ruft Betriebs Statistiken für einen Dienst ab. unterstützt die Arbeitsstations-und Server Dienste.</span><span class="sxs-lookup"><span data-stu-id="a509a-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="a509a-110">Die **netstatisticsget** -Funktion gibt eine [**stat-Arbeitsstation \_ \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) -Struktur zurück, wenn Arbeitsstations Statistiken angefordert werden. die Funktion gibt eine [**stat \_ Server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) -Struktur zurück, wenn Server Statistiken angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a509a-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



