---
description: Entscheidend für die Organisation, welche Dateien von welchem Writer gesichert oder wiederhergestellt werden sollen, ist das Konzept einer Komponente.
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

Entscheidend für die Organisation, welche Dateien von welchem Writer gesichert oder wiederhergestellt werden sollen, ist das Konzept einer [*Komponente*](vssgloss-c.md).

Komponenten ermöglichen es einem Writer, einer Sicherungs-Engine anzugeben, wie die Dateien organisiert werden sollen, welche Abhängigkeiten zwischen Dateien bestehen und welche Art von Daten diese Dateien enthalten können. Dadurch kann eine Sicherungs-Engine entscheiden, wie Dateien für maximale Effizienz gespeichert werden sollen.

Darüber hinaus verwenden VSS-basierte Anwendungen Komponenten als Bausteine für ihre Metadaten und das Medium für die Kommunikation zwischen Writer und Anforderer.

Writer und Anforderer speichern Informationen zu Komponenten separat – im Writer Metadata Document bzw. im Backup Components Document – und die Informationen unterscheiden sich in jeder Darstellung.

Komponenteninformationen in Writer Metadata Documents umfassen Folgendes:

-   Informationen von nur einem Writer in jedem Dokument
-   Alle Komponenten dieses Writers, unabhängig davon, ob sie [*explizit eingeschlossen*](vssgloss-e.md) werden können oder implizit in einen Sicherungs- oder Wiederherstellungsvorgang [*eingeschlossen*](vssgloss-i.md) werden müssen
-   Informationen zum [*logischen Pfad,*](vssgloss-l.md) die verwendet werden, um eine für die Sicherungskomponente auswählbare mit einer bestimmten, für Sicherungskomponenten nicht auswählbaren Komponente zu verknüpfen und so einen Komponentensatz zu bilden.
-   Die [*Dateisatzinformationen*](vssgloss-f.md) – Pfad, Dateispezifikation und Rekursionsflag – werden für jede Komponente verwaltet.

WriterMetadatendokumente enthalten auch Metadateninformationen auf Writerebene, z. B. Wiederherstellungsmethoden und alternative Speicherortzuordnungen für die Wiederherstellung. Writer Metadata Documents sind schreibgeschützt. Die Schnittstelle zum Untersuchen dieser Informationen ist [**IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

Komponenteninformationen in Sicherungskomponentendokumenten umfassen Folgendes:

-   Nur Informationen zu explizit eingeschlossenen Komponenten
-   Metadateninformationen auf Writerebene, z. B. Alternative Speicherortzuordnungen und Wiederherstellung
-   Zustandsinformationen, die einen Sicherungs- oder Wiederherstellungsvorgang beschreiben

Sicherungskomponentendokumente enthalten keine Informationen zu [*den Dateisätzen*](vssgloss-f.md)der Komponenten. Sicherungskomponentendokumente sind nicht schreibgeschützt und können vom Writer geändert werden. Die Schnittstelle für den Zugriff auf diese Informationen ist [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Der Lebenszyklus und die Beziehung zwischen den beiden Ausdrücken einer Komponente können wie folgt verstanden werden:

-   Writer sind für die anfänglichen Definitionen von Komponenten verantwortlich.
-   Ein Anforderer untersucht die Metadaten aller Writer und deren Komponenten.
-   Anhand der Selektivitäts- und logischen Pfadinformationen von Komponenten bestimmt ein Anforderer, welche Komponenten explizit eingeschlossen werden müssen, welche explizit eingeschlossen werden können, welche Komponentensätze definieren und welche Elemente von Komponentensätzen sind.
-   Ein Anforderer fügt die Komponenten hinzu, die explizit eingeschlossen werden müssen, und schließt implizit Unterkomponenten in [*Komponentensätze*](/windows) ein (deren Informationen nicht im Sicherungskomponentendokument enthalten sind).
-   Bei der Behandlung von Ereignissen können Writer und Anforderer die im Dokument sicherungskomponenten gespeicherten Komponenteninformationen ändern und untersuchen, um ihre Aktivitäten zu koordinieren.

Sowohl der Writer als auch die Komponenteninformationen der Anfordernden sind erforderlich, um Sicherungs- und Wiederherstellungsvorgänge ordnungsgemäß auszuführen, und beide müssen mit allen gesicherten Daten gespeichert werden:

-   [Komponententypen](component-types.md)
-   [Definition von Komponenten nach Writern](definition-of-components-by-writers.md)
-   [Verwendung von Komponenten durch den Anforderer](use-of-components-by-the-requestor.md)

 

 
