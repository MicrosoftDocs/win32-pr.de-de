---
title: Anwendungsverzeichnis Partitionen
description: In Windows Server 2003 unterstützen Active Directory Domain Services Anwendungsverzeichnis Partitionen.
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- Anwendungsverzeichnis Partitionen AD
- Anwendungsverzeichnis Partitionen AD, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038805"
---
# <a name="application-directory-partitions"></a>Anwendungsverzeichnis Partitionen

In Windows Server 2003 unterstützen Active Directory Domain Services Anwendungsverzeichnis Partitionen. Eine Anwendungsverzeichnis Partition kann eine Hierarchie beliebiger Objekttypen enthalten, mit Ausnahme von Sicherheits Prinzipale, und kann so konfiguriert werden, dass Sie auf eine beliebige Gruppe von Domänen Controllern in der Gesamtstruktur repliziert wird. Im Gegensatz zu einer Domänen Partition ist eine Anwendungsverzeichnis Partition nicht für die Replikation auf alle Domänen Controller in einer Domäne erforderlich, und die Partition kann auf Domänen Controllern in verschiedenen Domänen der Gesamtstruktur repliziert werden. Weitere Informationen zu Anwendungsverzeichnis Partitionen finden Sie unter Informationen [zu Anwendungsverzeichnis Partitionen](about-application-directory-partitions.md).

Eine Anwendungsverzeichnis Partition kann erstellt werden. geändert und gelöscht mit standardmäßigen ADSI-, LDAP-und [System. Director yservices](/dotnet/api/system.directoryservices) -Vorgängen. Der Sicherheitskontext, der erforderlich ist, um eine Anwendungsverzeichnis Partition zu erstellen und zu ändern, ist identisch mit der zum Erstellen einer Domänen Partition.

In den folgenden Themen wird beschrieben, wie Sie mit Anwendungsverzeichnis Partitionen arbeiten:

-   [Anwendungsverzeichnis-Partitions Replikation](application-directory-partition-replication.md)
-   [Sicherheit der Anwendungsverzeichnis Partition](application-directory-partition-security.md)
-   [Erstellen einer Anwendungsverzeichnis Partition](creating-an-application-directory-partition.md)
-   [Löschen einer Anwendungsverzeichnis Partition](deleting-an-application-directory-partition.md)
-   [Auflisten von Anwendungsverzeichnis Partitionen in einer Gesamtstruktur](enumerating-application-directory-partitions-in-a-forest.md)
-   [Suchen eines Anwendungsverzeichnis-Partitions Host Servers](locating-an-application-directory-partition-host-server.md)
-   [Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikats](adding-or-deleting-an-application-directory-partition-replica.md)
-   [Auflisten von Replikaten einer Anwendungsverzeichnis Partition](enumerating-replicas-of-an-application-directory-partition.md)
-   [Ändern der Konfiguration der Anwendungsverzeichnis Partition](modifying-application-directory-partition-configuration.md)

 

 