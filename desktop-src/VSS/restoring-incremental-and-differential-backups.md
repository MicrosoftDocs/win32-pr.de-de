---
description: Die Wiederherstellung einer inkrementellen oder differenziellen Sicherung unter VSS unterscheidet sich nicht wesentlich von anderen VSS-Wiederherstellungs Vorgängen
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Inkrementelle und differenzielle Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528703"
---
# <a name="restoring-incremental-and-differential-backups"></a>Inkrementelle und differenzielle Sicherungen

Die Wiederherstellung einer inkrementellen oder differenziellen Sicherung unter VSS unterscheidet sich nicht wesentlich von anderen VSS-Wiederherstellungs Vorgängen

Ein Writer kann Wiederherstellungs Ziele ändern oder die Ziel Adressieren von Anforderungen ändern, und ein Anforderer muss Alternative Speicherort Zuordnungen und neue Ziele wie jede andere Wiederherstellung verarbeiten. Es gibt jedoch zwei wichtige Probleme, die bei der Behandlung der Wiederherstellung einer inkrementellen oder differenziellen Sicherung zu beachten sind: zusätzliche Wiederherstellungen und Sicherungs Stempel.

## <a name="additional-restores"></a>Weitere Wiederherstellungen

Das erste Problem ist die zusätzliche Wiederherstellung. Ein Sicherungs Operator muss möglicherweise mehrere Wiederherstellungs Vorgänge mithilfe eines anfänglichen vollständigen und nachfolgenden inkrementellen oder differenziellen Sicherungs Mediums als Quelle ausführen.

Einige Writer (in der Regel als Teil ihrer Behandlung eines [*postrestore*](vssgloss-p.md) -Ereignisses mit [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)) verwenden wiederhergestellte Dateien, um Updates der aktuell auf dem Datenträger gespeicherten Daten auszuführen. Für einige dieser Writer ist es ineffizient – oder gefährlich –, Daten auf dem Datenträger wiederholt aus wiederhergestellten Dateien zu aktualisieren.

Daher ist es wichtig, dass Sicherungs Anwendungen angeben, wenn eine Komponente oder ein Komponenten Satz nachfolgende Wiederherstellungen erfordern, indem [**IVssBackupComponents:: setadditionalbackups**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)aufgerufen wird.

Ein Writer würde [**IVssComponent:: getadditionalbackups**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) aufrufen, um zu bestimmen, ob der Sicherungs Operator eine größere Anzahl von Wiederherstellungen der Komponente oder des Komponenten Satzes geplant hat.

Wenn der Anforderer nicht [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)aufgerufen hat, gibt [**IVssComponent:: getadditionalrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) false zurück, und der Writer kann jede Verarbeitung nach der Wiederherstellung ausführen, die benötigt wird.

Wenn [**IVssBackupComponents:: setadditionalrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) aufgerufen wurde, gibt [**IVssComponent:: getadditionalrestore**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) den Wert **true** zurück, und ein Writer sollte entscheiden, wie nach der Wiederherstellung gearbeitet werden soll – beispielsweise kann der Writer seine Daten auf dem Datenträger nicht aktualisieren.

## <a name="backup-stamps"></a>Sicherungs Stempel

Im Rahmen des vorherigen vollständigen Sicherungs Vorgangs hat ein Writer möglicherweise einen Sicherungs Stempel im Dokument mit den Sicherungs Komponenten der Anforderer gespeichert.

Der Sicherungs Stempel wird als Zeichenfolge gespeichert, und sein Format und seine Informationen sind für den Anforderer nicht verständlich. Daher kann der Anforderer die Sicherungs Stempel Informationen nicht direkt verwenden.

Stattdessen besteht seine Aufgabe darin, diese Informationen für den Writer verfügbar zu machen, indem die [**IVssBackupComponents:: setpreviousbackupstamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) -Methode vor der Generierung eines [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) -Ereignisses für eine inkrementelle Sicherung aufgerufen wird.

Der Anforderer führt dies Komponenten Weise aus. Ein Anforderer überprüft gespeicherte Komponenten-oder Komponenten Sicherungs Stempel Informationen mithilfe von [**IVssComponent:: getbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Wenn Sicherungs Stempel Informationen für die Art der Wiederherstellung geeignet sind, die der Anforderer unternimmt, wird er als Zeitstempel der letzten Sicherung einer Komponente mit der [**IVssBackupComponents:: setpreviousbackupstamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) -Methode zur Verfügung gestellt.

Ein Writer stellt die Sicherungs Stempel Informationen mithilfe von [**IVssComponent:: getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)wieder her. Ein Writer dieser Klasse hat den ersten Sicherungs Stempel generiert, sodass der Writer diesen Stempel decodieren und die Informationen verwenden kann. Basierend darauf kann ein Writer bei der Verarbeitung eines [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Diensts Aktionen ausführen, z. b. das Ändern von Wiederherstellungs Zielen oder das Anfordern einer gerichteten Ziel adressierenden adressieren.

 

 



