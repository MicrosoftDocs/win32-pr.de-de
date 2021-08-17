---
description: Das Konzept einer Komponente ist entscheidend für die Organisation, welche Dateien von welchem Writer sicherungs- oder wiederhergestellt werden sollen.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: VSS-Metadatenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac121ae62798d0318233dba48e6d0b56c36e2065a71fe8e12af9c963893dd027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751433"
---
# <a name="vss-metadata-components"></a>VSS-Metadatenkomponenten

Entscheidend für die Organisation, welche Dateien von welchem Writer sicherungs- oder wiederhergestellt werden sollen, ist das Konzept einer [*Komponente*](vssgloss-c.md).

Mit Komponenten kann ein Writer einem Sicherungsmodul angeben, wie seine Dateien organisiert werden sollen, welche Abhängigkeiten zwischen Dateien bestehen und welche Art von Daten diese Dateien enthalten können. Dadurch kann eine Sicherungs-Engine entscheiden, wie Dateien gespeichert werden, um maximale Effizienz zu erzielen.

Darüber hinaus verwenden VSS-basierte Anwendungen Komponenten als Bausteine für ihre Metadaten und das Medium für die Kommunikation zwischen Writer und Anfordernden.

Writer und Anfordernde speichern Informationen zu Komponenten separat – im Writer Metadata Document bzw. im Backup Components Document – und die Informationen unterscheiden sich in jeder Darstellung.

Komponenteninformationen in Writer Metadata Documents umfassen Folgendes:

-   Informationen von nur einem Writer in jedem Dokument
-   Alle Komponenten dieses Writers, unabhängig [](vssgloss-e.md) davon, ob sie explizit eingeschlossen werden können oder implizit [*in*](vssgloss-i.md) einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen werden müssen
-   [*Logische Pfadinformationen,*](vssgloss-l.md) die verwendet werden, um eine für die Sicherungskomponente auswählbare Komponente bestimmten nicht auswählbaren Sicherungskomponenten zu zuordnen, wodurch ein Komponentensatz erstellt wird.
-   Die [*Dateisatzinformationen*](vssgloss-f.md) – Pfad, Dateispezifikation und Rekursionsflag – werden für jede Komponente verwaltet.

Writer-Metadatendokumente enthalten auch Metadateninformationen auf Writerebene, z. B. Wiederherstellungsmethoden und alternative Speicherortzuordnungen für die Wiederherstellung. Writer-Metadatendokumente sind schreibgeschützt. Die Schnittstelle zum Untersuchen dieser Informationen ist [**IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

Die Komponenteninformationen in Sicherungskomponentendokumenten umfassen Folgendes:

-   Nur Informationen zu explizit eingeschlossenen Komponenten
-   Metadateninformationen auf Writerebene, z. B. alternative Speicherortzuordnungen und Wiederherstellungen
-   Zustandsinformationen, die einen Sicherungs- oder Wiederherstellungsvorgang beschreiben

Sicherungskomponentendokumente enthalten keine Informationen zu den [*Komponentendateisätzen.*](vssgloss-f.md) Sicherungskomponentendokumente sind nicht schreibgeschützt und können vom Writer geändert werden. Die Schnittstelle für den Zugriff auf diese Informationen ist [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Der Lebenszyklus und die Beziehung zwischen den beiden Ausdrücken einer Komponente können wie folgt verstanden werden:

-   Writer sind für die anfänglichen Definitionen von Komponenten verantwortlich.
-   Eine Anfordernde untersucht die Metadaten aller Writer und deren Komponenten.
-   Anhand der Auswählbarkeits- und logischen Pfadinformationen von Komponenten bestimmt ein An anfordernde Benutzer, welche Komponenten explizit eingeschlossen werden müssen, die explizit eingeschlossen werden können, welche Komponentensätze definieren und welche Member von Komponentensätzen sind.
-   Eine anfordernde Person fügt die Komponenten hinzu, die explizit eingeschlossen werden müssen, und schließt implizit Unterkomponenten [*in*](/windows) Komponentensätze ein (deren Informationen nicht im Sicherungskomponentendokument enthalten sind).
-   Bei der Behandlung von Ereignissen können Writer und Anfordernde die im Dokument sicherungskomponenten gespeicherten Komponenteninformationen ändern und untersuchen, um ihre Aktivitäten zu koordinieren.

Sowohl die Komponenteninformationen der Writer- als auch der anfordernden Version sind erforderlich, um Sicherungs- und Wiederherstellungsvorgänge ordnungsgemäß auszuführen, und beide müssen mit allen gesicherten Daten gespeichert werden:

-   [Komponententypen](component-types.md)
-   [Definition von Komponenten nach Writern](definition-of-components-by-writers.md)
-   [Verwendung von Komponenten durch den Anfordernden](use-of-components-by-the-requestor.md)

 

 
