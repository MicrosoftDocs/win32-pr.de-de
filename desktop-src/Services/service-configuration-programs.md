---
description: Programmierer und Systemadministratoren verwenden Dienst Konfigurationsprogramme, um die Datenbank der installierten Dienste zu ändern oder abzufragen.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Dienst Konfigurationsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128897"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="2a7ae-103">Dienst Konfigurationsprogramme</span><span class="sxs-lookup"><span data-stu-id="2a7ae-103">Service Configuration Programs</span></span>

<span data-ttu-id="2a7ae-104">Programmierer und Systemadministratoren verwenden Dienst Konfigurationsprogramme, um die Datenbank der installierten Dienste zu ändern oder abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="2a7ae-105">Der Zugriff auf die Datenbank ist auch über die-Registrierungsfunktionen möglich.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="2a7ae-106">Sie sollten jedoch nur die SCM-Konfigurationsfunktionen verwenden, die sicherstellen, dass der Dienst ordnungsgemäß installiert und konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="2a7ae-107">Die SCM-Konfigurationsfunktionen erfordern entweder ein Handle für ein scmanager-Objekt oder ein Handle für ein Dienst Objekt.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="2a7ae-108">Um diese Handles zu erhalten, muss das Dienst Konfigurationsprogramm Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="2a7ae-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="2a7ae-109">Verwenden Sie die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion, um ein Handle für die SCM-Datenbank auf einem angegebenen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="2a7ae-110">Verwenden Sie die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -oder die-Funktion von "up [**Service Service"**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) , um ein Handle für das Dienst Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a7ae-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="2a7ae-111">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="2a7ae-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2a7ae-112">Dienst Installation, Entfernung und Enumeration</span><span class="sxs-lookup"><span data-stu-id="2a7ae-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="2a7ae-113">Dienstkonfiguration:</span><span class="sxs-lookup"><span data-stu-id="2a7ae-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="2a7ae-114">Konfigurieren eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="2a7ae-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



