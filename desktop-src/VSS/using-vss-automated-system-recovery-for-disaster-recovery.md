---
description: Eine VSS-Sicherungs-und-Wiederherstellungs Anwendung, die eine Notfall Wiederherstellung durchführt (auch als Bare-Metal-Recovery bezeichnet), kann den ASR-Writer (Automated System Recovery) mit Windows Preinstallation Environment (Windows PE) zum Sichern und Wiederherstellen kritischer Volumes und anderer Komponenten des Start fähigen System Status verwenden. Die Sicherungs Anwendung wird als VSS-Anforderer implementiert.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Verwenden der automatisierten VSS-System Wiederherstellung für die Notfall Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e31ef8ba223f40928e2422fa92240656f94592d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347769"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Verwenden der automatisierten VSS-System Wiederherstellung für die Notfall Wiederherstellung

Eine VSS-Sicherungs-und-Wiederherstellungs Anwendung, die eine Notfall Wiederherstellung durchführt (auch als Bare-Metal-Recovery bezeichnet), kann den ASR-Writer (Automated System Recovery) mit Windows Preinstallation Environment (Windows PE) zum Sichern und Wiederherstellen kritischer Volumes und anderer Komponenten des Start fähigen System Status verwenden. Die Sicherungs Anwendung wird als VSS-Anforderer implementiert.

**Hinweis**  Anwendungen, die ASR verwenden, müssen Windows PE lizenzieren.

**Windows Server 2003 und Windows XP:** ASR ist nicht als VSS Writer implementiert.

Informationen zu den Ablauf Verfolgungs Tools, die Sie mit ASR verwenden können, finden Sie unter Verwenden von Ablauf [Verfolgungs Tools mit VSS ASR-Anwendungen](using-tracing-tools-with-vss-asr-applications.md).

**In diesem Artikel:**

-   [Übersicht über Sicherungs Phasen Tasks](#overview-of-backup-phase-tasks)
-   [Auswählen der zu sichernden kritischen Komponenten](#choosing-which-critical-components-to-back-up)
-   [Übersicht über Wiederherstellungs Phasen Tasks](#overview-of-restore-phase-tasks)
-   [Ausschließen aller Datenträger für ein Volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Übersicht über Sicherungs Phasen Tasks

Zum Zeitpunkt der Sicherung führt der Anforderer die folgenden Schritte aus.

> [!Note]  
> Alle Schritte sind erforderlich, sofern nicht anders angegeben.

 

1.  Rufen Sie die Funktion " [**foratevssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) " auf, um eine Instanz der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle zu erstellen, und rufen Sie die [**IVssBackupComponents:: initializeforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) -Methode auf, um die Instanz zum Verwalten einer Sicherung zu initialisieren.
2.  Nennen Sie [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) , um den Kontext für den Schattenkopievorgang festzulegen.
3.  Nennen Sie [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) , um die Sicherung zu konfigurieren. Legen Sie den Parameter " *bbackupbootablesystemstate* " auf " **true** " fest, um anzugeben, dass die Sicherung einen Start baren Systemstatus enthalten soll.
4.  Wählen Sie die kritischen Komponenten im Writer-Metadatendokument des ASR Writer aus, um die Sicherungskopie zu sichern und [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) für jede dieser Dateien aufzurufen.
5.  Rufen Sie [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) auf, um einen neuen leeren Schattenkopiesatz zu erstellen.
6.  Nennen Sie [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , um den asynchronen Kontakt mit Writern zu initiieren.
7.  Rufen Sie [**IVssBackupComponents:: getschreibmetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) auf, um das Writer-Metadatendokument des ASR Writer abzurufen. Die Writer-ID für den ASR-Writer lautet BE000CBE-11FE-4426-9C58-531AA6355FC4, und die Writer-namens Zeichenfolge lautet "ASR Writer".
8.  Nennen Sie [**ivssexaminewrite Metadata:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) , um eine Kopie des Writer-Metadatendokuments des ASR Writer zu speichern.
9.  Nennen Sie [**IVssBackupComponents:: adddesnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) für jedes Volume, das an Schatten Kopien teilnehmen kann, um das Volume dem Schattenkopiesatz hinzuzufügen.
10. Nennen Sie [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , um Writer zu benachrichtigen, dass ein Sicherungs Vorgang vorbereitet werden soll.
11. Nennen Sie [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (oder [**IVssBackupComponentsEx3:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)), um den Status des ASR-Writers zu überprüfen.
12. An diesem Punkt können Sie Fehlermeldungen Abfragen, die vom Writer in seiner [**CVssWriter:: onpreparebackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) -Methode festgelegt wurden. Beispielcode, der zeigt, wie Sie diese Meldungen anzeigen, finden Sie unter [**ivsscomponestex:: getprepareforbackupfailuremsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Rufen Sie [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) auf, um eine Volumeschattenkopie zu erstellen.
14. Nennen Sie [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) , um den Status des ASR-Writers zu überprüfen.
15. Sichern Sie die Daten.
16. Geben Sie an, ob der Sicherungs Vorgang erfolgreich war, indem Sie [**IVssBackupComponents:: setbackuperfolgreicher**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)aufrufen.
17. Nennen Sie [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , um anzugeben, dass der Sicherungs Vorgang abgeschlossen wurde.
18. Nennen Sie [**IVssBackupComponents:: gatherschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) und [**IVssBackupComponents:: getschreiterstatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). Der Schreib Sitzungs Zustands Speicher ist eine begrenzte Ressource, und Writer müssen die Sitzungs Zustände schließlich wieder verwenden. Durch diesen Schritt wird der Status der Sicherungs Sitzung des Writers als abgeschlossen markiert und VSS benachrichtigt, dass dieser Sicherungs Sitzungs Slot von einem nachfolgenden Sicherungs Vorgang wieder verwendet werden kann.
    > [!Note]  
    > Dies ist nur auf Windows Server 2008 mit Service Pack 2 (SP2) und früher erforderlich.

     

19. Nennen Sie [**IVssBackupComponents:: SaveAsXml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) , um eine Kopie des Dokuments mit den Sicherungs Komponenten des Anforderers zu speichern. Die Informationen im Dokument mit den Sicherungs Komponenten werden zum Zeitpunkt der Wiederherstellung verwendet, wenn die anfordernde Person die [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) -Methode aufruft.

## <a name="choosing-which-critical-components-to-back-up"></a>Auswählen der zu sichernden kritischen Komponenten

In der Initialisierungsphase der Sicherung meldet der ASR Writer die folgenden Typen von Komponenten im Writer-Metadatendokument:

-   Kritische Volumes, wie z. b. die Volumes Boot, System und Windows Recovery Environment (Windows RE) und die Windows RE-Partition, die mit der derzeit laufenden Instanz von Windows Vista oder Windows Server 2008 verknüpft ist. Ein Volume ist ein *wichtiges Volume* , wenn es Systemstatus Informationen enthält. Die Start-und Systemvolumes werden automatisch eingeschlossen. Der Anforderer muss alle Volumes mit systemkritischen Komponenten enthalten, die von Writern gemeldet werden, z. b. die Volumes, die die Active Directory enthalten. System kritische Komponenten werden als "nicht auswählbar für Sicherung" markiert. In VSS bedeutet "nicht wählbar" "nicht optional". Daher muss die anfordernde Person Sie als Teil des Systemstatus sichern. Weitere Informationen finden Sie unter [Sichern und Wiederherstellen des System Status](locating-additional-system-files.md). Komponenten, für die das VSS \_ CF \_ nicht \_ -systemstatusflag \_ festgelegt ist, sind nicht System kritisch.
    > [!Note]  
    > Bei der ASR-Komponente handelt es sich um eine systemkritische Komponente, die vom ASR-Writer gemeldet wird.

     

-   Datenträger. Jeder Festplatten Datenträger auf dem Computer wird als Komponente in ASR verfügbar gemacht. Wenn ein Datenträger während der Sicherung nicht ausgeschlossen wurde, wird er während der Wiederherstellung zugewiesen und kann neu erstellt und neu formatiert werden. Beachten Sie, dass die anfordernde Person während der Wiederherstellung weiterhin einen Datenträger erstellen kann, der während der Sicherung ausgeschlossen wurde, indem Sie die [**IVssBackupComponents:: abtrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) -Methode aufgerufen hat. Wenn ein Datenträger in einem Dynamic Disk Pack ausgewählt ist, müssen auch alle anderen Datenträger dieses Pakets ausgewählt werden. Wenn ein Volume ausgewählt ist, weil es sich um ein wichtiges Volume handelt (d. h. ein Volume, das Systemstatus Informationen enthält), muss jeder Datenträger, der einen Wertebereich für dieses Volume enthält, ebenfalls ausgewählt werden. Um die Blöcke für ein Volume zu finden, verwenden Sie den Code zum Abrufen von volumedatenträger für Volume Abrufen von Volumes. [**\_ \_ \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents)

    > [!Note]  
    > Während der Sicherung sollte der Anforderer alle Festplatten Datenträger einschließen. Wenn der Datenträger, der den Sicherungs Satz des Anforderers enthält, ein lokaler Datenträger ist, sollte dieser Datenträger eingeschlossen werden. Während der Wiederherstellung muss der Anforderer den Datenträger ausschließen, der den Sicherungs Satz des Anforderers enthält, um zu verhindern, dass er überschrieben wird.

     

    In einer Cluster Umgebung erstellt ASR das Layout der freigegebenen Datenträger des Clusters nicht neu. Diese Datenträger sollten Online wieder hergestellt werden, nachdem das Betriebssystem in Windows RE wieder hergestellt wurde.

-   Startkonfigurationsdaten (BCD)-Speicher. Diese Komponente gibt den Pfad des Verzeichnisses an, das den BCD-Speicher enthält. Der Anforderer muss diese Komponente angeben und alle Dateien im BCD-Speicher Verzeichnis sichern. Weitere Informationen zum BCD-Speicher finden Sie unter [about BCD (Informationen zu BCD](/previous-versions/windows/desktop/bcd/about-bcd)).
    > [!Note]  
    > Auf Computern, die die erweiterte Firmware-Schnittstelle (EFI) verwenden, ist die EFI-System Partition (ESP) immer ausgeblendet und kann nicht in eine Volumeschattenkopie eingefügt werden. Der Anforderer muss den Inhalt dieser Partition sichern. Da diese Partition nicht in eine Volumeschattenkopie eingeschlossen werden kann, kann die Sicherung nur über das Live Volume und nicht über die Schatten Kopie ausgeführt werden. Weitere Informationen zu EFI und ESP finden Sie im [Leitfaden zur Einführung](/windows-hardware/drivers/bringup/).

Die Komponentennamen verwenden die folgenden Formate:

-   Für Datenträger Komponenten lautet das Format

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    Dabei steht *n* für die Datenträger Nummer. Nur die Datenträger Nummer wird aufgezeichnet. Um die Datenträger Nummer zu erhalten, verwenden Sie den [**IOCTL- \_ Speicher \_ \_ Geräte \_ Nummer**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) -Steuerungs Code.

-   Bei volumekomponenten lautet das Format

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    Dabei ist *GUID* die Volume-GUID.

-   Für die BCD-Speicherkomponente lautet das Format.

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Wenn die Systempartition einen VolumeGuid-Namen aufweist, kann diese Komponente ausgewählt werden. Andernfalls ist Sie nicht auswählbar.

    > [!Note]  
    > ASR fügt die Dateien der Datei Gruppe der BCD-Speicherkomponente wie folgt hinzu:
    >
    > -   Bei EFI-Datenträgern fügt ASR
    >
    >     *Systempartitionpath* \\ EFI \\ Microsoft- \\ Start \\ \* .\*
    >
    >     Dabei ist " *systempartitionpath* " der Pfad zur Systempartition.
    >
    > -   Für GPT-Datenträger fügt ASR
    >
    >     *Systempartitionpath* \\ Starten \\ \* .\*
    >
    >     Dabei ist " *systempartitionpath* " der Pfad zur Systempartition.
    >
    > -   Der Pfad der Systempartition befindet sich unter dem folgenden Registrierungsschlüssel: **HKEY \_ local \_ Machine** \\ **System** \\ **Setup** \\ **Systempartition** .

     

Bei der Wiederherstellung müssen alle Komponenten, die als kritische Volumes gekennzeichnet sind, wieder hergestellt werden. Wenn ein oder mehrere kritische Volumes nicht wieder hergestellt werden können, kann der Wiederherstellungs Vorgang nicht ausgeführt werden.

In der [**vorab**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) Version der Wiederherstellungs Sequenz werden Datenträger, die während der Sicherung nicht ausgeschlossen wurden, neu erstellt und standardmäßig neu formatiert. Sie werden jedoch nicht neu erstellt oder neu formatiert, wenn Sie die folgenden Bedingungen erfüllen:

-   Ein Basis Datenträger wird nicht neu erstellt, wenn das Datenträger Layout intakt ist oder nur Additive Änderungen vorgenommen wurden. Das Datenträger Layout ist intakt, wenn die folgenden Bedingungen zutreffen:
    -   Die Datenträger Signatur, der Datenträger Stil (GPT oder MBR), die logische Sektorgröße und der Offset des volumestarts werden nicht geändert.
    -   Die Volumegröße wird nicht gesenkt.
    -   Für GPT-Datenträger wird der Partitions Bezeichner nicht geändert.
-   Ein dynamischer Datenträger wird nicht neu erstellt, wenn das Datenträger Layout intakt ist oder nur Additive Änderungen vorgenommen wurden. Damit ein dynamischer Datenträger intakt ist, müssen alle Bedingungen für eine Basis Festplatte erfüllt werden. Außerdem muss die Volumestruktur des gesamten Datenträger Pakets intakt sein. Die Volumestruktur des Datenträger Pakets ist intakt, wenn die folgenden Bedingungen erfüllt sind, die für MBR-und GPT-Datenträger gelten:
    -   Die Anzahl der Volumes, die während der Wiederherstellung im physischen Paket verfügbar sind, muss größer oder gleich der Anzahl der Volumes sein, die während der Sicherung in den ASR Writer-Metadaten angegeben wurden.
    -   Die Anzahl von [*plexes*](../vds/virtual-disk-service-glossary-all.md) pro Volume muss unverändert bleiben.
    -   Die Anzahl der [*Elemente muss unverändert*](../vds/virtual-disk-service-glossary-all.md) bleiben.
    -   Die Anzahl der Werte für den physischen Datenträger muss größer sein als die Anzahl der in den ASR Writer-Metadaten angegebenen Datenträger Blöcke.
    -   Ein intaktes Paket bleibt intakt, wenn zusätzliche Volumes hinzugefügt werden, oder wenn ein Volume im Paket erweitert wird (z. b. von einem einfachen Volume zu einem übergreifenden Volume).
        > [!Note]  
        > Wenn ein einfaches Volume gespiegelt wird, ist das Paket nicht intakt und wird neu erstellt, um sicherzustellen, dass der Status von BCD und Start Volume nach der Wiederherstellung konsistent bleibt. Wenn Volumes gelöscht werden, wird das Paket neu erstellt.

         
-   Wenn die Volumestruktur des dynamischen Datenträger Pakets intakt ist und nur Additive Änderungen vorgenommen wurden, werden die Datenträger im Paket nicht neu erstellt.

    **Windows Vista:** Dynamische Datenträger werden immer neu erstellt. Beachten Sie, dass sich dieses Verhalten in Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) geändert hat.

Der Anforderer kann zu einem beliebigen Zeitpunkt vor Beginn der Wiederherstellungs Phase festlegen, dass die Datenträger schnell formatiert werden sollen, indem Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **restoresession** festlegen. Unter diesem Schlüssel ist ein Wert mit dem Namen " **Quick Format** " mit dem Datentyp "reg \_ DWORD" vorhanden. Wenn dieser Wert nicht vorhanden ist, sollten Sie ihn erstellen. Legen Sie für die schnelle Formatierung die Daten des **QuickFormat** -Werts auf 1 und für eine langsame Formatierung den Wert 0 fest.

Wenn der **QuickFormat** -Wert nicht vorhanden ist, werden die Datenträger langsam formatiert.

Die schnelle Formatierung ist erheblich schneller als eine langsame Formatierung (auch als vollständige Formatierung bezeichnet). Bei der schnellen Formatierung werden die einzelnen Sektoren auf dem Volume jedoch nicht überprüft.

## <a name="overview-of-restore-phase-tasks"></a>Übersicht über Wiederherstellungs Phasen Tasks

Zum Zeitpunkt der Wiederherstellung führt der Anforderer die folgenden Schritte aus:

> [!Note]  
> Alle Schritte sind erforderlich, sofern nicht anders angegeben.

 

1.  Rufen Sie die Funktion " [**foratevssbackupcomponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) " auf, um eine Instanz der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle zu erstellen und die [**IVssBackupComponents:: initializeforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) -Methode aufzurufen, um die Instanz für die Wiederherstellung zu initialisieren, indem Sie das Dokument mit den Sicherungs Komponenten der Anforderer
2.  \[Dieser Schritt ist nur erforderlich, wenn die anfordernde Person ändern muss, ob "includdisk" oder "exclutodisk" für einen oder mehrere Datenträger angegeben ist. \] Nennen Sie [**IVssBackupComponents:: setrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) , um die Wiederherstellungsoptionen für die ASR Writer-Komponenten festzulegen. Der ASR Writer unterstützt die folgenden Optionen: "includedisk" ermöglicht dem Anforderer, einen Datenträger auf dem Zielsystem aufzunehmen, der für die Wiederherstellung berücksichtigt werden soll, auch wenn er während der Sicherungs Phase nicht ausgewählt wurde. Mithilfe von "excludedisk" kann der Anforderer verhindern, dass ein Datenträger auf dem Zielsystem neu erstellt wird. Beachten Sie Folgendes: Wenn für einen Datenträger mit einem wichtigen Volume "excludedisk" angegeben wird, tritt beim nachfolgenden Aufrufen von [**IVssBackupComponents::P**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) erneute Ausführung ein Fehler auf.

    Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von "" [**mithilfe von "**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) " mithilfe von "" die Datenträger 0 und Disk 1 neu erstellen und Treiber von Drittanbietern in das wiederhergestellte Start Volume einfügen können.

    **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Die Injektion von Drittanbieter Treibern wird nicht unterstützt.

    Im Beispiel wird davon ausgegangen, dass der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Zeiger "m \_ pbackupcomponents" gültig ist.

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

    

    Informationen zum Ausschließen aller Datenträger für ein angegebenes Volume finden Sie im folgenden "Ausschließen aller Datenträger für ein Volume".

3.  Aufrufen von [**IVssBackupComponents::P erneut ausführen**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , um den ASR-Writer zu benachrichtigen, dass ein Wiederherstellungs Vorgang vorbereitet werden soll. Nennen Sie [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) so oft wie nötig, bis der Statuswert, der im *phrresult* -Parameter zurückgegeben wird, nicht "VSS" \_ \_ Async \_ Pending ist.
4.  Stellen Sie die Daten wieder her. In der Wiederherstellungs Phase konfiguriert ASR den Volume-GUID-Pfad neu ( \\ \\ ? \\ Volume {GUID}) für jedes Volume, das dem Volume-GUID-Pfad entspricht, der während der Sicherungs Phase verwendet wurde. Laufwerk Buchstaben werden jedoch nicht beibehalten, da dies Konflikte mit den Laufwerk Buchstaben verursachen würde, die automatisch in der Wiederherstellungs Umgebung zugewiesen werden. Daher muss die anfordernde Person beim Wiederherstellen von Daten VolumeGuid-Pfade und nicht Laufwerk Buchstaben verwenden, um auf die Volumes zuzugreifen.
5.  Legen Sie den Registrierungsschlüssel " **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **restoresession** " fest, um die Gruppe von Volumes anzugeben, die wieder hergestellt oder neu formatiert wurden.

    Unter diesem Schlüssel ist ein Wert mit dem Namen **restoredvolumes** mit dem Datentyp reg \_ \_ MultiSZ vorhanden. Wenn dieser Wert nicht vorhanden ist, sollten Sie ihn erstellen. Unter diesem Wert sollte der Anforderer einen VolumeGuid-Eintrag für jedes wiederhergestellte Volume erstellen. Dieser Eintrag sollte das folgende Format \\ aufweisen: \\ \\ Volume {78618c8a-aefd-11da-a898-806e6f 6e6963}. Bei jeder Durchführung einer Bare-Metal-Wiederherstellung legt ASR den Wert **restoredvolumes** auf den Satz von Volumes fest, die von ASR wieder hergestellt wurden. Wenn die anfordernde Person zusätzliche Volumes wieder hergestellt hat, sollte Sie diesen Wert auf die Gesamtmenge der Volumes festlegen, die der Anforderer wieder hergestellt hat, sowie auf die Menge der Volumes, die von ASR wieder hergestellt wurden. Wenn der Anforderer nicht ASR verwendet hat, sollte er die Liste der Volumes ersetzen.

    Sie sollten auch einen Wert mit dem Namen **LastInstance** mit dem Datentyp reg \_ SZ erstellen. Dieser Schlüssel sollte ein zufälliges Cookie enthalten, das den aktuellen Wiederherstellungs Vorgang eindeutig identifiziert. Ein solches Cookie kann mit den Funktionen [**uuidcreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) und [**uuiddestring**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) erstellt werden. Jedes Mal, wenn eine Bare-Metal-Wiederherstellung durchgeführt wird, setzt ASR diesen Registrierungs Wert zurück, um Anforderer und nicht-VSS-Sicherungs Anwendungen zu benachrichtigen, dass die Wiederherstellung erfolgt ist.

6.  Nennen Sie [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , um das Ende des Wiederherstellungs Vorgangs anzugeben. Nennen Sie [**IVssAsync:: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) so oft wie nötig, bis der Statuswert, der im *phrresult* -Parameter zurückgegeben wird, nicht "VSS" \_ \_ Async \_ Pending ist.

In der Wiederherstellungs Phase kann ASR Partitionen erstellen oder entfernen, um den Computer in seinem vorherigen Zustand wiederherzustellen. Anforderer darf nicht versuchen, Datenträger Nummern aus der Sicherungs Phase der Wiederherstellungs Phase zuzuordnen.

Bei der Wiederherstellung muss der Anforderer den Datenträger ausschließen, der den Sicherungs Satz des Anforderers enthält. Andernfalls kann der Sicherungs Satz durch den Wiederherstellungs Vorgang überschrieben werden.

Bei der Wiederherstellung wird ein Datenträger ausgeschlossen, wenn er während der Sicherung nicht als Komponente ausgewählt wurde, oder wenn er durch den Aufruf von [**IVssBackupComponents:: abtrestoreoptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) mit der Option "excludedisk" während der Wiederherstellung explizit ausgeschlossen wird.

Beachten Sie, dass während der WinPE-Notfall Wiederherstellung die ASR Writer-Funktionalität vorhanden ist, aber keine anderen Writer verfügbar sind und der VSS-Dienst nicht ausgeführt wird. Nachdem die WinPE-Notfall Wiederherstellung abgeschlossen wurde, wurde der Computer neu gestartet, und das Windows-Betriebssystem wird normal ausgeführt. der VSS-Dienst kann gestartet werden, und der Anforderer kann alle zusätzlichen Wiederherstellungs Vorgänge durchführen, die eine Teilnahme an anderen Writern als ASR Writer erfordern.

Wenn während der Wiederherstellungs Sitzung von der Sicherungs Anwendung erkannt wird, dass die eindeutigen Volume-IDs unverändert bleiben und daher alle Volumes ab dem Zeitpunkt der Sicherung vorhanden und intakt sind, kann die Sicherungs Anwendung mit der Wiederherstellung des Inhalts der Volumes fortfahren, ohne ASR zu verwenden. In diesem Fall sollte die Sicherungs Anwendung angeben, dass der Computer wieder hergestellt wurde, indem der folgende Registrierungsschlüssel im wiederhergestellten Betriebssystem festgelegt wird: **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **restoresession**

Geben Sie unter diesem Schlüssel **LastInstance** als Wert Name, reg \_ SZ für den Werttyp und ein zufälliges Cookie (z. b. eine GUID, die von der [**uuidcreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) -Funktion erstellt wurde) für die Wertdaten an.

Wenn während der Wiederherstellungs Sitzung von der Sicherungs Anwendung erkannt wird, dass ein oder mehrere Volumes geändert werden oder fehlen, sollte die Sicherungs Anwendung ASR zum Durchführen der Wiederherstellung verwenden. ASR erstellt die Volumes genauso wie zum Zeitpunkt der Sicherung neu und legt den Registrierungsschlüssel **restoresession** fest.

## <a name="excluding-all-disks-for-a-volume"></a>Ausschließen aller Datenträger für ein Volume

Im folgenden Beispiel wird gezeigt, wie alle Datenträger für ein bestimmtes Volume ausgeschlossen werden.


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



 

 
