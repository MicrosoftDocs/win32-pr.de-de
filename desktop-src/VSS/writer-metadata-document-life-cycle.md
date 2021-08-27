---
description: Als Reaktion auf ein Identify-Ereignis erstellt jeder writer, der im System vorhanden ist, mithilfe von IVssCreateWriterMetadata ein eigenes Writer-Metadatendokument. Ein Identify-Ereignis wird in der Regel von einem Anfordernden generiert, der IVssBackupComponents::GatherWriterMetadata aufruft.
ms.assetid: bae9bbe7-ca55-47cb-b253-8092007cb181
title: Lebenszyklus von Writermetadatendokumenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2796d1a7b995f13829ac81485f74fa342bebe5e0e312b7b014d761a9962aa74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121573"
---
# <a name="writer-metadata-document-life-cycle"></a>Lebenszyklus von Writermetadatendokumenten

Als Reaktion auf ein [*Identify-Ereignis*](vssgloss-i.md)erstellt jeder writer, der im System vorhanden ist, mithilfe von [**IVssCreateWriterMetadata ein eigenes Writer-Metadatendokument.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) Ein *Identify-Ereignis* wird in der Regel von einem Anfordernden generiert, der [**IVssBackupComponents::GatherWriterMetadata aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)

Beim Erstellen eines Writer-Metadatendokuments muss ein Writer entweder über die [**IVssCreateWriterMetadata-Schnittstelle**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) oder über die Writerinitialisierung ([**CVssWriter::Initialize)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)explizit Folgendes angeben:

-   [*Wiederherstellungsmethode*](vssgloss-r.md)
-   Writername
-   [*Writer-Klassen-ID*](vssgloss-w.md)
-   Datennutzung (siehe [**\_ VSS-VERWENDUNGSTYP \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Datumsquelle (siehe [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Darüber hinaus kann folgendes angegeben werden:

-   Komponenten (die Dateisätze enthalten können oder nicht)
-   Hinzufügen alternativer Zuordnungen
-   Ausschließen von Dateilisten

Eine Übersicht über die Erstellung von Writer-Metadatendokumenten finden Sie unter Writer actions during Backup Initialization (Schreibaktionen [während der Sicherungsinalisierung).](overview-of-backup-initialization.md)

Anfordernde verwenden in der Regel eine von zwei Methoden, um Zugriff auf Writer-Metadaten zu erhalten:

-   Bei den meisten Sicherungsvorgängen verwendet eine Anfordernde [**IVssBackupComponents::GetWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) um eine Instanz der [**IVssExwriterMetadata-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) zu erhalten, um den Zugriff auf die Metadaten eines aktuell ausgeführten Writer zu ermöglichen.
-   Bei Wiederherstellungsvorgängen oder Sicherungen mit importierten Schattenkopien (weitere Informationen zum Importieren von Schattenkopien finden Sie unter [Importieren](importing-transportable-shadow-copied-volumes.md) von transportierbaren Schattenkopien) ruft eine Anfordernde ein XML-Dokument ab, das die Metadaten enthält, und verwendet [**CreateVssExwriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssexaminewritermetadata) um eine [**IVssExschutzWriterMetadata-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) abzurufen, die zum Lesen der Wiederherstellungsmetadaten verwendet wird.

Writer-Metadatendokumente ermöglichen dem Anfordernden, eine Sicherung zu erstellen, um sich über die derzeit ausgeführten Writer während der Ermittlungsphase einer Sicherung zu informieren.

Für die Writer, die sich für die Teilnahme an einer Sicherung entschieden haben, importiert ein Ansucher während der Ermittlungsphase einer Sicherung viele, aber nicht alle Informationen im Writer-Metadatendokument in sein eigenes Sicherungskomponentendokument.

Allerdings enthalten nur Writer-Metadatendokumente und nicht das Sicherungskomponentendokument die Datei- und Pfadspezifikationen.

Weitere Informationen zur Durchführung der Ermittlungsphase eines Sicherungsvorgang finden Sie unter [Übersicht über die Sicherungsermittlungsphase.](overview-of-the-backup-discovery-phase.md)

Darüber hinaus werden nur [*explizit eingeschlossene*](vssgloss-e.md) Komponenten während eines Sicherungsvorgang im Sicherungskomponentendokument gespeichert. Informationen [*zu*](vssgloss-i.md) implizit eingeschlossenen Komponenten sind während eines Sicherungsvorgang nicht im Sicherungskomponentendokument enthalten und müssen mithilfe von Informationen zu den explizit enthaltenen Komponenten und den verfügbaren Writermetadatendokumenten interpoliert werden.

Implizit eingeschlossene Komponenten können möglicherweise weiterhin für die Wiederherstellung [*ausgewählt*](vssgloss-s.md) werden und müssen möglicherweise zum Zeitpunkt der Wiederherstellung explizit in das Dokument sicherungskomponenten eingeschlossen werden. Ebenso wie das Hinzufügen einer Komponente während eines Sicherungsvorgang den Zugriff auf das Writer-Metadatendokument der Komponente erforderte (das dann vom Writer abgerufen wurde), benötigt ein An anfordernde Benutzer Zugriff auf eine Kopie der Writermetadatendokumente dieses Writers, die zur Sicherungszeit gespeichert sind.

Daher besteht die einzige Möglichkeit zum Abrufen aller Informationen zu allen Dateien und Komponenten, die an einer Sicherung oder Wiederherstellung beteiligt sind, in jedem Writer-Metadatendokument für jeden Writer, der an einer Sicherung beteiligt ist, zusammen mit dem Sicherungskomponentendokument. (Weitere Informationen finden Sie unter [Übersicht über die tatsächliche Dateiwiederherstellung.)](overview-of-actual-file-restoration.md)

 

 



