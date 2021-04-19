---
description: Writer sind Anwendungen oder Dienste, die persistente Informationen in Dateien auf dem Datenträger speichern und die Namen und Speicherorte dieser Dateien für anfordernde Personen mithilfe der schattenkopienschnittstelle bereitstellen.
ms.assetid: 24fc2d7c-f8d6-49ca-9bb5-0179bef68e78
title: Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ca409e8dc6153a6b3e2b747dc23cc391055471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353079"
---
# <a name="writers"></a>Writers

[*Writer*](vssgloss-w.md) sind Anwendungen oder Dienste, die persistente Informationen in Dateien auf dem Datenträger speichern und die Namen und Speicherorte dieser Dateien für anfordernde Personen mithilfe der schattenkopienschnittstelle bereitstellen.

Bei Sicherungs Vorgängen stellen Writer sicher, dass Ihre Daten ineskalierend und stabil sind – geeignet für Schatten Kopien und Sicherungen. Writer arbeiten mit Wiederherstellungen zusammen, indem Sie nach Möglichkeit Dateien entsperren und bei Bedarf Alternative Speicherorte angeben.

Wenn während eines VSS-Sicherungs Vorgangs keine Writer vorhanden sind, kann noch eine Schatten Kopie erstellt werden. In diesem Fall befinden sich alle Daten auf dem auf dem Schatten kopierten Volume im [*Absturz konsistenten Zustand*](vssgloss-c.md).

## <a name="writer-state"></a>Writer-Status

Writer behalten ihren Zustand in einem XML-basierten Metadatenobjekt, dem [*Writer-Metadatendokument*](vssgloss-w.md).

Diese Writer-Metadaten sind die einzige Datenstruktur, die den [*Datei Satz*](vssgloss-f.md)– Pfad, die Datei Spezifikation und das Rekursions Flag – der zu sichernden und wiederherzustellenden Daten enthält.

Das Writer-Metadatendokument organisiert die Datei Sätze des Writers in Gruppen oder [*Komponenten*](vssgloss-c.md). Die Beziehung einer dieser Komponenten während Sicherungs-und Wiederherstellungs Vorgängen für die anderen vom Writer verwalteten Komponenten wird im Writer-Metadatendokument von der [*selekmentabilität*](vssgloss-s.md)der Komponente für die Sicherung, der [*selekmentelle für die Wiederherstellung*](vssgloss-s.md)und den [*logischen Pfaden*](vssgloss-l.md)beschrieben. (Weitere Informationen finden Sie unter [Einrichten der Komponenten Organisation](definition-of-components-by-writers.md) und [Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md).)

Weitere Informationen, die die Wiederherstellung von Dateien und andere Probleme steuern, sind in diesem Dokument ebenfalls enthalten.

Der Anforderer benötigt die Writer-Metadaten in Verbindung mit seinem eigenen Dokument mit den Sicherungs Komponenten, um eine Sicherung oder eine Wiederherstellung zu verarbeiten.

Im Gegensatz zum Sicherungs Komponenten Dokument sollte das Writer-Metadatendokument als schreibgeschützte Struktur betrachtet werden. Nachdem ein Writer ihn erstellt hat, wird das Dokument nicht geändert.

## <a name="writer-event-handling"></a>Writer-Ereignis Behandlung

Die VSS-Vorgänge eines Writers werden durch den Empfang von COM-Ereignissen initiiert.

Wenn keine Ereignisse vorhanden sind, führt ein Writer keine VSS-Vorgänge aus (z. b. eine VSS-Sicherung oder-Wiederherstellung). Stattdessen werden die normalen arbeiten durchführt, z. b. das reagieren auf Datenbankabfragen, das Verwalten von Benutzerdaten oder das Bereitstellen anderer Dienste.

Gehen Sie folgendermaßen vor, um sicherzustellen, dass die Fehlerbehandlung mehrerer paralleler Sicherungs-und Wiederherstellungs Sitzungen ordnungsgemäß durchgeführt wird, und um sicherzustellen, dass eine Sicherungs-oder Wiederherstellungs Sitzung eine andere nicht beschädigt.

-   Wenn der-Ereignishandler eines Writers (z. b. [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze)) die [**CVssWriterEx2:: getessionid**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-getsessionid), [**CVssWriter:: setschreiterfailure**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-setwriterfailure)oder [**CVssWriterEx2:: setschreiterfailureex**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriterex2-setwriterfailureex) -Methode aufruft, muss der Ereignishandler die-Methode im gleichen Thread aufrufen, der den Ereignishandler aufgerufen hat.
-   Die Implementierung eines Ereignis Handlers (z. b. [**OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) ) durch den Writer kann bei Bedarf Arbeit an Arbeitsthreads auslagern, solange jeder Arbeits Thread alle benötigten Fehlerberichte an den ursprünglichen ereignishandlerthread zurück marshun.

## <a name="handling-identify-events"></a>Behandeln von identifizierten Ereignissen

Mit Ausnahme des identifizereignisses hängt der Typ und die Reihenfolge der Ereignisse, die ein Writer empfängt, eindeutig von dem Typ der VSS-Vorgänge ab, die zurzeit fortgeführt werden.

Das Ereignis identifizieren erfordert, dass Writer die Systeminformationen über Ihre Konfiguration und die von Ihnen verwalteten Dateien über das [*Writer-Metadatendokument*](vssgloss-w.md)bereitstellen. Zur Unterstützung von fast jedem VSS-Vorgang wird ein identifizier ungsereignis generiert, einschließlich System Abfragen sowie Schatten Kopien und Sicherungs-und Wiederherstellungs Vorgänge. Daher muss jede Implementierung des identifizierungsereignishandlers [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) eines Writers jederzeit in der Lage sein, ein identifizierungsereignis zu behandeln – einschließlich in der Mitte der Verarbeitung eines anderen VSS-Vorgangs, z. b. einer Sicherung oder Wiederherstellung. Ein identifizier ungsereignis sollte nie als Teil des Lebenszyklus eines VSS-Vorgangs betrachtet werden, auch wenn seine Generierung vor dem Start des Vorgangs erwartet und erforderlich ist.

Es ist besonders wichtig, dass Zustandsinformationen zu einem VSS-Vorgang in [**CVssWriter:: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)nicht geändert werden, da diese Informationen durch den Empfang eines Ereignisses außerhalb der Reihenfolge zurückgesetzt werden.

## <a name="backup-and-restore-events"></a>Sicherungs-und Wiederherstellungs Ereignisse

Abhängig davon, ob Sie an einer Sicherung oder Wiederherstellung teilnimmt, empfängt ein Writer zusätzlich zu einem anfänglichen identifiktereignis zwischen zwei und sieben Ereignissen.

Die Behandlung dieser Ereignisse stellt den Lebenszyklus eines Sicherungs-oder Wiederherstellungs Vorgangs (aus Sicht eines Writers) dar.

Bei einem typischen Sicherungs Vorgang (siehe [Übersicht über die Verarbeitung einer Sicherung unter VSS](overview-of-processing-a-backup-under-vss.md)) behandelt ein Writer die folgenden Ereignisse (zusätzlich zu einem anfänglichen identifizierungsereignis):

-   PrepareForBackup
-   Prepareforsnapshot
-   Freeze
-   Reaktivieren
-   PostSnapshot
-   BackupComplete
-   BackupShutdown

Bei einem typischen Wiederherstellungs Vorgang (siehe [Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](overview-of-processing-a-restore-under-vss.md)) werden die folgenden Ereignisse von einem Writer behandelt:

-   Vorabversion
-   Postrestore

 

 



