---
description: Ein AppContainer wird implementiert, indem dem Prozesstoken neue Informationen hinzugefügt und SeAccessCheck() so geändert wird, dass alle älteren, unveränderten ACL-Objekte (Access Control List) standardmäßig Zugriffsanforderungen von AppContainer-Prozessen blockieren und ACL-Objekte erneut erstellen, die für AppContainers verfügbar sein sollten.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementieren eines AppContainers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d50c0a5aa9f80755084886554a533fe1c82a6791840a9ff4ea4fdcf1476fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670800"
---
# <a name="implementing-an-appcontainer"></a>Implementieren eines AppContainers

Ein AppContainer wird implementiert, indem dem Prozesstoken neue Informationen hinzugefügt und [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so geändert wird, dass alle älteren, unveränderten ACL-Objekte (Access Control List) standardmäßig Zugriffsanforderungen von AppContainer-Prozessen blockieren und ACL-Objekte erneut erstellen, die für AppContainers verfügbar sein sollten.

## <a name="the-process"></a>Der Prozess

Fügen Sie zunächst neue Informationen für das Prozesstoken hinzu. Ändern Sie **dann SeAccessCheck(),** sodass alle veralteten, unveränderten ACLs Zugriffsanforderungen von AppContainer-Prozessen standardmäßig blockieren. Schließlich müssen ACL-Ressourcen, die für AppContainers verfügbar sein sollen, erneut hinzugefügt werden.

Die AppContainer-SID ist ein dauerhafter eindeutiger Bezeichner für den App-Container. Funktions-SIDs gewähren Gruppen von AppContainers Zugriff auf Ressourcengruppen. Eine AppContainerNumber ist ein vorübergehendes **DWORD,** das verwendet wird, um zwischen AppContainers zu unterscheiden. Sie sollte jedoch nicht als Identität für den AppContainer verwendet werden.

Damit ein einzelner AppContainer auf eine Ressource zugreifen kann, fügen Sie dessen AppContainerSID der ACL für diese Ressource hinzu.

Damit mehrere bestimmte AppContainer auf eine Ressource zugreifen können, fügen Sie der ACL für diese Ressource alle AppContainerSIDs hinzu.

Um Gruppen von Berechtigungen zu verwalten, erstellen Sie eine Funktions-SID (eine GUID), und legen Sie diese Funktions-SID für alle Ressourcen ab, die gewährt werden sollen. Fügen Sie ihrem Prozesstoken dann die Funktions-SID hinzu.

Damit alle AppContainer auf eine Ressource zugreifen können, fügen Sie der ACL für diese Ressource die **SID** ALLE ANWENDUNGSPAKETE hinzu. Dies verhält sich wie ein Platzhalter.

Sowohl AppContainerSID als auch CapabilitySID unterstützen Zugriffsmasken in Access Control Entries (ACE). Legen Sie entsprechend fest.

 

 
