---
description: Festlegen von Administratorrechten für eine Partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Festlegen von Administratorrechten für eine Partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748280"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Festlegen von Administratorrechten für eine Partition

Benutzer, denen die Administrator Rolle der com+-System Anwendung zugewiesen ist, können COM+-Partitionen erstellen, ändern und löschen. Im Verwaltungs Programmkomponenten Dienste können den Benutzern administrative Rollen zugewiesen werden, indem der Ordner **Rollen** der com+-System Anwendung erweitert wird.

Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die com+-System Anwendung den Wert eoac- \_ deaktivierte \_ AAA. Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird beim Starten der System Anwendung im [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Befehl verwendet. Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitions Metriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitions Caches](configuring-the-partition-cache.md)
</dt> <dt>

[Gruppieren von Anwendungen in Partitionen](grouping-applications-into-partitions.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
