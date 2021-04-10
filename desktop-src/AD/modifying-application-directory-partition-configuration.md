---
title: Ändern der Konfiguration der Anwendungsverzeichnis Partition
description: Eine Anwendungsverzeichnis Partition kann geändert werden, indem bestimmte Attribute des CrossRef-Objekts geändert werden, das die Anwendungsverzeichnis Partition darstellt.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Ändern der Konfiguration der Anwendungsverzeichnis Partition
- Anwendungsverzeichnis Partitionen AD, Ändern der Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c976c297e8491dbb87a32cf2241446ca0403e7f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858141"
---
# <a name="modifying-application-directory-partition-configuration"></a>Ändern der Konfiguration der Anwendungsverzeichnis Partition

Eine Anwendungsverzeichnis Partition kann geändert werden, indem bestimmte Attribute des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts geändert werden, das die Anwendungsverzeichnis Partition darstellt. Um das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt zu suchen, das eine bestimmte Anwendungsverzeichnis Partition darstellt, suchen Sie den Partitions Container nach einem **CrossRef** -Objekt, das einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert aufweist, der gleich dem Distinguished Name der Anwendungsverzeichnis Partition ist. Der Distinguished Name des **CrossRef** -Objekts kann dann verwendet werden, um eine Bindung zum **CrossRef** -Objekt herzustellen.

In der folgenden Tabelle werden die Attribute des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts aufgelistet, die geändert werden können.

| Attribut                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSDS-Replication-notify-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Gibt die Verzögerung in Sekunden an, nach der ein Ursprungs Objekt geändert wird, bevor der erste Replikations Partner benachrichtigt wird. Weitere Informationen finden Sie unter [Anwendungsverzeichnis-Partitions Replikation](application-directory-partition-replication.md).                                                                                                   |
| [**MSDS-Replication-notify-Replication-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Gibt die Verzögerung (in Sekunden) zwischen nachfolgenden Benachrichtigungen zum zweiten, dritten usw. Replikations Partner an. Weitere Informationen finden Sie unter [Anwendungsverzeichnis-Partitions Replikation](application-directory-partition-replication.md).                                                                                                 |
| [**MSDS-sdreferencedomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifiziert die Domäne, die das Sicherheits Subsystem verwendet, um lokale Domänen Verweise in den [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) -Attributen von Objekten in dieser Anwendungsverzeichnis Partition zu interpretieren. Weitere Informationen finden Sie unter [Anwendungsverzeichnis-Partitions Sicherheit](application-directory-partition-security.md). |
| [**MSDS-NC-Replikat-Standorte**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Enthält den Distinguished Name des [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts für jeden Domänen Controller, der ein Replikat der Anwendungsverzeichnis Partition hostet. Weitere Informationen finden Sie unter [Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikats](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 