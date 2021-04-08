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
# <a name="service-control-programs"></a>Dienst Steuerungsprogramme

Die Dienste werden von einem Dienst Steuerungsprogramm gestartet und gesteuert. Es führt die folgenden Aktionen aus:

-   Startet einen Dienst-oder Treiber Dienst, wenn der Starttyp "Service \_ Demand Start" lautet \_ .
-   Sendet Steuerungsanforderungen an einen laufenden Dienst.
-   Fragt den aktuellen Status eines laufenden Dienstanbieter ab.

Diese Aktionen erfordern ein geöffnetes Handle für das Dienst Objekt. Zum Abrufen des Handles muss das Dienst Steuerungsprogramm Folgendes ausführen:

1.  Verwenden Sie die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion, um ein Handle für die SCM-Datenbank auf einem angegebenen Computer abzurufen.
2.  Verwenden Sie die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -oder die-Funktion von "up [**Service Service"**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) , um ein Handle für das Dienst Objekt zu erhalten.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Dienst Start](service-startup.md)
-   [Dienst Steuerungsanforderungen](service-control-requests.md)
-   [Steuern eines Dienstanbieter mit SC](controlling-a-service-using-sc.md)

 

 



