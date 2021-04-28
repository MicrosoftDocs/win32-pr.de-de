---
description: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3c34e43daf8346888a32ef76d55f93ac5a563e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088368"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.

## <a name="platform"></a>Plattform

 **Server :** Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad:** Hoch  
**Häufigkeit:** Hoch  


## <a name="description"></a>BESCHREIBUNG

In Windows Server 2008 R2 kann der Dateireplikationsdienst (File Replication Service, FRS) nicht zum Replizieren von DFS-Ordnern (verteiltes Dateisystem) oder benutzerdefinierten Daten (nicht SYSVOL) verwendet werden. Ein Windows Server 2008 R2-Domänencontroller kann frs weiterhin verwenden, um den Inhalt der SYSVOL-Freigabe in einer Domäne zu replizieren, die FRS zum Replizieren der SYSVOL-Freigabe zwischen Domänencontrollern verwendet. Windows Server 2008 R2-Server können frs jedoch nicht verwenden, um den Inhalt eines Replikats zu replizieren, das sich von der SYSVOL-Freigabe unterscheidet. Der DFS-Replikation Dienst ist ein Ersatz für FRS und kann verwendet werden, um den Inhalt der SYSVOL-Freigabe, der DFS-Ordner und anderer benutzerdefinierter Daten (nicht SYSVOL) zu replizieren. Migrieren Sie alle Nicht-SYSVOL FRS-Replikatgruppen zu DFS-Replikation. Es wird außerdem dringend empfohlen, die Replikation der SYSVOL-Freigabe von FRS zu DFS-Replikation zu migrieren, da DFS-Replikation stabiler, skalierbarer und eine bessere Replikationsleistung als FRS bietet.

## <a name="manifestation"></a>Manifestation

Die FRS-Replikation benutzerdefinierter Daten unterbricht nach einem unmittelbaren Upgrade unumkehrbar. Die einzige Möglichkeit zur Wiederherstellung aus dieser Situation wäre die Neuinstallation eines älteren Betriebssystems auf dem Server und das erneute Initialisieren der FRS-Replikation. Server, die auf Windows Server 2008 R2 aktualisiert wurden, dürfen nicht an vorhandenen FRS-Replikationsgruppen teilnehmen.

## <a name="mitigation-of-impact"></a>Entschärfung der Auswirkungen

Um Probleme zu vermeiden, die aufgrund dieser Änderungen auftreten können, migrieren Sie benutzerdefinierte FRS-Replikationssätze zu DFS-Replikation. Der DFS-Replikation-Dienst bietet gegenüber FRS viele Vorteile, einschließlich verbesserter Verwaltungstools, höherer Leistung und delegierter Verwaltung.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [ÜBERSICHT ÜBER FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [DFS-Replikation: Häufig gestellte Fragen](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Anleitung zur SYSVOL-Replikationsmigration: FRS- zu DFS-Replikation](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
