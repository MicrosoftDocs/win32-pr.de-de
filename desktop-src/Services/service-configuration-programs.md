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
# <a name="service-configuration-programs"></a>Dienst Konfigurationsprogramme

Programmierer und Systemadministratoren verwenden Dienst Konfigurationsprogramme, um die Datenbank der installierten Dienste zu ändern oder abzufragen. Der Zugriff auf die Datenbank ist auch über die-Registrierungsfunktionen möglich. Sie sollten jedoch nur die SCM-Konfigurationsfunktionen verwenden, die sicherstellen, dass der Dienst ordnungsgemäß installiert und konfiguriert ist.

Die SCM-Konfigurationsfunktionen erfordern entweder ein Handle für ein scmanager-Objekt oder ein Handle für ein Dienst Objekt. Um diese Handles zu erhalten, muss das Dienst Konfigurationsprogramm Folgendes ausführen:

1.  Verwenden Sie die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion, um ein Handle für die SCM-Datenbank auf einem angegebenen Computer abzurufen.
2.  Verwenden Sie die [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) -oder die-Funktion von "up [**Service Service"**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) , um ein Handle für das Dienst Objekt zu erhalten.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Dienst Installation, Entfernung und Enumeration](service-installation-removal-and-enumeration.md)
-   [Dienstkonfiguration:](service-configuration.md)
-   [Konfigurieren eines Dienstanbieter mit SC](configuring-a-service-using-sc.md)

 

 



