---
description: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72940d2b73b807d5420aface3096714ac132df2095d154fc7563717c33fa6e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759940"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Der Dateireplikationsdienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet.

## <a name="platform"></a>Plattform

 **Server –** Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Hoch  
**Häufigkeit:** Hoch  


## <a name="description"></a>Beschreibung

In Windows Server 2008 R2 kann der Dateireplikationsdienst (File Replication Service, FRS) nicht zum Replizieren von verteiltes Dateisystem-Ordnern (DFS) oder benutzerdefinierten Daten (nicht SYSVOL) verwendet werden. Ein Windows Server 2008 R2-Domänencontroller kann weiterhin FRS verwenden, um den Inhalt der SYSVOL-Freigabe in einer Domäne zu replizieren, die FRS zum Replizieren der SYSVOL-Freigabe zwischen Domänencontrollern verwendet. Allerdings können Windows Server 2008 R2-Server FRS nicht verwenden, um den Inhalt von Replikaten zu replizieren, die von der SYSVOL-Freigabe getrennt sind. Der DFS-Replikation-Dienst ist ein Ersatz für FRS und kann verwendet werden, um den Inhalt der SYSVOL-Freigabe, der DFS-Ordner sowie anderer benutzerdefinierter Daten (nicht SYSVOL) zu replizieren. Migrieren Sie alle NICHT-SYSVOL FRS-Replikatgruppen zu DFS-Replikation. Außerdem wird dringend empfohlen, die Replikation der SYSVOL-Freigabe von FRS zu DFS-Replikation zu migrieren, da DFS-Replikation stabiler, skalierbarer ist und eine bessere Replikationsleistung als FRS auf hat.

## <a name="manifestation"></a>Manifestation

Die FRS-Replikation benutzerdefinierter Daten unterbricht bei einem upgradebasierten Upgrade unumkehrbar. Die einzige Möglichkeit zur Wiederherstellung in dieser Situation ist die Neuinstallation eines älteren Betriebssystems auf dem Server und das erneute Initialisieren der FRS-Replikation. Server, die auf Windows Server 2008 R2 aktualisiert wurden, dürfen nicht an vorhandenen FRS-Replikationsgruppen teilnehmen.

## <a name="mitigation-of-impact"></a>Entschärfung der Auswirkungen

Um Probleme zu vermeiden, die aufgrund dieser Änderungen auftreten können, migrieren Sie benutzerdefinierte FRS-Replikationssätze zu DFS-Replikation. Der DFS-Replikation-Dienst bietet viele Vorteile gegenüber FRS, einschließlich verbesserter Verwaltungstools, höherer Leistung und delegierter Verwaltung.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [ÜBERSICHT ÜBER FRS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [DFS-Replikation: Häufig gestellte Fragen](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Anleitung zur SYSVOL-Replikationsmigration: FRS- zu DFS-Replikation](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
