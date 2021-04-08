---
description: Ein appcontainer wird implementiert, indem dem Prozess Token neue Informationen hinzugefügt werden, wobei seaccesscheck () so geändert wird, dass alle veralteten, nicht geänderten Zugriffs Steuerungs Listen (ACL-Objekte) Zugriffs Anforderungen von appcontainer-Prozessen standardmäßig blockieren, sowie für appcontainers verfügbare reacl-Objekte.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementieren eines appcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867811"
---
# <a name="implementing-an-appcontainer"></a>Implementieren eines appcontainer

Ein appcontainer wird implementiert, indem dem Prozess Token neue Informationen hinzugefügt werden, wobei [**seaccesscheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so geändert wird, dass alle veralteten, nicht geänderten Zugriffs Steuerungs Listen (ACL-Objekte) Zugriffs Anforderungen von appcontainer-Prozessen standardmäßig blockieren, sowie für appcontainers verfügbare reacl-Objekte.

## <a name="the-process"></a>Der Prozess

Fügen Sie zunächst neue Informationen für das Prozess Token hinzu. Ändern Sie dann **seaccesscheck ()** , damit alle veralteten, nicht geänderten ACLs standardmäßig Zugriffs Anforderungen von appcontainer-Prozessen blockieren. Zum Schluss sollten Sie Ressourcen für die Ressourcen bereitstellungscontainer bereitstellen.

Die appcontainer-sid ist ein beständiger eindeutiger Bezeichner für den appcontainer. Funktionen-SIDs gewähren Zugriff auf Gruppen von Ressourcen für Gruppen von appcontainers. Eine appcontainernumber ist ein vorübergehendes **DWORD** , mit dem zwischen appcontainers unterschieden werden kann. Es sollte jedoch nicht als Identität für den appcontainer verwendet werden.

Damit ein einzelner appcontainer auf eine Ressource zugreifen kann, fügen Sie seine appcontainersid der ACL für diese Ressource hinzu.

Fügen Sie alle zugehörigen appcontainersids der ACL für diese Ressource hinzu, damit mehrere bestimmte appcontainers auf eine Ressource zugreifen können.

Erstellen Sie zum Verwalten von Berechtigungs Gruppen eine Funktions-sid (GUID), und legen Sie diese Funktions-sid für alle Ressourcen fest, die gewährt werden sollen. Fügen Sie dann die Funktions-sid zum Prozess Token hinzu.

Damit alle appcontainers auf eine Ressource zugreifen können, fügen Sie die SID **alle Anwendungspakete** der ACL für diese Ressource hinzu. Dies verhält sich wie ein Platzhalter.

Sowohl appcontainersid als auch capabilitysid unterstützen Zugriffs Masken in Access Control Einträgen (ACE). Legen Sie nach Bedarf fest.

 

 
