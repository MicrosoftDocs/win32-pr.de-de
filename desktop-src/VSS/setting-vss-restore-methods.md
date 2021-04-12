---
description: Die Konfiguration von Wiederherstellungs Vorgängen beginnt tatsächlich während der Datensicherung, wenn Writer in ihren Writer-Metadatendokumenten angeben, wie Ihre Daten wieder hergestellt werden sollen.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Festlegen von VSS-Wiederherstellungsmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412cb699fb791a973e280f63fec03bd2854ccd1d
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104218911"
---
# <a name="setting-vss-restore-methods"></a>Festlegen von VSS-Wiederherstellungsmethoden

Die Konfiguration von Wiederherstellungs Vorgängen beginnt tatsächlich während der Datensicherung, wenn Writer in ihren Writer-Metadatendokumenten angeben, wie Ihre Daten wieder hergestellt werden sollen.

Diese Spezifikationen, die als [*Wiederherstellungsmethoden*](vssgloss-r.md) oder ursprüngliche [*Wiederherstellungs Ziele*](vssgloss-r.md)bezeichnet werden, können während der Wiederherstellung durch Writer geändert werden, indem neue Wiederherstellungs Ziele festgelegt werden oder wenn anfordernde Personen an neuen Speicherorten wieder hergestellt werden (siehe [nicht standardmäßige Sicherungs-und Wiederherstellungs](non-default-backup-and-restore-locations.md)Pfade

Durch den Aufruf von [**ivsscreateschreitermetadata:: abtrestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)gibt ein Writer an, welche Wiederherstellungsmethode in seinem Writer-Metadatendokument verwendet werden soll. Die Restore-Methode wird als Writer breit festgelegt und auf alle Dateien in allen von einem Writer verwalteten Komponenten angewendet.

Ein Anforderer erhält diese Informationen (und muss Sie berücksichtigen), indem [**ivssexamineschreitermetadata:: getrestoremethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)aufgerufen wird.

Die Restore-Methode wird durch eine [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) -Enumeration definiert, die an [**ivsskreateschreitermetadata:: abtrestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) übergeben und von [**ivssexamineschreitermetadata:: getrestoremethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)zurückgegeben wird.

Das Writer-Metadatendokument unterstützt die folgenden gültigen Wiederherstellungsmethoden (eine Wiederherstellungsmethode von VSS \_ RME ist \_ undefiniert und weist auf einen Schreiber Fehler hin) In den Abbildungen wird zusammengefasst, wie die verschiedenen unterstützten und definierten Wiederherstellungsmethoden implementiert werden sollten (VSS \_ RME \_ Custom hat keine Abbildung, da sie definitionsgemäß für den Writer spezifisch ist und den jeweiligen Writer-APIs und-Dokumentationen folgen muss):

-   VSS \_ RME \_ Restore, wenn dies nicht der Fall \_ ist \_ \_ . Stellen Sie Komponenten Dateien auf dem Datenträger wieder her, wenn sich keine der Dateien bereits auf dem Datenträger befinden. Der Ziel Dateistatus sollte nach einem [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Ereignis geprüft werden.
    ![Diagramm, das eine Problem Behandlungs Struktur für VSS_RME_RESTORE_IF_NOT_THERE zeigt.](images/rint.png)
-   VSS \_ RME \_ Restore, \_ Wenn von \_ ersetzt werden kann \_ . Stellen Sie Dateien auf dem Datenträger wieder her, wenn alle Dateien ersetzt werden können. Der Ziel Dateistatus sollte nach einem [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Ereignis geprüft werden.
    ![Diagramm, das eine Problem Behandlungs Struktur für VSS_RME_RESTORE_IF_CAN_REPLACE zeigt.](images/ricr.png)
-   der VSS- \_ RME \_ beendet die \_ Wiederherstellung \_ . Ein Dienst wird beendet, bevor die Dateien wieder hergestellt werden.
    ![Diagramm, das eine Problem Behandlungs Struktur für VSS_RME_STOP_RESTORE_START zeigt.](images/srr.png)
-   VSS- \_ RME \_ \_ an einem \_ Alternativen \_ Speicherort wiederherstellen. Wiederherstellen von Dateien auf einem Datenträger an einem alternativen Speicherort. Die alternativen Speicherort Zuordnungen werden im Writer-Metadatendokument angegeben.
    ![Diagramm, das eine Problem Behandlungs Struktur für VSS_RME_RESTORE_TO_ALTERNATE_LOCATION zeigt.](images/rtal.png)
-   VSS- \_ RME- \_ Wiederherstellung \_ beim \_ Neustart. Bewirkt, dass Dateien wieder hergestellt (überschrieben) werden, wenn der Computer neu gestartet wird.
    ![Diagramm, das eine Problem Behandlungs Struktur für VSS_RME_RESTORE_AT_REBOOT zeigt.](images/rar.png)
-   VSS- \_ RME- \_ Wiederherstellung \_ beim \_ Neustart, \_ Wenn \_ nicht \_ ersetzen kann. Wenn eine Datei nicht auf dem Datenträger auf einem laufenden System wieder hergestellt werden konnte, wird Sie beim Neustart des Computers wieder hergestellt (überschrieben).
    ![Diagramm, das eine Problem Behandlungs Struktur forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE zeigt. ](images/raricr.png)
-   VSS- \_ RME \_ Benutzer definiert. Keine der vordefinierten Methoden funktioniert. die Sicherungs Anwendung muss spezielle APIs verwenden, um den Wiederherstellungs Vorgang auszuführen. Bei dieser Sicherungsmethode muss der Anforderer den fraglichen Writer vollständig verstehen. Siehe [spezielle VSS-Verwendungs Fälle](special-vss-usage-cases.md) für derzeit unterstützte Instanzen.

 

 



