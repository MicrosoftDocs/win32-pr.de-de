---
description: 'Als Reaktion auf ein identifizierungsereignis erstellt jeder Writer, der auf dem System vorhanden ist, sein eigenes Writer-Metadatendokument mithilfe von ivsskreateschreitermetadata. Ein identifizereignis wird normalerweise von einem Anforderer generiert, der IVssBackupComponents:: gatherschreibmetadata aufruft.'
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Lebenszyklus von Writer-Metadatendokumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45be5748625d21f99abe3e77e0d6474a62210904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348400"
---
# <a name="writer-metadata-document-life-cycle"></a>Lebenszyklus von Writer-Metadatendokumenten

Als Reaktion auf ein [*identifizierungsereignis*](vssgloss-i.md)erstellt jeder Writer, der auf dem System vorhanden ist, sein eigenes Writer-Metadatendokument mithilfe von [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata). Ein *identifizereignis* wird normalerweise von einem Anforderer generiert, der [**IVssBackupComponents:: gatherschreibmetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)aufruft.

Beim Erstellen eines Writer-Metadatendokuments entweder über die [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) -Schnittstelle oder über die Writer-Initialisierung ([**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)) muss ein Writer Folgendes explizit angeben:

-   [*Wiederherstellungsmethode*](vssgloss-r.md)
-   Writer-Name
-   [*Writer-Klassen-ID*](vssgloss-w.md)
-   Datennutzung (siehe [**VSS \_ - \_ Verwendungstyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Datums Quelltyp (siehe [**VSS \_ - \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Außerdem kann Sie Folgendes angeben:

-   Komponenten (die Datei Sätze enthalten können oder enthalten dürfen)
-   Alternative Zuordnungen hinzufügen
-   Dateilisten ausschließen

Eine Übersicht über die Erstellung von Writer-Metadatendokumenten finden Sie in [Writer-Aktionen während der Sicherungs Initialisierung](overview-of-backup-initialization.md).

Anforderer verwendet in der Regel eine von zwei Methoden, um Zugriff auf Writer-Metadaten zu erhalten:

-   Bei den meisten Sicherungs Vorgängen verwendet ein Anforderer [**IVssBackupComponents:: getschreibmetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) , um eine Instanz der [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) -Schnittstelle zu erhalten, um den Zugriff auf die Metadaten eines derzeit ausgeführten Writers zuzulassen.
-   Für Wiederherstellungs Vorgänge oder Sicherungen mit importierten Schatten Kopien (Weitere Informationen zum Importieren von Schatten Kopien finden Sie unter [Importieren von transportable-Schattenkopievolumes](importing-transportable-shadow-copied-volumes.md) ), Ruft ein Anforderer ein XML-Dokument ab, das die Metadaten enthält, [**und verwendet "**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) ", um die Wiederherstellungs [**Metadaten zu**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) lesen.

Writer-Metadatendokumente ermöglichen es der anfordernden Person, eine Sicherung durchzuführen, um zu erfahren, wie derzeit Writer während der Ermittlungsphase einer Sicherung ausgeführt werden.

Für diejenigen, die sich für die Teilnahme an einer Sicherung entschieden haben, importiert ein Anforderer während der Ermittlungsphase einer Sicherung viel, aber nicht alle Informationen im Writer-Metadatendokument in ein eigenes Sicherungs Komponenten Dokument.

Allerdings enthalten nur Writer-Metadatendokumente und nicht das Dokument mit den Sicherungs Komponenten die Datei-und Pfadspezifikationen.

Weitere Informationen zur Durchführung der Ermittlungsphase eines Sicherungs Vorgangs finden Sie unter Übersicht über [die Sicherungs Ermittlungsphase](overview-of-the-backup-discovery-phase.md).

Außerdem werden während eines Sicherungs Vorgangs nur [*explizit enthaltene*](vssgloss-e.md) Komponenten im Dokument mit den Sicherungs Komponenten gespeichert. Informationen zu [*implizit enthaltenen*](vssgloss-i.md) Komponenten sind während eines Sicherungs Vorgangs nicht im Dokument mit den Sicherungs Komponenten enthalten und müssen mithilfe von Informationen zu den explizit enthaltenen Komponenten und den verfügbaren Writer-Metadatendokumenten interpoliert werden.

Implizit enthaltene Komponenten können weiterhin [*für die Wiederherstellung ausgewählt*](vssgloss-s.md) werden und müssen möglicherweise beim Wiederherstellungs Zeitpunkt explizit im Dokument mit den Sicherungs Komponenten enthalten sein. Wenn in diesem Fall eine Komponente während eines Sicherungs Vorgangs Zugriff auf das Writer-Metadatendokument der Komponente benötigt (dann vom Writer abgerufen), benötigt ein Anforderer Zugriff auf eine Kopie der Writer-Metadatendokumente dieses Writers, die zum Zeitpunkt der Sicherung gespeichert werden.

Daher besteht die einzige Möglichkeit zum Abrufen aller Informationen zu allen Dateien und Komponenten, die an einer Sicherung oder Wiederherstellung beteiligt sind, darin, dass jedes Writer-Metadatendokument für jeden Writer, der an einer Sicherung beteiligt ist, zusammen mit dem Sicherungs Komponenten Dokument gespeichert wird. (Weitere Informationen finden Sie unter [Übersicht über die tatsächliche Dateiwiederherstellung](overview-of-actual-file-restoration.md).)

 

 



