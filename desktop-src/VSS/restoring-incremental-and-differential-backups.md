---
description: Das Wiederherstellen einer inkrementellen oder differenziellen Sicherung unter VSS ist nicht wesentlich von anderen VSS-Wiederherstellungsvorgangen.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Wiederherstellen inkrementeller und differenzieller Sicherungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcc0c2df57e2f7c0f21436248ddaa46231c7bf6440c76a38f4d1c92ab2adf97f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864050"
---
# <a name="restoring-incremental-and-differential-backups"></a>Wiederherstellen inkrementeller und differenzieller Sicherungen

Das Wiederherstellen einer inkrementellen oder differenziellen Sicherung unter VSS ist nicht wesentlich von anderen VSS-Wiederherstellungsvorgangen.

Ein Writer kann Wiederherstellungsziele oder anforderungsgesteuerte Zielgruppenadressierungen ändern, und ein An anfordernde Benutzer muss wie bei jeder anderen Wiederherstellung alternative Speicherortzuordnungen und neue Ziele verarbeiten. Es gibt jedoch zwei wichtige Probleme, die bei der Wiederherstellung einer inkrementellen oder differenziellen Sicherung zu beachten sind: zusätzliche Wiederherstellungen und Sicherungsstempel.

## <a name="additional-restores"></a>Zusätzliche Wiederherstellungen

Das erste Problem besteht in zusätzlichen Wiederherstellungen. Ein Sicherungsoperator muss möglicherweise mehrere Wiederherstellungsvorgänge ausführen, indem er ein erstes vollständiges und nachfolgendes inkrementelles oder differenzielles Sicherungsmedium als Quelle verwendet.

Einige Writer verwenden in der Regel im Rahmen der Verarbeitung eines [*PostRestore-Ereignisses*](vssgloss-p.md) mit [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)wiederhergestellte Dateien, um Aktualisierungen von Daten durchzuführen, die derzeit auf dem Datenträger gespeichert sind. Für einige dieser Writer ist es ineffizient oder gefährlich, wiederholt Datenträgerdaten aus wiederhergestellten Dateien zu aktualisieren.

Daher ist es wichtig, dass Sicherungsanwendungen angeben, wann eine Komponente oder ein Komponentensatz nachfolgende Wiederherstellungen erfordern kann, indem [**IVssBackupComponents::SetAdditionalRestores aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)

Ein Writer würde [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) aufrufen, um zu bestimmen, ob der Sicherungsoperator weitere Wiederherstellungen des Komponenten- oder Komponentensets geplant hat.

Wenn der Anfordernde [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores)nicht aufgerufen hat, gibt [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) false zurück, und der Writer kann jede verarbeitung nach der Wiederherstellung durchführen, die er benötigt.

Wenn [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) aufgerufen wurde, gibt [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) **true** zurück, und ein Writer sollte entscheiden, wie Vorgänge nach der Wiederherstellung behandelt werden sollen. Beispielsweise kann der Writer seine Daten auf dem Datenträger nicht aktualisieren.

## <a name="backup-stamps"></a>Sicherungsstempel

Im Rahmen des vorherigen vollständigen Sicherungsvorgang hat ein Writer möglicherweise einen Sicherungsstempel im Sicherungskomponentendokument des Anfordernden gespeichert.

Der Sicherungsstempel wird als Zeichenfolge gespeichert, und das Format und die Informationen sind für den Anfordernden nicht verständlich. Daher kann der Anfordernde die Informationen zum Sicherungsstempel nicht direkt verwenden.

Stattdessen besteht die Aufgabe darin, diese Informationen dem Writer zur Verfügung zu stellen, indem die [**IVssBackupComponents::SetPreviousBackupStamp-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) vor der Generierung eines [**PrepareForBackup-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) für eine inkrementelle Sicherung aufruft.

Der Anfordernde führt dies komponentenspezifischen Ausklang aus. Eine Anfordernde untersucht gespeicherte Komponenten- oder Komponentensatz-Sicherungsstempelinformationen mithilfe von [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Wenn sicherungsstempelinformationen für den Wiederherstellungstyp geeignet sind, den der Anfordernde durchführen soll, macht er ihn als Zeitstempel der letzten Sicherung einer Komponente mit der [**IVssBackupComponents::SetPreviousBackupStamp-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) verfügbar.

Ein Writer stellt die Sicherungsstempelinformationen mithilfe von [**IVssComponent::GetPreviousBackupStamp wieder her.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp) Ein Writer dieser Klasse hat den anfänglichen Sicherungsstempel generiert, sodass der Writer diesen Stempel decodieren und die Informationen verwenden kann. Basierend darauf kann ein Writer bei der Behandlung eines [**PreRestore-Ereignisses**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) aktionen wie das Ändern von Wiederherstellungszielen oder das Anfordern einer gezielten Zielgruppenadressierung durchführen.

 

 



