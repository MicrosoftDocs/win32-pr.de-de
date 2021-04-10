---
description: Ein Anforderer ist eine beliebige Anwendung, die die VSS-API (insbesondere die IVssBackupComponents-Schnittstelle) zum Anfordern der Dienste des Volumeschattenkopie-Dienst zum Erstellen und Verwalten von Schatten Kopien und schattenkopiesätzen von einem oder mehreren Volumes verwendet.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Anfordernde Personen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215544"
---
# <a name="requesters"></a>Anfordernde Personen

Ein [*Anforderer*](vssgloss-r.md) ist eine beliebige Anwendung, die die VSS-API (insbesondere die [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle) zum Anfordern der Dienste des Volumeschattenkopie-Dienst zum Erstellen und Verwalten von Schatten Kopien und schattenkopiesätzen von einem oder mehreren Volumes verwendet.

Das typische Beispiel für einen Anforderer (und der einzige, der in dieser Dokumentation behandelt wird) ist eine VSS-fähige Sicherungs-/Wiederherstellungsanwendung, die Schatten kopierte Daten als stabile Quelle für die Sicherungs Vorgänge verwendet.

Neben der Einleitung von Schatten Kopien kommunizieren Sicherungs-/Wiederherstellungs Anforderer-Anwendungen mit Daten Producer (Writer), um Informationen zum System zu sammeln und Writer zu signalisieren, Ihre Daten für die Sicherung vorzubereiten.

## <a name="requester-state"></a>Status der Anforderer

Ein Anforderer behält seine Zustandsinformationen in einem XML-basierten Metadatenobjekt bei, das als Sicherungs Komponenten Dokument bezeichnet wird. Die Anforderer-Metadaten sind erforderlich, aber nicht ausreichend, damit ein Anforderer ein Dateisystem sichern und wiederherstellen kann. Hierfür gibt es die folgenden Gründe:

-   Während eines Sicherungs Vorgangs wird nur eine Teilmenge aller Komponenten, die an der Sicherung beteiligt sind –[*nicht auswählbar für Sicherungs*](vssgloss-s.md) Komponenten ohne auswählbare für Sicherungs-und auswählbare Sicherungs Komponenten, die explizit in der Sicherung [*enthalten*](vssgloss-e.md) sind, dem Dokument mit den Sicherungs Komponenten der Anforderer hinzugefügt.
-   Die Informationen selbst für die Komponenten, die dem Dokument mit den Sicherungs Komponenten hinzugefügt werden, sind unvollständig – Datei-und Pfadspezifikationen sind nicht enthalten.
-   Während des Wiederherstellungs Vorgangs kann eine Komponente, die implizit in der Sicherung [*enthalten*](vssgloss-i.md) ist, [*für die Wiederherstellung ausgewählt*](vssgloss-s.md) werden und kann daher explizit in die Wiederherstellung eingeschlossen werden. Hierfür muss das Dokument mit den Sicherungs Komponenten der Anforderer mit Informationen aus gespeicherten Kopien des Writer-Metadatendokuments eines Writers aktualisiert werden.

Um die vollständige Angabe eines Sicherungs-oder Wiederherstellungs Vorgangs zu ermöglichen, ermöglicht die VSS-API dem Anforderer das Abfragen der Metadaten von Writern (während der Sicherungen) oder das Überprüfen gespeicherter Writer-Metadaten (während der Wiederherstellung) Außerdem kann ein Writer im Rahmen eines Sicherungs-oder Wiederherstellungs Vorgangs Komponenten Informationen im Sicherungs Komponenten Dokument ändern.

Mithilfe der Informationen zu den Komponenten, die für die Sicherung und Wiederherstellung ausgewählt wurden, und den Regeln bezüglich der Komponentenauswahl (Weitere Informationen finden Sie unter [Einrichten der Komponenten Organisation](definition-of-components-by-writers.md) und [Arbeiten mit Selektierbarkeit und logischen Pfaden](working-with-selectability-and-logical-paths.md)), kann ein Anforderer ermitteln, welche Dateien er sichern oder wiederherstellen muss und wo er diese Dateien finden kann.

Als Teil einer Sicherung müssen sowohl die Anforderer-als auch die Writer-Metadaten gespeichert werden, damit Sie in der Wiederherstellung verwendet werden können. Im Gegensatz dazu erfordern Wiederherstellungs Vorgänge das Abrufen der alten Sicherungs Komponenten und Writer-Metadatendokumente, um vollständige Anweisungen zum Wiederherstellen von Dateien zu erhalten.

## <a name="requester-interprocess-communication"></a>Prozessübergreifende Kommunikation mit Anforderer

Der Anforderer behält die Kontrolle über VSS-Sicherungs-und Wiederherstellungs Vorgänge, indem er com-Ereignisse über verschiedene Aufrufe in der requestapi erzeugt. Diese Aufrufe können folgende Aktionen ausführen:

-   Anforderungen an die Anbieter stellen, z. b. [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) bewirkt, dass der Anbieter eine Schatten Kopie des ausgewählten Volumes erstellt.
-   Veranlassen Sie, dass die Writer Informationen zurückgeben, z. b. [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) ermöglicht dem Anforderer, das Writer-Metadatendokument jedes Writers abzurufen.
-   Erfordert, dass Writer verschiedene Phasen der Schattenkopie-und Sicherungs Vorgänge vorbereiten oder verarbeiten können, z. b. [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) signalisiert Writer, dass die e/a-Sperre eingerichtet werden soll.

Ein Anforderer empfängt Informationen von den Writern mithilfe von livedokumenten oder gespeicherten Writer-Metadatendokumenten und durch die Verwendung der [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) -Schnittstelle, die der Writer aktualisieren kann.

## <a name="life-cycle-of-a-requester-during-backup"></a>Lebenszyklus eines Anforderers während der Sicherung

Im folgenden finden Sie eine Zusammenfassung des Lebenszyklus der Anforderer für die Sicherung:

1.  Instanziieren und Initialisieren von VSS-API-Schnittstellen.
2.  Wenden Sie sich an Writer, und rufen Sie Ihre Informationen ab
3.  Wählen Sie die zu sichernden Daten aus.
4.  Fordern Sie eine Schatten Kopie des Anbieters an.
5.  Sichern Sie die Daten.
6.  Geben Sie die-Schnittstelle und die Schatten Kopie frei.

## <a name="life-cycle-of-a-requester-during-restore"></a>Lebenszyklus eines Anforderers während der Wiederherstellung

Der Lebenszyklus der Wiederherstellung erfordert keine Schatten Kopie, erfordert aber trotzdem die Writer-Zusammenarbeit:

1.  Instanziieren von VSS-API-Schnittstellen.
2.  Initialisieren Sie den Anforderer für den Wiederherstellungs Vorgang, indem Sie ein Dokument mit gespeicherten Sicherungs Komponenten laden.
3.  Abrufen gespeicherter Writer-Metadaten und Sicherungs Komponenten Dokumente.
4.  Kontaktieren Sie die Writer, um die Zusammenarbeit zu initialisieren
5.  Überprüfen Sie das Dokument mit den Sicherungs Komponenten auf Writer-Updates.
6.  Stellen Sie die Daten wieder her.

 

 



