---
description: Das Windows-Betriebssystem enthält eine Reihe von VSS-Writern, die für das Auflisten der Daten verantwortlich sind, die für die verschiedenen Windows-Features erforderlich sind. Diese werden als &\# 0034;in-box&\# 0034; Writers bezeichnet.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: In-Box-VSS-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e34591cb046a8cc702d32452c159e5b8877f2e66603cbd1b048a0841a04e3bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767799"
---
# <a name="in-box-vss-writers"></a>In-Box-VSS-Writer

Das Windows-Betriebssystem enthält eine Reihe von VSS-Writern, die für das Auflisten der Daten verantwortlich sind, die für die verschiedenen Windows-Features erforderlich sind. Diese werden als "In-Box"-Writer bezeichnet.

> [!Note]  
> Der MSDE-In-Box-Writer ist in Windows Vista, Windows Server 2008 und höher nicht verfügbar. Stattdessen sollte der SQL Writer zum Sichern von Datenbanken SQL Server werden. Nur SQL Server 2005 SP2 und höher werden unter Windows Vista, Windows Server 2008 und höher unterstützt.

 

-   [Active Directory Domain Services (NTDS) VSS Writer](#active-directory-domain-services-ntds-vss-writer)
-   [Active Directory-Verbunddienste (AD FS) Writer](#active-directory-federation-services-writer)
-   [Active Directory Lightweight Directory Services (LDS) VSS Writer](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Active Directory Rights Management Services (AD RMS) Writer](#active-directory-rights-management-services-ad-rms-writer)
-   [Automatisierter ASR-Writer (System Recovery)](#automated-system-recovery-asr-writer)
-   [Background Intelligent Transfer Service (BITS) Writer](#background-intelligent-transfer-service-bits-writer)
-   [Certificate Authority Writer](#certificate-authority-writer)
-   [Cluster Service Writer](#cluster-service-writer)
-   [Freigegebenes Clustervolume VSS Writer (CSV)](#cluster-shared-volume-csv-vss-writer)
-   [COM+-Klassenregistrierung – Datenbankwriter](#com-class-registration-database-writer)
-   [Datendeduplizierungs-Writer](#data-deduplication-writer)
-   [DFS-Replikation (DFSR)](#distributed-file-system-replication-dfsr)
-   [DHCP-Writer (Dynamic Host Configuration Protocol)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Dateireplikationsdienst (File Replication Service, FRS)](#file-replication-service-frs)
-   [File Server Resource Manager (FSRM) Writer](#file-server-resource-manager-fsrm-writer)
-   [Hyper-V Writer](#hyper-v-writer)
-   [IIS Configuration Writer](#iis-configuration-writer)
-   [IIS Metabase Writer](#iis-metabase-writer)
-   [Microsoft Message Queuing (MSMQ) Writer](#microsoft-message-queuing-msmq-writer)
-   [MSSearch Service Writer](#mssearch-service-writer)
-   [NPS VSS Writer](#nps-vss-writer)
-   [Leistungsindikator-Writer](#performance-counters-writer)
-   [Registrierungs-Writer](#registry-writer)
-   [Remotedesktopdienste (Terminal Services) Gateway VSS Writer](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Remotedesktopdienste (Terminal Services) Licensing VSS Writer](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Shadow Copy Optimization Writer](#shadow-copy-optimization-writer)
-   [Sync Share Service Writer](#sync-share-service-writer)
-   [System Writer](#system-writer)
-   [Taskplaner Writer](#task-scheduler-writer)
-   [VSS Metadata Store Writer](#vss-metadata-store-writer)
-   [Windows Deployment Services (WDS) Writer](#windows-deployment-services-wds-writer)
-   [interne Windows-Datenbank Writer (WID)](#windows-internal-database-wid-writer)
-   [Windows WINS-Writer (Internet Name Service)](#windows-internet-name-service-wins-writer)
-   [WMI Writer](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Active Directory Domain Services (NTDS) VSS Writer

Dieser Writer meldet die NTDS-Datenbankdatei (ntds.dit) und die zugeordneten Protokolldateien. Diese Dateien sind erforderlich, um Active Directory ordnungsgemäß wiederherzustellen.

Es gibt nur eine ntds.dit-Datei pro Domänencontroller, und sie wird in den Writer-Metadaten wie im folgenden Beispiel gemeldet:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Hier ist ein Beispiel, das zeigt, wie Komponenten in den Metadaten des Writers aufgeführt werden:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

Zum Zeitpunkt der Sicherung legt der Writer die Ablaufzeit der Sicherung in den Sicherungsmetadaten des Writers fest. Anfordernde Benutzer sollten diese Metadaten mithilfe von [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist. Abgelaufene Datenbanken können nicht wiederhergestellt werden.

Wenn der Computer, der die NTDS-Datenbank enthält, ein Domänencontroller ist, sollte die Sicherungsanwendung immer eine Systemstatussicherung auf allen Volumes durchführen, die wichtige Systemstatusinformationen enthalten. Zur Wiederherstellungszeit sollte die Anwendung zunächst den Computer im Verzeichnisdienst-Wiederherstellungsmodus neu starten und dann eine Wiederherstellung des Systemstatus durchführen.

Die Zeichenfolge für den Writernamen für diesen Writer ist "NTDS".

Die Writer-ID für diesen Writer ist B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Active Directory-Verbunddienste (AD FS) Writer

Dieser Writer meldet die Active Directory-Verbunddienste (AD FS) (AD FS)-Datendateien.

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer ist "AD FS VSS Writer".

Die Writer-ID für diesen Writer ist 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Active Directory Lightweight Directory Services (LDS) VSS Writer

Dieser Writer meldet die ADAM-Datenbankdatei (adamntds.dit) und die zugehörigen Protokolldateien für jede Instanz in %program files% \\ Microsoft ADAM \\ instance *N* data, wobei \\ *N* die ADAM-Instanznummer ist. Diese Datenbankprotokolldateien sind erforderlich, um ADAM-Instanzen wiederherzustellen.

**Windows XP:** Dieser Writer wird nicht unterstützt.

Hier ist ein Beispiel, das zeigt, wie Komponenten in den Metadaten des Writers aufgeführt werden:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

Zur Sicherungszeit legt der Writer die Ablaufzeit der Sicherung in den Sicherungsmetadaten fest. Sicherungsanwendungen sollten diese Metadaten mithilfe der [**IVssComponent::GetBackupMetadata-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist. Abgelaufene Datenbanken können nicht wiederhergestellt werden.

Die Zeichenfolge für den Writernamen für diesen Writer ist "ADAM (Instanz *N*) Writer", wobei *N* die ADAM-Instanznummer ist, z.B. "ADAM (instance1) Writer", "ADAM (instance2) Writer" und so weiter.

Die Writer-ID für diesen Writer ist DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Diese Writer-ID ist für alle Instanzen identisch.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Active Directory Rights Management Services (AD RMS) Writer

Dieser Writer meldet die Active Directory Rights Management-Datendateien (AD RMS Service).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer ist "AD RMS Writer".

Die Writer-ID für diesen Writer ist 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Automatisierter ASR-Writer (System Recovery)

Der ASR Writer speichert die Konfiguration von Datenträgern auf dem System. Dieser Writer meldet die Startkonfigurationsdatenbank (Boot Configuration Database, BCD) und ist auch für die Bereitstellung der Registrierungsstruktur verantwortlich, die die BCD während der Erstellung von Schattenkopien darstellt. Der ASR-Writer muss in allen Sicherungen enthalten sein, die für die Bare-Metal-Wiederherstellung erforderlich sind. Weitere Informationen zu ASR finden Sie unter [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge für den Writernamen für diesen Writer ist "ASR Writer".

Die Writer-ID für den ASR-Writer ist BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Background Intelligent Transfer Service (BITS) Writer

Der BITS-Writer verwendet den **Registrierungsschlüssel FilesNotToBackup,** um Dateien aus dem BITS-Cacheordner auszuschließen. Der Standardcachespeicherort ist %AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ Cache.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Darüber hinaus schließt der BITS-Writer die folgenden Dateien aus der Sicherung aus: die BITS-Zustandsdateien (qmgr0.dat und qmgr1.dat), die BITS-Debugprotokolldatei und teilweise heruntergeladene BITS-Dateien.

Wenn es sich bei der BITS-Downloadzieldatei um eine SMB-Datei handelt, muss das Clientkonto eine Vertrauensstellung mit dem Server haben. Ander denn, bei Sicherungen kann ein Fehler auftauen.

Die Zeichenfolge für den Writernamen für diesen Writer ist "BITS Writer".

Die Writer-ID für den BITS-Writer ist 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Certificate Authority Writer

Dieser Writer ist für das Aufzählen der Datendateien für den Zertifikatserver verantwortlich.

Die Zeichenfolge für den Writernamen für diesen Writer ist "Certificate Authority".

**Windows XP:** Die Writer-Namenszeichenfolge für diesen Writer ist "Certificate Server Writer".

Die Writer-ID für den Writer ist 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Cluster Service Writer

Der Clusterdienst-VSS Writer ist in der Dokumentation zur [Clusterdienst-API](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) dokumentiert.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst nach Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 unterstützt.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Freigegebenes Clustervolume VSS Writer (CSV)

Dieser Writer meldet die csv-Datendateien (Freigegebenes Clustervolume). Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer lautet "Freigegebenes Clustervolume VSS Writer".

Die Writer-ID für den Writer lautet 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>COM+-Klassenregistrierungsdatenbank-Writer

Dieser Writer ist für den Inhalt des Verzeichnisses %SystemRoot% \\ Registration verantwortlich. Der COM+-Katalog ist eine Datei in %SystemRoot% \\ Registration mit einem Namen, der dem Muster R *xxxxxxxxxxxxxx*.clb folgt, wobei *xxxxxxxxxxxxxx* eine 12-stellige Hexadezimalzahl ist. Es kann mehrere solcher Dateien geben, wenn COM+-Anwendungen auf dem Computer konfiguriert wurden. Die Datei, die den aktuellen COM+-Katalog enthält, ist die Datei mit dem größten Wert von *xxxxxxxxxxxx.*

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die COM+-Klassenregistrierungsdatenbank hängt davon ab, dass ein Registrierungsschlüssel gesichert wird und daher zusammen mit der Registrierung gesichert und wiederhergestellt werden muss.

Um die COM+-Registrierungsdatenbank wiederherzustellen, muss eine Sicherungsanwendung (Anfordernde) die [**ICOMAdminCatalog::RestoreREGDB-Methode**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) aufrufen.

Die Writer-Namenszeichenfolge für diesen Writer lautet "COM+ REGDB Writer".

Die Writer-ID für den COM+-Klassenregistrierungsdatenbank-Writer lautet 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Data Deduplication Writer

Der VSS Writer für die Datendeduplizierung ist in der Dokumentation zur [Datendeduplizierungs-API](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) dokumentiert. Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.

## <a name="distributed-file-system-replication-dfsr"></a>DFS-Replikation (DFSR)

Die folgende Komponente enthält einen VSS Writer: [verteiltes Dateisystem Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst Windows Vista mit SP1 und Windows Server 2008 unterstützt.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>DHCP-Writer (Dynamic Host Configuration Protocol)

Dieser Writer ist für das Aufzählen von Dateien zuständig, die für die DHCP-Serverrolle erforderlich sind. Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

Die Writer-Namenszeichenfolge für diesen Writer lautet "Dhcp Jet Writer".

Die Writer-ID für diesen Writer lautet BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Dateireplikationsdienst (File Replication Service, FRS)

Der Dateireplikationsdienst-Writer ist unter [Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md)dokumentiert.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst Windows Vista mit SP1 und Windows Server 2008 unterstützt.

## <a name="file-server-resource-manager-fsrm-writer"></a>FsRM-Writer (File Server Resource Manager)

Dieser Writer listet die FSRM-Konfigurationsdateien auf, die für die Systemstatussicherung verwendet werden. Während Wiederherstellungsvorgängen werden Änderungen an der FSRM-Konfiguration verhindert, und die Erzwingung von Kontingenten und Dateibildschirmen wird vorübergehend angehalten. Nach Abschluss der Wiederherstellung aktualisiert der Writer FSRM mit der wiederhergestellten Konfiguration. Dieser Writer ist nur vorhanden, wenn FSRM (Teil der Dateidiensterolle) installiert ist und ausgeführt wird. Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

**Windows Server 2003:** Dieser Writer wird erst Windows Server 2003 R2 unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer lautet "FSRM Writer".

Die Writer-ID für diesen Writer lautet 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Hyper-V Writer

Der Hyper-V VSS Writer ist in der Dokumentation zur [Hyper-V-API](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) dokumentiert. Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

**Windows Server 2003:** Dieser Writer wird erst Windows Server 2008 unterstützt.

## <a name="iis-configuration-writer"></a>IIS-Konfigurationswriter

Der IIS-Konfigurationswriter ist für das Aufzählen der IIS-Konfigurationsdateien verantwortlich.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst Windows Vista mit SP1 und Windows Server 2008 unterstützt. Anforderer müssen die IIS-Konfigurationsdateien sichern, einschließlich der .NET FX-machine.config datei oder der ASP.NET Stammdatei web.config.

Dieser Writer gesichert nicht die .NET FX-machine.config datei oder die ASP.NET Stammdatei web.config, da diese Dateien vom SystemWriter aufzählt werden.

Dieser Writer gesichert alle Dateien, die sich im Konfigurationsschema %windir% \\ system32 \\ inetsrv \\ \\ und %windir% \\ system32 \\ inetsrv \\ inetsrv-Konfigurationsverzeichnissen befinden, mit Ausnahme von Dateien, die vom Systemwriter aufzählt werden.

Die Writer-ID für den IIS-Konfigurationswriter lautet 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>IIS Metabase Writer

Der IiS-Metabasiswriter (Internet Information Server) ist für das Aufzählen der IIS-Metabasisdatei verantwortlich.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst Windows Vista mit SP1 und Windows Server 2008 unterstützt. Anforderer müssen die IIS-Metabasisdatei sichern.

Die Writer-ID für den IIS-Metabasiswriter lautet 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Microsoft Message Queuing (MSMQ) Writer

Dieser Writer meldet die MSMQ-Datendateien (Microsoft Message Queuing).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer lautet "MSMQ Writer (*SvcName*)", wobei *SvcName* der Name des MSMQ-Diensts ist, dem der Writer zugeordnet ist. Bei der Standardinstallation lautet der Dienstname "MSMQ". Bei gruppierten Instanzen lautet der Dienstname MSMQ$*ResourceName*, wobei *ResourceName* der gruppierte MSMQ-Ressourcenname ist.

Die Writer-ID für diesen Writer lautet 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>MSSearch Service Writer

Dieser Writer ist zum Löschen von Suchindexdateien aus Schattenkopien nach der Erstellung vorhanden. Dies wird durchgeführt, um die Auswirkungen von E/A-Kopie bei Schreibzugriff während regulärer E/A-Vorgänge auf diese Dateien auf dem durch Schatten kopierten Volume zu minimieren.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Um diesen Writer auf dem Server zu installieren, müssen Sie die Rolle Dateidienste installieren und den Windows-Suchdienst aktivieren.

Die Writer-Namenszeichenfolge für diesen Writer lautet "MSSearch Service Writer".

Die Writer-ID für den MSSearch-Dienstwriter lautet CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>NPS VSS Writer

Der NPS Writer ist für das Aufzählen der NPS-Konfigurationsdateien (Netzwerkrichtlinienserver) für Server verantwortlich, auf denen die Netzwerkrichtlinie und Access Services-Rolle installiert sind.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst Windows Vista mit SP1 und Windows Server 2008 unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer lautet "NPS VSS Writer".

Die Writer-ID für den NPS VSS Writer lautet 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Performance Counters Writer

Dieser Writer meldet die Konfigurationsdateien des Leistungsindikators. Diese Dateien werden nur während der Anwendungsinstallation geändert und sollten bei Systemstatussicherungen und -wiederherstellungen gesichert und wiederhergestellt werden.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt. Anforderer müssen diese Dateien manuell sichern. (Siehe [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md).)

Die Writer-Namenszeichenfolge für diesen Writer lautet "Performance Counters Writer".

Die Writer-ID für den Leistungsindikatorwriter lautet 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Registry Writer

Der Registrierungswriter meldet die Windows Registrierungsdateien, um die sicherungen und Wiederherstellungen der Registrierung zu ermöglichen. Es werden keine Benutzerstrukturen berichtet.

**Windows Server 2003:** In Windows Server 2003 verwendet dieser Writer eine Zwischen-Repositorydatei (manchmal auch als "Spit-Datei" bezeichnet), um Registrierungsdaten zu speichern. (Siehe [Registrierungssicherungs- und -wiederherstellungsvorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)

**Windows XP:** Dieser Writer wird nicht unterstützt. (Siehe [Registrierungssicherungs- und -wiederherstellungsvorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)

Die Writer-Namenszeichenfolge für diesen Writer lautet "Registry Writer".

Die Writer-ID für den Registrierungswriter lautet AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>Remotedesktopdienste Gateway VSS Writer (Terminaldienste)

Dieser Writer ist für das Aufzählen der Remotedesktopdienste (Terminaldienste)-Gatewaydateien für Server verantwortlich, auf denen Remotedesktop Gateway, eine Unterrolle Remotedesktopdienste Rolle, installiert ist.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Dieser Writer ist ein in der Box enthaltener Writer für Windows Server-Betriebssystemversionen. sie wird nicht in Windows Client versendet.

Das Remotedesktopdienste Gateway hängt von mehreren Registrierungsschlüsseln ab, die gesichert werden, und muss daher zusammen mit der Registrierung gesichert und wiederhergestellt werden.

Die Writer-Namenszeichenfolge für diesen Writer lautet "TS Gateway Writer".

Die Writer-ID für diesen Writer lautet 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Remotedesktopdienste (Terminaldienste) – Lizenzierung von VSS Writer

Dieser Writer ist für das Aufzählen der Dateien Remotedesktopdienste Licensing (RD Licensing) oder Terminal Services Licensing (TS Licensing) für Server verantwortlich, auf denen Remotedesktop Licensing, eine Unterrolle der Remotedesktopdienste-Rolle, installiert ist.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Dieser Writer ist ein In-Box-Writer für Windows Server-Betriebssystemversionen. es wird nicht im Windows.

Remotedesktopdienste Lizenzierung hängt davon ab, dass mehrere Registrierungsschlüssel sichern werden und daher zusammen mit der Registrierung sichern und wiederhergestellt werden müssen.

Die Writer-Namenszeichenfolge für diesen Writer ist "TermServLicensing".

Die Writer-ID für diesen Writer ist 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Shadow Copy Optimization Writer

Dieser Writer löscht bestimmte Dateien aus Volumeschattenkopien. Dies wird durchgeführt, um die Auswirkungen von E/A beim Kopieren beim Schreiben während der regulären E/A auf diese Dateien auf dem Schattenkopie-Volume zu minimieren. Die gelöschten Dateien sind in der Regel temporäre Dateien oder Dateien, die keinen Benutzer- oder Systemstatus enthalten.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer ist "Shadow Copy Optimization Writer".

Die Writer-ID für den Writer für die Schattenkopieoptimierung ist 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Sync Share Service Writer

**Windows Server 2012 R2:** Dieser Writer ist in Windows Server 2012 R2 und neueren Serverversionen enthalten. Sie ist nicht mit Desktopversionen kompatibel.

Dieser Writer ist für das Aufzählen der Synchronisierungsfreigaben auf Servern verantwortlich, auf denen der Synchronisierungsfreigabedienst installiert ist, und dafür sicherzustellen, dass die Metadaten und Daten während der Sicherung und Wiederherstellung konsistent bleiben.

Dieser Writer ist nur vorhanden, wenn der Synchronisierungsfreigabedienst installiert ist und ausgeführt wird.

Es gibt eine VSS Writer-Komponente für jede Synchronisierungsfreigabe. Dies schließt die Metadaten und Datenpfade ein. Diese müssen zur Konsistenz zusammen sichern werden.

Die Zeichenfolge für den Writernamen ist "Sync Share Service VSS Writer".

Die Writer-ID ist D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>System Writer

Der Systemwriter aufzählt alle Betriebssystem- und Treiberbinärdateien und ist für eine Systemstatussicherung erforderlich.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Dieser Writer wird als Teil des Kryptografiediensts (CryptSvc) ausgeführt. Der SystemWriter generiert eine Dateiliste, die die folgenden Dateien enthält:

-   Alle statischen Dateien, die installiert wurden. Eine statische Datei ist eine Datei, die im Komponentenmanifest aufgeführt ist, bei der das **WriteableType-Dateiattribut** auf "static" oder "" festgelegt ist. Statische Dateien enthalten alle Dateien, die durch Windows Resource Protection (WRP) geschützt sind. Allerdings sind nicht alle statischen Dateien WRP-geschützte Dateien. Beispielsweise sind Spieldateien statisch, aber nicht WRP-geschützt, sodass Administratoren einstellungen für die Jugendschutzverwaltung ändern können.
-   Der Inhalt des Windows WinSxS-Verzeichnisses (Side-by-Side), einschließlich aller Manifeste, optionalen Komponenten und Win32-Drittanbieterdateien.
    > [!Note]  
    > Viele der Dateien im Verzeichnis %windir% system32 sind harte Links zu Dateien \\ im WinSxS-Verzeichnis.

     

-   Alle PnP-Dateien für installierte Treiber (im Besitz von PnP).
-   Alle Benutzermodusdienste und Nicht-PnP-Treiber.
-   Alle Kataloge im Besitz von CryptSvc.

Die Wiederherstellungsanwendung ist dafür verantwortlich, die Dateien und die Registrierung zu erstellen und ACLs so zu konfigurieren, dass sie mit der Schattenkopie des Systems übereinstimmen. Die entsprechenden hard-Links müssen auch erstellt werden, damit eine Wiederherstellung des Systemstatus erfolgreich ist.

Die Zeichenfolge für den Writernamen für diesen Writer ist "System Writer".

Die Writer-ID für den Systemwriter ist E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Taskplaner Writer

Dieser Writer meldet die Aufgabendateien des Aufgabenplaners.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt. An anfordernde Benutzer müssen diese Dateien manuell sichern. (Siehe [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md).)

Die Writer-Namenszeichenfolge für diesen Writer ist "Taskplaner Writer".

Die Writer-ID für den Writer ist D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>VSS Metadata Store Writer

Dieser Writer meldet die Writermetadatendateien für alle VSS Express Writer.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer ist "VSS Express Writer Metadata Store Writer".

Die Writer-ID für den Writer ist 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Windows Deployment Services (WDS) Writer

Dieser Writer meldet die Windows WDS-Datendateien (Deployment Services).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Writer-Namenszeichenfolge für diesen Writer ist "WDS VSS Writer".

Die Writer-ID für diesen Writer ist 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>interne Windows-Datenbank Writer (WID)

Dieser Writer meldet die interne Windows-Datenbank -Datendateien (WID).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003** und Windows XP: Dieser Writer wird nicht unterstützt.

Die Zeichenfolge für den Writernamen für diesen Writer ist "WIDWriter".

Die Writer-ID für diesen Writer ist 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Windows WINS-Writer (Internet Name Service)

Dieser Writer ist für das Aufzählen von Dateien verantwortlich, die für WINS erforderlich sind.

**Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge für den Writernamen für diesen Writer ist "WINS Jet Writer".

Die Writer-ID für diesen Writer ist F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>WMI Writer

Dieser Writer wird verwendet, um WMI-spezifische Status und Daten während Sicherungsvorgängen zu identifizieren. Die Daten enthalten Dateien aus dem WBEM-Repository.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge für den Writernamen für diesen Writer ist "WMI Writer".

Die Writer-ID für diesen Writer ist A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
