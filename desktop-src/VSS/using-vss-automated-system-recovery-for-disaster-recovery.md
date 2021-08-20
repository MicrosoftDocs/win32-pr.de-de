---
description: Eine VSS-Sicherungs- und -Wiederherstellungsanwendung, die die Notfallwiederherstellung durchführt (auch als Bare-Metal-Wiederherstellung bezeichnet), kann den Writer für die automatisierte Systemwiederherstellung (ASR) zusammen mit der Windows-Vorinstallationsumgebung (Windows PE) verwenden, um kritische Volumes und andere Komponenten des startbaren Systemstatus zu sichern und wiederherzustellen. Die Sicherungsanwendung wird als VSS-Anfordernde implementiert.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Verwenden der automatisierten VsS-Systemwiederherstellung für die Notfallwiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813f0f746600fa665ed20bb208f3241cb1a88a12de721d53a8afa77be4a4c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998060"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Verwenden der automatisierten VsS-Systemwiederherstellung für die Notfallwiederherstellung

Eine VSS-Sicherungs- und -Wiederherstellungsanwendung, die die Notfallwiederherstellung durchführt (auch als Bare-Metal-Wiederherstellung bezeichnet), kann den Writer für die automatisierte Systemwiederherstellung (ASR) zusammen mit der Windows-Vorinstallationsumgebung (Windows PE) verwenden, um kritische Volumes und andere Komponenten des startbaren Systemstatus zu sichern und wiederherzustellen. Die Sicherungsanwendung wird als VSS-Anfordernde implementiert.

**Hinweis:**  Anwendungen, die ASR verwenden, müssen Windows PE lizenzen.

**Windows Server 2003 und Windows XP:** ASR ist nicht als VSS Writer implementiert.

Informationen zu Ablaufverfolgungstools, die Sie mit ASR verwenden können, finden Sie unter Verwenden von [Ablaufverfolgungstools mit VSS ASR-Anwendungen.](using-tracing-tools-with-vss-asr-applications.md)

**In diesem Artikel:**

-   [Übersicht über Sicherungsphasenaufgaben](#overview-of-backup-phase-tasks)
-   [Auswählen der zu sichernden kritischen Komponenten](#choosing-which-critical-components-to-back-up)
-   [Übersicht über Wiederherstellungsphasenaufgaben](#overview-of-restore-phase-tasks)
-   [Ausschließen aller Datenträger für ein Volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Übersicht über Sicherungsphasenaufgaben

Zur Sicherungszeit führt der Anfordernde die folgenden Schritte aus.

> [!Note]  
> Alle Schritte sind erforderlich, sofern nicht anders angegeben.

 

1.  Rufen Sie die [**CreateVssBackupComponents-Funktion**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) auf, um eine Instanz der [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) zu erstellen, und rufen Sie die [**IVssBackupComponents::InitializeForBackup-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) auf, um die Instanz zum Verwalten einer Sicherung zu initialisieren.
2.  Rufen [**Sie IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) auf, um den Kontext für den Schattenkopievorgang zu festlegen.
3.  Rufen [**Sie IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) auf, um die Sicherung zu konfigurieren. Legen Sie *den Parameter bBackupBootableSystemState* auf **TRUE fest,** um anzugeben, dass die Sicherung einen startbaren Systemstatus enthält.
4.  Wählen Sie aus, welche kritischen Komponenten im Writer-Metadatendokument des ASR-Writers für jede komponente sichern und [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) aufrufen sollen.
5.  Rufen [**Sie IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) auf, um einen neuen, leeren Schattenkopiesatz zu erstellen.
6.  Rufen [**Sie IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) auf, um einen asynchronen Kontakt mit Writern zu initiieren.
7.  Rufen [**Sie IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) auf, um das Writer-Metadatendokument des ASR-Writers abzurufen. Die Writer-ID für den ASR-Writer ist BE000CBE-11FE-4426-9C58-531AA6355FC4, und die Zeichenfolge für den Writernamen ist "ASR Writer".
8.  Rufen [**Sie IVssExwriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) auf, um eine Kopie des Writer-Metadatendokuments des ASR-Writers zu speichern.
9.  Rufen [**Sie IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) für jedes Volume auf, das an Schattenkopien teilnehmen kann, um das Volume dem Schattenkopiesatz hinzuzufügen.
10. Rufen [**Sie IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) auf, um Writer zu benachrichtigen, sich auf einen Sicherungsvorgang vorzubereiten.
11. Rufen Sie [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (oder [**IVssBackupComponentsEx3::GetWriterStatus)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)auf, um den Status des ASR-Writer zu überprüfen.
12. An diesem Punkt können Sie Fehlermeldungen abfragen, die vom Writer in seiner [**CVssWriter::OnPrepareBackup-Methode festgelegt**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) wurden. Beispielcode, der zeigt, wie diese Nachrichten angezeigt werden, finden Sie unter [**IVssComponentEx::GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Rufen [**Sie IVssBackupComponents::D oSnapshotSet auf,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) um eine Volumeschattenkopie zu erstellen.
14. Rufen [**Sie IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) auf, um den Status des ASR-Writer zu überprüfen.
15. Sichern Sie die Daten.
16. Geben Sie an, ob der Sicherungsvorgang erfolgreich war, indem [**Sie IVssBackupComponents::SetBackupSucceeded aufrufen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)
17. Rufen [**Sie IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) auf, um anzugeben, dass der Sicherungsvorgang abgeschlossen wurde.
18. Rufen [**Sie IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents::GetWriterStatus auf.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) Der Sitzungszustandsspeicher des Writers ist eine begrenzte Ressource, und Writer müssen schließlich Sitzungszustände wiederverwenden. Dieser Schritt markiert den Sicherungssitzungsstatus des Writers als abgeschlossen und benachrichtigt VSS, dass dieser Sicherungssitzungsslot von einem nachfolgenden Sicherungsvorgang wiederverwendet werden kann.
    > [!Note]  
    > Dies ist nur auf Windows Server 2008 mit Service Pack 2 (SP2) und früher erforderlich.

     

19. Rufen [**Sie IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) auf, um eine Kopie des Sicherungskomponentendokuments des Anfordernden zu speichern. Die Informationen im Sicherungskomponentendokument werden zum Zeitpunkt der Wiederherstellung verwendet, wenn der Anfordernde die [**IVssBackupComponents::InitializeForRestore-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) aufruft.

## <a name="choosing-which-critical-components-to-back-up"></a>Auswählen der zu sichernden kritischen Komponenten

In der Initialisierungsphase der Sicherung meldet der ASR-Writer die folgenden Komponententypen im Writer-Metadatendokument:

-   Wichtige Volumes, z. B. start-, system- und Windows Recovery Environment-Volumes (Windows RE) und die Windows RE-Partition, die der instanz von Windows Vista oder Windows Server 2008 zugeordnet ist, die derzeit ausgeführt wird. Ein Volume ist ein *kritisches Volume,* wenn es Systemstatusinformationen enthält. Die Start- und Systemvolumes werden automatisch eingeschlossen. Der Anfordernde muss alle Volumes enthalten, die systemkritische Komponenten enthalten, die von Writern gemeldet werden, z. B. die Volumes, die Active Directory enthalten. Systemkritische Komponenten werden als "für die Sicherung nicht auswählbar" markiert. In VSS bedeutet "Nicht auswählbar" "nicht optional". Daher muss der Anfordernde sie als Teil des Systemstatus sichern. Weitere Informationen finden Sie unter [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md). Komponenten, für die das VSS \_ CF NOT SYSTEM STATE-Flag festgelegt \_ \_ \_ ist, sind nicht systemkritisch.
    > [!Note]  
    > Die ASR-Komponente ist eine systemkritische Komponente, die vom ASR-Writer gemeldet wird.

     

-   Datenträger. Jeder Festplattendatenträger auf dem Computer wird als Komponente in ASR verfügbar gemacht. Wenn ein Datenträger während der Sicherung nicht ausgeschlossen wurde, wird er während der Wiederherstellung zugewiesen und kann neu erstellt und neu formatiert werden. Beachten Sie, dass der Anfordernde während der Wiederherstellung weiterhin einen Datenträger neu erstellen kann, der während der Sicherung ausgeschlossen wurde, indem er die [**IVssBackupComponents::SetRestoreOptions-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) aufruft. Wenn ein Datenträger in einem dynamischen Datenträgerpaket ausgewählt ist, müssen auch alle anderen Datenträger in diesem Paket ausgewählt werden. Wenn ein Volume ausgewählt wird, da es sich um ein kritisches Volume (d. h. ein Volume mit Systemstatusinformationen) handelt, muss auch jeder Datenträger ausgewählt werden, der einen Umfang für dieses Volume enthält. Verwenden Sie den Steuerungscode [**IOCTL \_ VOLUME \_ GET VOLUME DISK \_ \_ \_ EXTENTS,**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) um die Extents für ein Volume zu finden.

    > [!Note]  
    > Während der Sicherung sollte der Anfordernde alle Festplatten enthalten. Wenn der Datenträger, der den Sicherungssatz des Anfordernden enthält, ein lokaler Datenträger ist, sollte dieser Datenträger enthalten sein. Während der Wiederherstellung muss der Anfordernde den Datenträger ausschließen, der den Sicherungssatz des Anfordernden enthält, um zu verhindern, dass er überschrieben wird.

     

    In einer Clusteringumgebung erstellt ASR das Layout der freigegebenen Datenträger des Clusters nicht neu. Diese Datenträger sollten online wiederhergestellt werden, nachdem das Betriebssystem in der Datenbank wiederhergestellt Windows RE.

-   Startkonfigurationsdaten (BCD)-Speicher. Diese Komponente gibt den Pfad des Verzeichnisses an, das den BCD-Speicher enthält. Der Anfordernde muss diese Komponente angeben und alle Dateien im BCD-Speicherverzeichnis sichern. Weitere Informationen zum BCD-Speicher finden Sie unter [Informationen zu BCD.](/previous-versions/windows/desktop/bcd/about-bcd)
    > [!Note]  
    > Auf Computern, die die erweiterte Firmwareschnittstelle (Extended Firmware Interface, EFI) verwenden, ist die EFI-Systempartition (ESP) immer ausgeblendet und kann nicht in einer Volumeschattenkopie enthalten sein. Der Anfordernde muss den Inhalt dieser Partition sichern. Da diese Partition nicht in einer Volumeschattenkopie enthalten sein kann, kann die Sicherung nur über das Live-Volume und nicht über die Schattenkopie ausgeführt werden. Weitere Informationen zu EFI und ESP finden Sie im [Leitfaden zum Einrichten von](/windows-hardware/drivers/bringup/).

Die Komponentennamen verwenden die folgenden Formate:

-   Für Datenträgerkomponenten ist das Format

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    wobei *n* die Datenträgernummer ist. Nur die Datenträgernummer wird aufgezeichnet. Um die Datenträgernummer zu erhalten, verwenden Sie den [**IOCTL \_ STORAGE GET DEVICE \_ \_ \_ NUMBER-Steuerungscode.**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number)

-   Für Volumekomponenten ist das Format

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    Dabei *ist GUID* die Volume-GUID.

-   Für die BCD-Speicherkomponente ist das Format

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Wenn die Systempartition über einen Volume-GUID-Namen verfügt, kann diese Komponente ausgewählt werden. Andernfalls ist sie nicht auswählbar.

    > [!Note]  
    > ASR fügt die Dateien der Dateigruppe der BCD-Speicherkomponente wie folgt hinzu:
    >
    > -   Für EFI-Datenträger fügt ASR hinzu.
    >
    >     *SystemPartitionPath* \\ EFI \\ Microsoft \\ Boot \\ \* .\*
    >
    >     Dabei *ist SystemPartitionPath* der Pfad zur Systempartition.
    >
    > -   Für GPT-Datenträger fügt ASR hinzu.
    >
    >     *SystemPartitionPath* \\ Starten Sie \\ \* .\*
    >
    >     Dabei *ist SystemPartitionPath* der Pfad zur Systempartition.
    >
    > -   Den Systempartitionspfad finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **Setup** \\ **SystemPartition**

     

Bei der Wiederherstellung müssen alle Komponenten, die als kritische Volumes gekennzeichnet sind, wiederhergestellt werden. Wenn mindestens ein kritisches Volumes nicht wiederhergestellt werden kann, schlägt der Wiederherstellungsvorgang fehl.

In der [**PreRestore-Phase**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) der Wiederherstellungssequenz werden Datenträger, die während der Sicherung nicht ausgeschlossen wurden, standardmäßig neu erstellt und neu formatiert. Sie werden jedoch nicht neu erstellt oder neu formatiert, wenn sie die folgenden Bedingungen erfüllen:

-   Ein Basisdatenträger wird nicht neu erstellt, wenn sein Datenträgerlayout intakt ist oder nur additive Änderungen vorgenommen wurden. Das Datenträgerlayout ist intakt, wenn die folgenden Bedingungen erfüllt sind:
    -   Die Datenträgersignatur, der Datenträgerstil (GPT oder MBR), die Logische Sektorgröße und der Volumestartoffset werden nicht geändert.
    -   Die Volumegröße wird nicht verringert.
    -   Bei GPT-Datenträgern wird der Partitionsbezeichner nicht geändert.
-   Ein dynamischer Datenträger wird nicht neu erstellt, wenn sein Datenträgerlayout intakt ist oder nur additive Änderungen vorgenommen wurden. Damit ein dynamischer Datenträger intakt ist, müssen alle Bedingungen für einen Basisdatenträger erfüllt sein. Darüber hinaus muss die Volumestruktur des gesamten Datenträgerpakets intakt sein. Die Volumestruktur des Datenträgerpakets ist intakt, wenn die folgenden Bedingungen erfüllt sind, die sowohl für MBR- als auch für GPT-Datenträger gelten:
    -   Die Anzahl der Volumes, die während der Wiederherstellung im physischen Paket verfügbar sind, muss größer oder gleich der Anzahl der Volumes sein, die während der Sicherung in den ASR Writer-Metadaten angegeben wurden.
    -   Die Anzahl der [*Plexes pro*](../vds/virtual-disk-service-glossary-all.md) Volume muss unverändert bleiben.
    -   Die Anzahl der [*Elemente*](../vds/virtual-disk-service-glossary-all.md) muss unverändert bleiben.
    -   Die Anzahl der physischen Datenträger-Extent muss größer sein als die Anzahl der Datenträger-Extent, die in den ASR Writer-Metadaten angegeben sind.
    -   Ein intaktes Paket bleibt intakt, wenn zusätzliche Volumes hinzugefügt werden oder wenn ein Volume im Paket erweitert wird (z. B. von einem einfachen Volume auf ein übergreifendes Volume).
        > [!Note]  
        > Wenn ein einfaches Volume gespiegelt wird, ist das Paket nicht intakt und wird neu erstellt, um sicherzustellen, dass der BCD- und Startvolumenstatus nach der Wiederherstellung konsistent bleiben. Wenn Volumes gelöscht werden, wird das Paket neu erstellt.

         
-   Wenn die Volumestruktur des dynamischen Datenträgerpakets intakt ist und nur additive Änderungen vorgenommen wurden, werden die Datenträger im Paket nicht neu erstellt.

    **Windows Vista:** Dynamische Datenträger werden immer neu erstellt. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) geändert hat.

Vor Beginn der Wiederherstellungsphase kann der Anfordernde jederzeit angeben, dass die Datenträger schnell formatiert werden sollen, indem der **Registrierungsschlüssel HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** festgelegt wird. Unter diesem Schlüssel befindet sich ein Wert namens **QuickFormat** mit dem Datentyp REG \_ DWORD. Wenn dieser Wert nicht vorhanden ist, sollten Sie ihn erstellen. Legen Sie die Daten des **QuickFormat-Werts** für die schnelle Formatierung auf 1 oder für langsame Formatierung auf 0 fest.

Wenn der **QuickFormat-Wert** nicht vorhanden ist, werden die Datenträger langsam formatiert.

Die schnelle Formatierung ist deutlich schneller als die langsame Formatierung (auch als vollständige Formatierung bezeichnet). Die schnelle Formatierung überprüft jedoch nicht jeden Sektor auf dem Volume.

## <a name="overview-of-restore-phase-tasks"></a>Übersicht über Wiederherstellungsphasenaufgaben

Zur Wiederherstellungszeit führt der Anfordernde die folgenden Schritte aus:

> [!Note]  
> Alle Schritte sind erforderlich, sofern nicht anders angegeben.

 

1.  Rufen Sie die [**CreateVssBackupComponents-Funktion**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) auf, um eine Instanz der [**IVssBackupComponents-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) zu erstellen, und rufen Sie die [**IVssBackupComponents::InitializeForRestore-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) auf, um die Instanz für die Wiederherstellung zu initialisieren, indem Sie das Sicherungskomponentendokument des Anfordernden in die Instanz laden.
2.  \[Dieser Schritt ist nur erforderlich, wenn der Anfordernde ändern muss, ob "IncludeDisk" oder "ExcludeDisk" für einen oder mehrere Datenträger angegeben ist. \] Rufen [**Sie IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) auf, um die Wiederherstellungsoptionen für die ASR Writer-Komponenten zu festlegen. Der ASR Writer unterstützt die folgenden Optionen: Mit "IncludeDisk" kann der Anfordernde einen Datenträger auf dem Zielsystem enthalten, der für die Wiederherstellung in Betracht gezogen werden kann, auch wenn er während der Sicherungsphase nicht ausgewählt wurde. Mit "ExcludeDisk" kann der Anfordernde verhindern, dass ein Datenträger auf dem Zielsystem neu erstellt wird. Beachten Sie Folgendes: Wenn "ExcludeDisk" für einen Datenträger angegeben wird, der ein kritisches Volume enthält, kann der nachfolgende Aufruf von [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) nicht mehr verwendet werden.

    Im folgenden Beispiel wird gezeigt, wie [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) verwendet wird, um zu verhindern, dass Datenträger 0 und Datenträger 1 neu erstellt werden, und treiber von Drittanbietern in das wiederhergestellte Startvolumen einjizieren.

    **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Die Einjektion von Treibern von Drittanbietern wird nicht unterstützt.

    Im Beispiel wird davon ausgegangen, dass der [**IVssBackupComponents-Zeiger**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) m \_ pBackupComponents gültig ist.

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    Informationen zum Ausschließen aller Datenträger für ein angegebenes Volume finden Sie unter "Ausschließen aller Datenträger für ein Volume".

3.  Rufen [**Sie IVssBackupComponents::P reRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) auf, um den ASR Writer zu benachrichtigen, sich auf einen Wiederherstellungsvorgang vorzubereiten. Rufen [**Sie IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) so oft wie nötig auf, bis der im *pHrResult-Parameter* zurückgegebene Statuswert nicht VSS \_ S \_ ASYNC PENDING \_ ist.
4.  Stellen Sie die Daten wieder her. In der Wiederherstellungsphase konfiguriert ASR den Volume-GUID-Pfad neu ( \\ \\ ? \\ Volume{GUID}) für jedes Volume, das mit dem Volume-GUID-Pfad übereinstimmen soll, der während der Sicherungsphase verwendet wurde. Laufwerkbuchstaben werden jedoch nicht beibehalten, da dies zu Kollisionen mit den Laufwerkbuchstaben führen würde, die automatisch in der Wiederherstellungsumgebung zugewiesen werden. Daher muss der Anfordernde beim Wiederherstellen von Daten Volume-GUID-Pfade und keine Laufwerkbuchstaben verwenden, um auf die Volumes zu zugreifen.
5.  Legen Sie **den Registrierungsschlüssel HKLM** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** fest, um den Satz von Volumes anzugeben, die wiederhergestellt oder neu formatiert wurden.

    Unter diesem Schlüssel befindet sich ein Wert namens **RestoredVolumes** mit dem Datentyp REG \_ MULTI \_ SZ. Wenn dieser Wert nicht vorhanden ist, sollten Sie ihn erstellen. Unter diesem Wert sollte der Anfordernde einen Volume-GUID-Eintrag für jedes Volume erstellen, das wiederhergestellt wurde. Dieser Eintrag sollte das folgende Format haben: \\ \\ ? \\ Volume{78618c8f-aefd-11da-a898-806e6f6e6963}. Bei jeder Bare-Metal-Wiederherstellung legt ASR den **RestoredVolumes-Wert** auf den Satz von Volumes fest, die von ASR wiederhergestellt wurden. Wenn der Anfordernde zusätzliche Volumes wiederhergestellt hat, sollte er diesen Wert auf die Vereinigung der Volumes festlegen, die der Anfordernde wiederhergestellt hat, und der Gruppe von Volumes, die ASR wiederhergestellt hat. Wenn der Anfordernde ASR nicht verwendet hat, sollte er die Liste der Volumes ersetzen.

    Sie sollten auch einen Wert namens **LastInstance mit** dem Datentyp REG \_ SZ erstellen. Dieser Schlüssel sollte ein zufälliges Cookie enthalten, das den aktuellen Wiederherstellungsvorgang eindeutig identifiziert. Ein solches Cookie kann mithilfe der [**Funktionen UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) und [**UuidToString erstellt**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) werden. Jedes Mal, wenn eine Bare-Metal-Wiederherstellung durchgeführt wird, setzt ASR diesen Registrierungswert zurück, um Anfordernde und Nicht-VSS-Sicherungsanwendungen darüber zu benachrichtigen, dass die Wiederherstellung erfolgt ist.

6.  Rufen [**Sie IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) auf, um das Ende des Wiederherstellungsvorgang anzugeben. Rufen [**Sie IVssAsync::QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) so oft wie nötig auf, bis der im *pHrResult-Parameter* zurückgegebene Statuswert nicht VSS \_ S \_ ASYNC PENDING \_ ist.

In der Wiederherstellungsphase kann ASR Partitionen erstellen oder entfernen, um den vorherigen Zustand des Computers wiederherzustellen. Anfordernde Dürfen nicht versuchen, Datenträgernummern aus der Sicherungsphase der Wiederherstellungsphase zu zuordnen.

Bei der Wiederherstellung muss der Anfordernde den Datenträger ausschließen, der den Sicherungssatz des Anfordernden enthält. Andernfalls kann der Sicherungssatz durch den Wiederherstellungsvorgang überschrieben werden.

Bei der Wiederherstellung wird ein Datenträger ausgeschlossen, wenn er während der Sicherung nicht als Komponente ausgewählt wurde, oder wenn er explizit durch Aufrufen von [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) mit der Option "ExcludeDisk" während der Wiederherstellung ausgeschlossen wird.

Beachten Sie, dass während der WinPE-Notfallwiederherstellung asr writer-Funktionen vorhanden sind, aber keine anderen Writer verfügbar sind und der VSS-Dienst nicht ausgeführt wird. Nachdem die WinPE-Notfallwiederherstellung abgeschlossen ist, der Computer neu gestartet wurde und das Windows-Betriebssystem normal ausgeführt wird, kann der VSS-Dienst gestartet werden, und der Anfordernde kann alle zusätzlichen Wiederherstellungsvorgänge ausführen, bei denen andere Writer als der ASR Writer teilnehmen müssen.

Wenn die Sicherungsanwendung während der Wiederherstellungssitzung erkennt, dass die eindeutigen Volume-IDs unverändert sind und daher alle Volumes ab dem Zeitpunkt der Sicherung vorhanden und in WinPE intakt sind, kann die Sicherungsanwendung nur den Inhalt der Volumes wiederherstellen, ohne ASR zu verwenden. In diesem Fall sollte die Sicherungsanwendung angeben, dass der Computer wiederhergestellt wurde, indem der folgende Registrierungsschlüssel im wiederhergestellten Betriebssystem angegeben wird: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

Geben Sie unter diesem Schlüssel **LastInstance** für den Wertnamen, REG SZ für den Werttyp und ein zufälliges Cookie (z. B. eine von der \_ [**UuidCreate-Funktion**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) erstellte GUID) für die Wertdaten an.

Wenn die Sicherungsanwendung während der Wiederherstellungssitzung erkennt, dass ein oder mehrere Volumes geändert wurden oder fehlen, sollte die Sicherungsanwendung ASR verwenden, um die Wiederherstellung durchzuführen. ASR erstellt die Volumes genau wie zum Zeitpunkt der Sicherung neu und setzt den **RestoreSession-Registrierungsschlüssel** fest.

## <a name="excluding-all-disks-for-a-volume"></a>Ausschließen aller Datenträger für ein Volume

Das folgende Beispiel zeigt, wie alle Datenträger für ein angegebenes Volume ausgeschlossen werden.


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
