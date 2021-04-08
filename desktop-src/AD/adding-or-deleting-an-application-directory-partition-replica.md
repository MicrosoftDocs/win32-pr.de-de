---
title: Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikats
description: Das erste Replikat einer Anwendungsverzeichnis Partition wird auf dem Domänen Controller erstellt, der zum Zeitpunkt der Erstellung an ihn gebunden war.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikat-AD
- Anwendungsverzeichnis Partitionen anzeigen, hinzufügen oder Löschen eines Partitions Replikats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101463"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Hinzufügen oder Löschen eines Anwendungsverzeichnis-Partitions Replikats

Das erste Replikat einer Anwendungsverzeichnis Partition wird auf dem Domänen Controller erstellt, der zum Zeitpunkt der Erstellung an ihn gebunden war. Auf allen Domänen Controllern in der Gesamtstruktur können zusätzliche Replikate erstellt werden, nicht notwendigerweise in derselben Domäne wie der anfängliche Domänen Controller. Ein Anwendungsverzeichnis-Partitions Replikat kann nur auf einem Domänen Controller vorhanden sein, auf dem Windows Server 2003 oder höher ausgeführt wird. Weitere Informationen finden Sie in diesem TechNet-Artikel zur [Partitions Verwaltung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Führen Sie die folgenden Schritte aus, um ein Replikat für eine Anwendungsverzeichnis Partition hinzuzufügen.**

1.  Durchsuchen Sie den Container Partitionen nach einem [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert aufweist, der gleich dem Distinguished Name der Anwendungsverzeichnis Partition ist.
2.  Binden an das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt mit aktivierter Delegierung. Dies ist erforderlich, da das **CrossRef** -Objekt nur für den Inhaber der Domain-Naming-Inhaber-Rolle geändert werden kann. Wenn die Delegierung aktiviert ist, kann der Domänen Controller den Inhaber der Domain-Naming FSMO-Rolle mit denselben Anmelde Informationen kontaktieren.
3.  Fügen Sie den Distinguished Name des [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts für den Domänen Controller, der das neue Replikat hostet, dem [**msDS-NC-Replikat-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) -Attribut des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts hinzu.

Wenn der neue [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut Wert auf den neuen Domänen Controller repliziert wird, der ein Replikat der Anwendungsverzeichnis Partition hostet, wird die KCC ausgelöst, um die Anwendungsverzeichnis Partition auf den Zieldomänen Controller zu replizieren.

Um ein Replikat für eine Anwendungsverzeichnis Partition zu entfernen, führen Sie dieselben Schritte wie oben aus, um das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt zu suchen, das die Anwendungsverzeichnis Partition darstellt, und entfernen Sie den Wert, der dem Domänen Controller entspricht, aus dem [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut des **CrossRef** -Objekts.

Wenn der neue [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut Wert auf den Domänen Controller repliziert wird, der kein Replikat der Anwendungsverzeichnis Partition mehr hostet, wird die KCC ausgelöst, um das Replikat der Anwendungsverzeichnis Partition auf dem Zieldomänen Controller zu entfernen.

Wenn ein Domänen Controller, der ein Anwendungsverzeichnis-Partitions Replikat hostet, entfernt oder herabgestuft wird, entfernt der Active Directory Server automatisch den Wert, der dem Domänen Controller entspricht, aus dem [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut aller [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekte.

 

 