---
description: .
ms.assetid: 18a03469-737a-4905-9851-f7961c46b867
title: Der Datei Replikations Dienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3acf7eb6310f2c296abfd5eb1db0f30c4b48dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360570"
---
# <a name="file-replication-service-frs-is-deprecated-in-windows-server-2008-r2"></a>Der Datei Replikations Dienst (File Replication Service, FRS) ist in Windows Server 2008 R2 veraltet

## <a name="platform"></a>Plattform

 **Server:** Windows Server 2008 R2  

## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad:** Hochrangiger  
**Häufigkeit:** Hochrangiger  


## <a name="description"></a>BESCHREIBUNG

In Windows Server 2008 R2 kann der Datei Replikations Dienst (File Replication Service, FRS) nicht zum Replizieren von verteiltes Dateisystem Ordner (DFS) oder benutzerdefinierten Daten (nicht-SYSVOL) verwendet werden. Ein Windows Server 2008 R2-Domänen Controller kann weiterhin FRS zum Replizieren des Inhalts der SYSVOL-Freigabe in einer Domäne verwenden, die FRS zum Replizieren der SYSVOL-Freigabe zwischen Domänen Controllern verwendet. Windows Server 2008 R2-Server können FRS jedoch nicht verwenden, um den Inhalt einer Replikat Gruppe außer der SYSVOL-Freigabe zu replizieren. Der DFS-Replikation-Dienst ist ein Ersatz für FRS und kann verwendet werden, um die Inhalte der SYSVOL-Freigabe, der DFS-Ordner und anderer benutzerdefinierter Daten (nicht-SYSVOL) zu replizieren. Migrieren Sie alle nicht-SYSVOL-FRS-Replikat Gruppen zu DFS-Replikation. Außerdem wird dringend empfohlen, die Replikation der SYSVOL-Freigabe von FRS zu DFS-Replikation zu migrieren, da DFS-Replikation stabiler, skalierbar und eine bessere Replikations Leistung als FRS aufweist.

## <a name="manifestation"></a>Ausstrahlung

Die FRS-Replikation von benutzerdefinierten Daten wird bei einem direkten Upgrade unwiderruflich unterbrechen. Die einzige Möglichkeit, diese Situation zu beheben, besteht darin, ein älteres Betriebssystem auf dem Server neu zu installieren und die FRS-Replikation erneut zu initialisieren. Server, die auf Windows Server 2008 R2 aktualisiert wurden, dürfen nicht an vorhandenen FRS-Replikations Gruppen teilnehmen.

## <a name="mitigation-of-impact"></a>Minderung der Auswirkung

Um Probleme zu vermeiden, die möglicherweise aufgrund dieser Änderungen auftreten, migrieren Sie benutzerdefinierte FRS-Replikations Gruppen zu DFS-Replikation. Der DFS-Replikation-Dienst hat gegenüber FRS viele Vorteile, einschließlich verbesserter Verwaltungs Tools, höherer Leistung und Delegierter Verwaltung.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [FRS (Übersicht)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754297(v=ws.11))
-   [DFS-Replikation: Häufig gestellte Fragen](/windows-server/storage/dfs-replication/dfsr-faq)
-   [Anleitung zur SYSVOL-Replikationsmigration: FRS- zu DFS-Replikation](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)

 

 
