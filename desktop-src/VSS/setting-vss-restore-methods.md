---
description: Die Konfiguration von Wiederherstellungsvorgängen beginnt tatsächlich während der Datensicherung, wenn Writer in ihren WriterMetadatendokumenten angeben, wie ihre Daten wiederhergestellt werden sollen.
ms.assetid: b1f948cd-d3b0-4637-b76d-b54a74bb5948
title: Festlegen von VSS-Wiederherstellungsmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f7b0d138555b1e10dba55483c694c08a649e97e59cb66ed65c1a276187d3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751726"
---
# <a name="setting-vss-restore-methods"></a>Festlegen von VSS-Wiederherstellungsmethoden

Die Konfiguration von Wiederherstellungsvorgängen beginnt tatsächlich während der Datensicherung, wenn Writer in ihren WriterMetadatendokumenten angeben, wie ihre Daten wiederhergestellt werden sollen.

Diese Spezifikationen, die entweder als [*Wiederherstellungsmethoden*](vssgloss-r.md) oder ursprüngliche [*Wiederherstellungsziele*](vssgloss-r.md)bezeichnet werden, können während der Wiederherstellung durch Writer, die neue Wiederherstellungsziele festlegen, oder durch Anfordernde geändert werden, die neue Speicherorte wiederherstellen (siehe [Nicht standardmäßige Sicherungs- und Wiederherstellungsspeicherorte).](non-default-backup-and-restore-locations.md)

Durch Aufrufen von [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod)gibt ein Writer an, welche Wiederherstellungsmethode im Writer Metadata Document verwendet werden soll. Die Wiederherstellungsmethode wird schreibgeweitet festgelegt und auf alle Dateien in allen Komponenten angewendet, die von einem Writer verwaltet werden.

Ein Anforderer ruft diese Informationen ab (und muss diese berücksichtigen), indem [**er IVssExmostWriterMetadata::GetRestoreMethod aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)

Die Wiederherstellungsmethode wird durch eine [**VSS \_ \_ RESTOREMETHOD-ENUM-Enumeration**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) definiert, die an [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) übergeben und von [**IVssExfiltrWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)zurückgegeben wird.

Das Writer Metadata Document unterstützt die folgenden gültigen Wiederherstellungsmethoden (eine Wiederherstellungsmethode von VSS \_ RME \_ UNDEFINED weist auf einen Writerfehler hin). Die Abbildungen fassen zusammen, wie die verschiedenen unterstützten und definierten Wiederherstellungsmethoden implementiert werden sollen (VSS \_ RME \_ CUSTOM ist keine Abbildung zugeordnet, da sie definitionsgemäß spezifisch für den Writer ist und den spezifischen Writer-APIs und der Dokumentation folgen muss):

-   VSS \_ RME \_ \_ RESTORE, FALLS \_ NICHT \_ VORHANDEN. Stellen Sie Komponentendateien auf dem Datenträger wieder her, wenn sich keine der Dateien bereits auf dem Datenträger befindet. Der Zieldateistatus sollte nach einem [**PreRestore-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) überprüft werden.
    ![Diagramm, das eine Problembehandlungsstruktur für VSS_RME_RESTORE_IF_NOT_THERE zeigt.](images/rint.png)
-   VSS \_ RME \_ \_ RESTORE, WENN \_ ERSETZT WERDEN \_ KANN. Stellen Sie Dateien auf dem Datenträger wieder her, wenn alle Dateien ersetzt werden können. Der Zieldateistatus sollte nach einem [**PreRestore-Ereignis**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) überprüft werden.
    ![Diagramm, das eine Problembehandlungsstruktur für VSS_RME_RESTORE_IF_CAN_REPLACE zeigt.](images/ricr.png)
-   VSS \_ RME \_ BEENDET DEN \_ WIEDERHERSTELLUNGSSTART. \_ Ein Dienst wird vor dem Wiederherstellen der Dateien beendet.
    ![Diagramm, das eine Problembehandlungsstruktur für VSS_RME_STOP_RESTORE_START zeigt.](images/srr.png)
-   VSS \_ RME RESTORE TO ALTERNATE LOCATION (VSS RME-WIEDERHERSTELLUNG \_ AN EINEM ALTERNATIVEN \_ \_ \_ SPEICHERORT). Stellen Sie Dateien an einem alternativen Speicherort auf dem Datenträger wieder her. Die alternativen Speicherortzuordnungen werden im Writer Metadata Document angegeben.
    ![Diagramm, das eine Problembehandlungsstruktur für VSS_RME_RESTORE_TO_ALTERNATE_LOCATION zeigt.](images/rtal.png)
-   VSS \_ RME RESTORE AT REBOOT (VSS RME-WIEDERHERSTELLUNG \_ BEIM \_ \_ NEUSTART). Bewirkt, dass Dateien wiederhergestellt (überschrieben) werden, wenn der Computer neu gestartet wird.
    ![Diagramm, das eine Problembehandlungsstruktur für VSS_RME_RESTORE_AT_REBOOT zeigt.](images/rar.png)
-   VSS \_ RME \_ RESTORE AT REBOOT IF CANNOT REPLACE (VSS RME-WIEDERHERSTELLUNG \_ BEIM \_ \_ NEUSTART, WENN NICHT ERSETZT WERDEN \_ \_ KANN). Wenn eine Datei auf einem ausgeführten System nicht auf dem Datenträger wiederhergestellt werden konnte, wird sie beim Neustart des Computers wiederhergestellt (überschrieben).
    ![Diagramm, das eine Problembehandlungsstruktur forVSS_RME_RESTORE_AT_REBOOT_IF_CANNOT_REPLACE zeigt. ](images/raricr.png)
-   VSS \_ RME \_ CUSTOM. Keine der vordefinierten Methoden funktioniert. Die Sicherungsanwendung muss spezialisierte APIs verwenden, um den Wiederherstellungsvorgang auszuführen. Für diese Sicherungsmethode muss der Anforderer den betreffenden Writer vollständig verstehen. Informationen zu derzeit unterstützten Instanzen finden Sie unter [Spezielle VSS-Anwendungsfälle.](special-vss-usage-cases.md)

 

 



