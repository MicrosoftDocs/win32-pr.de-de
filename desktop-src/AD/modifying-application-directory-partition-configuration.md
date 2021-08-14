---
title: Ändern der Anwendungsverzeichnispartitionskonfiguration
description: Eine Anwendungsverzeichnispartition kann geändert werden, indem bestimmte Attribute des crossRef-Objekts geändert werden, das die Anwendungsverzeichnispartition darstellt.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Ändern von Application Directory Partition Configuration AD
- Anwendungsverzeichnispartitionen AD , Konfiguration ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc378536a552bb7612877fc09913fdbad9daf507adbb34b5f53f8946c946e8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186315"
---
# <a name="modifying-application-directory-partition-configuration"></a>Ändern der Anwendungsverzeichnispartitionskonfiguration

Eine Anwendungsverzeichnispartition kann geändert werden, indem bestimmte Attribute des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) geändert werden, das die Anwendungsverzeichnispartition darstellt. Um das [**crossRef-Objekt**](/windows/desktop/ADSchema/c-crossref) zu suchen, das eine bestimmte Anwendungsverzeichnispartition darstellt, suchen Sie im Container Partitionen nach einem **crossRef-Objekt,** das über einen [**nCName-Attributwert**](/windows/desktop/ADSchema/a-ncname) verfügt, der dem Distinguished Name der Anwendungsverzeichnispartition entspricht. Der Distinguished Name des **crossRef-Objekts** kann dann zum Binden an das **crossRef-Objekt verwendet** werden.

In der folgenden Tabelle sind die Attribute des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) aufgeführt, die geändert werden können.

| attribute                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-Notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Gibt die Verzögerung in Sekunden an, nachdem ein Ursprüngliches Objekt geändert wurde, bevor der erste Replikationspartner benachrichtigt wird. Weitere Informationen finden Sie unter [Application Directory Partition Replication](application-directory-partition-replication.md).                                                                                                   |
| [**msDS-Replication-Notify-Subsequent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Gibt die Verzögerung in Sekunden zwischen nachfolgenden Benachrichtigungen an den zweiten, dritten und so weiter an Replikationspartner an. Weitere Informationen finden Sie unter [Application Directory Partition Replication](application-directory-partition-replication.md).                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifiziert die Domäne, die das Sicherheitssubsystem zum Interpretieren lokaler Domänenverweise in den [**nTSecurityDescriptor-Attributen**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) von Objekten in dieser Anwendungsverzeichnispartition verwendet. Weitere Informationen finden Sie unter [Application Directory Partition Security](application-directory-partition-security.md). |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Enthält den Distinguished Name des [**nTDSDSA-Objekts**](/windows/desktop/ADSchema/c-ntdsdsa) für jeden Domänencontroller, der ein Replikat der Anwendungsverzeichnispartition hostet. Weitere Informationen finden Sie unter [Hinzufügen oder Löschen eines Anwendungsverzeichnispartitionsreplikats.](adding-or-deleting-an-application-directory-partition-replica.md)            |



 

 

 