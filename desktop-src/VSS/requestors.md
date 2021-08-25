---
description: Ein Anforderer ist jede Anwendung, die die VSS-API (insbesondere die IVssBackupComponents-Schnittstelle) verwendet, um die Dienste der Volumeschattenkopie-Dienst anzufordern, um Schattenkopien und Schattenkopiesätze von einem oder mehreren Volumes zu erstellen und zu verwalten.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Anfordernde Personen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e7fa7b1718b0da278dabb164fbffee43c939cd688c150e202bfafc4731a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866380"
---
# <a name="requesters"></a>Anfordernde Personen

Ein [*Anforderer*](vssgloss-r.md) ist jede Anwendung, die die VSS-API (insbesondere die [**IVssBackupComponents-Schnittstelle)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) verwendet, um die Dienste der Volumeschattenkopie-Dienst anzufordern, um Schattenkopien und Schattenkopiesätze von einem oder mehreren Volumes zu erstellen und zu verwalten.

Das typischste Beispiel für einen Anforderer (und das einzige, das in dieser Dokumentation behandelt wird) ist eine VSS-fähige Sicherungs-/Wiederherstellungsanwendung, die schattenkopierte Daten als stabile Quelle für die Sicherungsvorgänge verwendet.

Zusätzlich zum Initiieren von Schattenkopien kommunizieren Sicherungs-/Wiederherstellungsanwendungen von Anfordernden mit Datenerstellern (Writern), um Informationen über das System zu sammeln und Writern zu signalisieren, ihre Daten für die Sicherung vorzubereiten.

## <a name="requester-state"></a>Anfordererstatus

Ein Anforderer verwaltet seine Zustandsinformationen in einem XML-basierten Metadatenobjekt namens Sicherungskomponentendokument. Die Anforderermetadaten sind erforderlich, aber nicht ausreichend, um einem Anforderer das Sichern und anschließende Wiederherstellen eines Dateisystems zu ermöglichen. Dies hat folgende Gründe:

-   Während eines Sicherungsvorgangs wurden dem Sicherungskomponentendokument des Anfordernden nur für eine Teilmenge aller an der Sicherung beteiligten Komponenten , die [*für Sicherungskomponenten nicht ausgewählt*](vssgloss-s.md) werden können, ohne für Sicherungsvorher auswählbar und für Sicherungskomponenten auswählbar, die explizit in die Sicherung [*eingeschlossen*](vssgloss-e.md) wurden, ihre Informationen hinzugefügt.
-   Die Informationen, auch für die Komponenten, die dem Sicherungskomponentendokument hinzugefügt wurden, sind unvollständig– Datei- und Pfadspezifikationen sind nicht enthalten.
-   Bei Wiederherstellungsvorgängen kann eine [*Komponente,*](vssgloss-i.md) die implizit in die Sicherung eingeschlossen ist, für die [*Wiederherstellung ausgewählt*](vssgloss-s.md) werden und kann daher explizit in die Wiederherstellung eingeschlossen werden. Dies erfordert die Aktualisierung des Sicherungskomponentendokuments des Anforderers mit Informationen aus gespeicherten Kopien des Writer-Metadatendokuments eines Writers.

Um eine vollständige Spezifikation eines Sicherungs- oder Wiederherstellungsvorgangs zu ermöglichen, ermöglicht die VSS-API dem Anforderer, ausgeführte Writermetadaten (während sicherungen) abzufragen oder gespeicherte Writermetadaten (während der Wiederherstellungen) zu untersuchen. Darüber hinaus kann ein Writer komponenteninformationen im Sicherungskomponentendokument während eines Sicherungs- oder Wiederherstellungsvorgangs ändern.

Anhand der Informationen darüber, welche Komponenten für die Sicherung und Wiederherstellung ausgewählt wurden, und den Regeln für die Komponentenauswahl (weitere Informationen finden Sie unter Einrichten der [Komponentenorganisation](definition-of-components-by-writers.md) und [Arbeiten mit Auswählbarkeit und logischen Pfaden),](working-with-selectability-and-logical-paths.md)kann ein Anforderer bestimmen, welche Dateien von welchem Writer er sichern oder wiederherstellen muss und wo er diese Dateien finden kann.

Im Rahmen einer Sicherung müssen die Metadaten des Anfordernden und des Writers gespeichert werden, damit sie bei der Wiederherstellung verwendet werden können. Umgekehrt erfordern Wiederherstellungsvorgänge das Abrufen der alten Sicherungskomponenten und WriterMetadatendokumente, um vollständige Anweisungen zum Wiederherstellen von Dateien zu erhalten.

## <a name="requester-interprocess-communication"></a>Prozessübergreifende Kommunikation des Anfordernden

Der Anforderer behält die Kontrolle über VSS-Sicherungs- und -Wiederherstellungsvorgänge, indem er COM-Ereignisse über verschiedene Aufrufe in der Anfordernden-API generiert. Diese Aufrufe können folgendermaßen ausführen:

-   Stellen Sie Anforderungen der Anbieter, z. [**B. bewirkt IVssBackupComponents::D oSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) dass der Anbieter eine Schattenkopie des ausgewählten Volumes erstellt.
-   Lösen Sie die Writer aus, um Informationen zurückzugeben, z. B. [**ermöglicht IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) dem Anforderer das Abrufen des Writer-Metadatendokuments jedes Writers.
-   Writer müssen sich auf verschiedene Phasen der Schattenkopie- und Sicherungsvorgänge vorbereiten oder diese verarbeiten, z. [**B. IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) signalisiert Writern, dass sie für das Einfrieren der E/A eingerichtet werden.

Ein Anforderer empfängt Informationen von den Writern über live gespeicherte Writer-Metadatendokumente und über die [**IVssComponent-Schnittstelle,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) die der Writer aktualisieren kann.

## <a name="life-cycle-of-a-requester-during-backup"></a>Lebenszyklus eines Anforderers während der Sicherung

Im Folgenden wird der Lebenszyklus des Anfordernden für die Sicherung zusammengefasst:

1.  Instanziieren und Initialisieren von VSS-API-Schnittstellen.
2.  Wenden Sie sich an Writer, und rufen Sie ihre Informationen ab.
3.  Wählen Sie zu sichernde Daten aus.
4.  Fordern Sie eine Schattenkopie des Anbieters an.
5.  Sichern Sie die Daten.
6.  Geben Sie die Schnittstelle und die Schattenkopie frei.

## <a name="life-cycle-of-a-requester-during-restore"></a>Lebenszyklus einer Anfordernden während der Wiederherstellung

Für den Wiederherstellungslebenszyklus ist keine Schattenkopie erforderlich, aber dennoch eine Zusammenarbeit mit dem Writer:

1.  Instanziieren sie VSS-API-Schnittstellen.
2.  Initialisieren Sie den Anforderer für den Wiederherstellungsvorgang, indem Sie ein gespeichertes Sicherungskomponentendokument laden.
3.  Ruft gespeicherte Writermetadaten und Sicherungskomponentendokumente ab.
4.  Wenden Sie sich an die Autoren, um die Zusammenarbeit zu initialisieren.
5.  Suchen Sie nach Writerupdates für das Sicherungskomponentendokument.
6.  Stellen Sie die Daten wieder her.

 

 



