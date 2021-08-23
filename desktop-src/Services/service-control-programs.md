---
description: Ein Dienststeuerungsprogramm startet und steuert Dienste.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Dienststeuerungsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889043"
---
# <a name="service-control-programs"></a>Dienststeuerungsprogramme

Ein Dienststeuerungsprogramm startet und steuert Dienste. Es führt die folgenden Aktionen aus:

-   Startet einen Dienst oder Treiberdienst, wenn der Starttyp SERVICE \_ DEMAND \_ START ist.
-   Sendet Steuerungsanforderungen an einen ausgeführten Dienst.
-   Fragt den aktuellen Status eines ausgeführten Diensts ab.

Diese Aktionen erfordern ein offenes Handle für das Dienstobjekt. Um das Handle zu erhalten, muss das Dienststeuerungsprogramm:

1.  Verwenden Sie [**die OpenSCManager-Funktion,**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) um ein Handle für die SCM-Datenbank auf einem angegebenen Computer abzurufen.
2.  Verwenden Sie [**die OpenService-**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) [**oder CreateService-Funktion,**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) um ein Handle für das Dienstobjekt zu erhalten.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Dienststart](service-startup.md)
-   [Dienststeuerungsanforderungen](service-control-requests.md)
-   [Steuern eines Diensts mit sc](controlling-a-service-using-sc.md)

 

 



