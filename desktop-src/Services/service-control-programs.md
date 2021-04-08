---
description: Die Dienste werden von einem Dienst Steuerungsprogramm gestartet und gesteuert.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Dienst Steuerungsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862383"
---
# <a name="service-control-programs"></a><span data-ttu-id="a58df-103">Dienst Steuerungsprogramme</span><span class="sxs-lookup"><span data-stu-id="a58df-103">Service Control Programs</span></span>

<span data-ttu-id="a58df-104">Die Dienste werden von einem Dienst Steuerungsprogramm gestartet und gesteuert.</span><span class="sxs-lookup"><span data-stu-id="a58df-104">A service control program starts and controls services.</span></span> <span data-ttu-id="a58df-105">Es führt die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a58df-105">It performs the following actions:</span></span>

-   <span data-ttu-id="a58df-106">Startet einen Dienst-oder Treiber Dienst, wenn der Starttyp "Service \_ Demand Start" lautet \_ .</span><span class="sxs-lookup"><span data-stu-id="a58df-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="a58df-107">Sendet Steuerungsanforderungen an einen laufenden Dienst.</span><span class="sxs-lookup"><span data-stu-id="a58df-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="a58df-108">Fragt den aktuellen Status eines laufenden Dienstanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="a58df-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="a58df-109">Diese Aktionen erfordern ein geöffnetes Handle für das Dienst Objekt.</span><span class="sxs-lookup"><span data-stu-id="a58df-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="a58df-110">Zum Abrufen des Handles muss das Dienst Steuerungsprogramm Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a58df-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="a58df-111">Verwenden Sie die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion, um ein Handle für die SCM-Datenbank auf einem angegebenen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a58df-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="a58df-112">Verwenden Sie die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -oder die-Funktion von "up [**Service Service"**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) , um ein Handle für das Dienst Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a58df-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="a58df-113">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="a58df-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a58df-114">Dienst Start</span><span class="sxs-lookup"><span data-stu-id="a58df-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="a58df-115">Dienst Steuerungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="a58df-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="a58df-116">Steuern eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="a58df-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



