---
description: Das Windows-Betriebssystem enthält eine Reihe von VSS-Writern, die für das Auflisten der Daten verantwortlich sind, die für die verschiedenen Windows-Features erforderlich sind. Diese werden als &\# 0034, in-Box-&\# 0034; Writer bezeichnet.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: In-Box-VSS-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357506"
---
# <a name="in-box-vss-writers"></a>In-Box-VSS-Writer

Das Windows-Betriebssystem enthält eine Reihe von VSS-Writern, die für das Auflisten der Daten verantwortlich sind, die für die verschiedenen Windows-Features erforderlich sind. Diese werden als "in-Box"-Writer bezeichnet.

> [!Note]  
> Der MSDE-in-Box-Writer ist in Windows Vista, Windows Server 2008 und höher nicht verfügbar. Stattdessen sollte der SQL Writer verwendet werden, um SQL Server-Datenbanken zu sichern. Nur SQL Server 2005 SP2 und höher werden unter Windows Vista, Windows Server 2008 und höher unterstützt.

 

-   [Active Directory Domain Services (NTDS) VSS Writer](#active-directory-domain-services-ntds-vss-writer)
-   [Active Directory-Verbunddienste (AD FS) Writer](#active-directory-federation-services-writer)
-   [Active Directory Lightweight Directory Services (LDS) VSS Writer](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Active Directory Rights Management Services (AD RMS) Writer](#active-directory-rights-management-services-ad-rms-writer)
-   [ASR-Writer (Automated System Recovery)](#automated-system-recovery-asr-writer)
-   [Background Intelligent Transfer Service (Bits) Writer](#background-intelligent-transfer-service-bits-writer)
-   [Zertifikatauthority-Writer](#certificate-authority-writer)
-   [Cluster Dienstanbieter](#cluster-service-writer)
-   [Freigegebenes Clustervolume (CSV) VSS Writer](#cluster-shared-volume-csv-vss-writer)
-   [Datenbank-Writer der com+-Klassen Registrierung](#com-class-registration-database-writer)
-   [Datendeduplizierungswriter](#data-deduplication-writer)
-   [DFS-Replikation (DFSR)](#distributed-file-system-replication-dfsr)
-   [DHCP-Writer (Dynamic Host Configuration-Protokoll)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Dateireplikationsdienst (File Replication Service, FRS)](#file-replication-service-frs)
-   [Datei Server Ressourcen-Manager Writer (File Server, f)](#file-server-resource-manager-fsrm-writer)
-   [Hyper-V-Writer](#hyper-v-writer)
-   [IIS-konfigurationswriter](#iis-configuration-writer)
-   [IIS-metabasiswriter](#iis-metabase-writer)
-   [Microsoft Message Queuing (MSMQ) Writer](#microsoft-message-queuing-msmq-writer)
-   [MSSearch-dienstwriter](#mssearch-service-writer)
-   [NPS-VSS-Writer](#nps-vss-writer)
-   [Leistungsindikatoren Writer](#performance-counters-writer)
-   [Registrierungswriter](#registry-writer)
-   [Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Writer zur Optimierung der Schatten Kopie](#shadow-copy-optimization-writer)
-   [Synchronisierungs Freigabe Dienst-Writer](#sync-share-service-writer)
-   [Systemwriter](#system-writer)
-   [Taskplaner Writer](#task-scheduler-writer)
-   [VSS-Metadatenspeicher-Writer](#vss-metadata-store-writer)
-   [Windows-Bereitstellungs Dienste (WDS) Writer](#windows-deployment-services-wds-writer)
-   [Interner Windows-Daten Bank Schreiber (WID)](#windows-internal-database-wid-writer)
-   [WINS-Writer (Windows Internet Name Service)](#windows-internet-name-service-wins-writer)
-   [WMI-Writer](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Active Directory Domain Services (NTDS) VSS Writer

Dieser Writer meldet die NTDS-Datenbankdatei (NTDS. dit) und die zugehörigen Protokolldateien. Diese Dateien sind erforderlich, um die Active Directory ordnungsgemäß wiederherzustellen.

Pro Domänen Controller ist nur eine NTDS. dit-Datei vorhanden, und Sie wird in den Writer-Metadaten wie im folgenden Beispiel berichtet:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Es folgt ein Beispiel, das zeigt, wie Sie Komponenten in den Metadaten des Writers auflisten:

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

Zum Zeitpunkt der Sicherung legt der Writer den Ablauf Zeitpunkt der Sicherung in den Sicherungs Metadaten des Writers fest. Anforderer sollten diese Metadaten mithilfe von [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist. Abgelaufene Datenbanken können nicht wieder hergestellt werden.

Wenn es sich bei dem Computer, der die NTDS-Datenbank enthält, um einen Domänen Controller handelt, sollte die Sicherungs Anwendung immer eine Systemstatus Sicherung auf allen Volumes mit kritischen Systemstatus Informationen ausführen. Zum Zeitpunkt der Wiederherstellung sollte die Anwendung den Computer zunächst im Verzeichnisdienst-Wiederherstellungs Modus neu starten und dann eine Systemstatus Wiederherstellung durchführen.

Die Zeichenfolge des Writer-namens für diesen Writer ist "NTDS".

Die Writer-ID für diesen Writer ist B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Active Directory-Verbunddienste (AD FS) Writer

Dieser Writer meldet die Active Directory-Verbunddienste (AD FS) (ADFS)-Datendateien.

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "ADFS VSS Writer".

Die Writer-ID für diesen Writer lautet 772c45b8-AE01-4l94-940c-94961864acad.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Active Directory Lightweight Directory Services (LDS) VSS Writer

Dieser Writer meldet die Adam-Datenbankdatei (Adamntds. dit) und die zugehörigen Protokolldateien für jede Instanz in% Program Files% \\ Microsoft Adam \\ instance *N* \\ Data, wobei *N* für die Adam-Instanznummer steht. Diese Daten Bank Protokolldateien sind erforderlich, um ADAM-Instanzen wiederherzustellen.

**Windows XP:** Dieser Writer wird nicht unterstützt.

Es folgt ein Beispiel, das zeigt, wie Sie Komponenten in den Metadaten des Writers auflisten:

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

Zum Zeitpunkt der Sicherung legt der Writer den Ablauf Zeitpunkt der Sicherung in den Sicherungs Metadaten fest. Sicherungs Anwendungen sollten diese Metadaten mithilfe der [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) -Methode abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist. Abgelaufene Datenbanken können nicht wieder hergestellt werden.

Die Zeichenfolge des Writer-namens für diesen Writer ist "Adam (Instance *N*) Writer", wobei *N* die Adam-Instanznummer ist, z. b. "Adam (instance1) Writer", "Adam (Instance2) Writer" usw.

Die Writer-ID für diesen Writer ist DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Diese Writer-ID ist für alle Instanzen identisch.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Active Directory Rights Management Services (AD RMS) Writer

Dieser Writer meldet die Datendateien des Active Directory Rights Management-Diensts (AD RMS).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "AD RMS Writer".

Die Writer-ID für diesen Writer lautet 886c43b1-D455-4428-a37b-4d6b9e43f.

## <a name="automated-system-recovery-asr-writer"></a>ASR-Writer (Automated System Recovery)

Der ASR Writer speichert die Konfiguration der Datenträger auf dem System. Dieser Writer meldet die Start Konfigurations Datenbank (Boot Configuration Database, BCD) und ist auch für das Aufheben der Bereitstellung der Registrierungs Struktur zuständig, die die BCD während der Erstellung von Schatten Kopien darstellt. Der ASR Writer muss in alle Sicherungen eingeschlossen werden, die für die Bare-Metal-Wiederherstellung erforderlich sind. Weitere Informationen zu ASR finden Sie unter [Verwenden der automatisierten VSS-System Wiederherstellung für die Notfall Wiederherstellung](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "ASR Writer".

Die Writer-ID für den ASR-Writer lautet BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Background Intelligent Transfer Service (Bits) Writer

Der Bits-Writer verwendet den Registrierungsschlüssel **FilesNotToBackup** , um Dateien aus dem Bits-Cache Ordner auszuschließen. Der Standard Cache Speicherort ist% ALLUSERSPROFILE% \\ Microsoft \\ Network \\ Downloader \\ Cache.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Außerdem schließt der Bits-Writer die folgenden Dateien von der Sicherung aus: die Bits-Zustands Dateien (qmgr0. dat und qmgr1. dat), die Bits-Debugprotokolldatei und die Bits-Dateien, die teilweise heruntergeladen wurden.

Wenn es sich bei der Bits-Download Zieldatei um eine SMB-Datei handelt, muss das Client Konto eine Vertrauensstellung mit dem Server aufweisen, andernfalls können Sicherungen fehlschlagen.

Die Zeichenfolge des Writer-namens für diesen Writer ist "Bits Writer".

Die Writer-ID für den Bits-Writer lautet 4969d978-be47-48b0-b100f 328l07ac1e0.

## <a name="certificate-authority-writer"></a>Zertifikatauthority-Writer

Dieser Writer ist für das Auflisten der Datendateien für den Zertifikat Server zuständig.

Die Zeichenfolge des Writer-namens für diesen Writer ist "Zertifizierungsstelle".

**Windows XP:** Die Zeichenfolge des Writer-namens für diesen Writer ist "Certificate Server Writer".

Die Writer-ID für den Writer ist 6b5b15b5-da24-4d88-B737-63063e3a1f.

## <a name="cluster-service-writer"></a>Cluster Dienstanbieter

Der Cluster Dienst VSS Writer ist in der Dokumentation zur [Cluster Dienst](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) -API dokumentiert.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst ab Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 unterstützt.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Freigegebenes Clustervolume (CSV) VSS Writer

Dieser Writer meldet die freigegebenes Clustervolume (CSV)-Datendateien. Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "freigegebenes Clustervolume VSS Writer".

Die Writer-ID für den Writer lautet 1072ae1c-e5a7-4ea1-9e4a-6l7964656570.

## <a name="com-class-registration-database-writer"></a>Datenbank-Writer der com+-Klassen Registrierung

Dieser Writer ist verantwortlich für den Inhalt des Registrierungs Verzeichnisses% systemroot% \\ . Der com+-Katalog ist eine Datei in der% systemroot%- \\ Registrierung mit einem Namen, der dem Muster R *xxxxxxxxxxxx*. CLB folgt, wobei *xxxxxxxxxxxx* eine 12-stellige hexadezimal Zahl ist. Es können möglicherweise mehrere Dateien vorhanden sein, wenn com+-Anwendungen auf dem Computer konfiguriert wurden. Die Datei, die den aktuellen com+-Katalog enthält, ist die Datei mit dem größten Wert *xxxxxxxxxxxx*.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die com+-Klassen Registrierungsdatenbank hängt von einem Registrierungsschlüssel ab, der gesichert wird, und muss daher zusammen mit der Registrierung gesichert und wieder hergestellt werden.

Zum Wiederherstellen der COM+-Registrierungsdatenbank muss eine Sicherungs Anwendung (Requester) die [**icomadmincatalog:: restoreregdb**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) -Methode abrufen.

Die Zeichenfolge des Writer-namens für diesen Writer ist "com+ RegDB Writer".

Die Writer-ID für den Datenbank-Writer der com+-Klassen Registrierung lautet 542da469-d3e1-473c-9F 4f -7847s01fc64f.

## <a name="data-deduplication-writer"></a>Datendeduplizierungswriter

Die VSS Writer für die Datendeduplizierung ist in der Dokumentation zur [Datendeduplizierung](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) -API dokumentiert. Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.

## <a name="distributed-file-system-replication-dfsr"></a>DFS-Replikation (DFSR)

Die folgende Komponente enthält eine VSS Writer: [verteiltes Dateisystem Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders) .

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>DHCP-Writer (Dynamic Host Configuration-Protokoll)

Dieser Writer ist für das Auflisten von Dateien zuständig, die für die DHCP-Server Rolle erforderlich sind. Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

Die Zeichenfolge des Writer-namens für diesen Writer ist "DHCP Jet Writer".

Die Writer-ID für diesen Writer ist BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Dateireplikationsdienst (File Replication Service, FRS)

Der Datei Replikations Dienst-Writer ist in [Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md)dokumentiert.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.

## <a name="file-server-resource-manager-fsrm-writer"></a>Datei Server Ressourcen-Manager Writer (File Server, f)

Dieser Writer listet die für die Systemstatus Sicherung verwendeten f-Konfigurationsdateien auf. Während des Wiederherstellungs Vorgangs wird verhindert, dass Änderungen an der Konfiguration der voll Funktions Konfiguration vorgenommen werden und die Erzwingung von Kontingenten Nachdem die Wiederherstellung durchgeführt wurde, aktualisiert der Writer den vollständigen Dienst mit der wiederhergestellten Konfiguration. Dieser Writer ist nur vorhanden, wenn "f" (Teil der Rolle "Dateidienste") installiert ist und ausgeführt wird. Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

**Windows Server 2003:** Dieser Writer wird bis Windows Server 2003 R2 nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "f-Writer".

Die Writer-ID für diesen Writer ist 12ce4370-5bb7-4C58-a76a-e5d5097e3674.

## <a name="hyper-v-writer"></a>Hyper-V-Writer

Die Hyper-v-VSS Writer ist in der Dokumentation zur [Hyper-v-](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API dokumentiert. Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

**Windows Server 2003:** Dieser Writer wird bis Windows Server 2008 nicht unterstützt.

## <a name="iis-configuration-writer"></a>IIS-konfigurationswriter

Der IIS-konfigurationswriter ist für das Auflisten der IIS-Konfigurationsdateien verantwortlich.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt. Anforderer ist erforderlich, um die IIS-Konfigurationsdateien zu sichern, einschließlich der .net FX machine.config-Datei oder der ASP.net-Stamm web.config Datei.

Dieser Writer sichert keine Sicherungskopie der .net FX-machine.config Datei oder der ASP.net-Stamm web.config Datei, da diese Dateien vom System-Writer aufgelistet werden.

Dieser Writer sichert alle Dateien, die sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config \\ und% windir% \\ system32 \\ inetsrv \\ config befinden, mit Ausnahme der Dateien, die vom System-Writer aufgelistet werden.

Die Writer-ID für den IIS-konfigurationswriter ist 2a40f D15-dfca-4aa8-a654-1F 8c654603.

## <a name="iis-metabase-writer"></a>IIS-metabasiswriter

Der IIS-metabasewriter (Internet Information Server) ist für das Auflisten der IIS-Metabasisdatei verantwortlich.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt. Anforderer ist erforderlich, um die IIS-Metabasisdatei zu sichern.

Die Writer-ID für den IIS-metabasiswriter lautet 59b1f0cf-90EF-465F-9609-6ca8b2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Microsoft Message Queuing (MSMQ) Writer

Dieser Writer meldet die Microsoft Message Queuing Datendateien (MSMQ).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer lautet "MSMQ Writer (*SvcName*)", wobei *SvcName* der Name des MSMQ-Diensts ist, dem der Writer zugeordnet ist. Bei der Standardinstallation lautet der Dienst Name "MSMQ". Bei gruppierten Instanzen lautet der Dienst Name MSMQ $*resourceName*, wobei *resourceName* der geclusterte MSMQ-Ressourcen Name ist.

Die Writer-ID für diesen Writer lautet 7e47b561-971a-46e6-96b9-696eeaa53b2a.

## <a name="mssearch-service-writer"></a>MSSearch-dienstwriter

Dieser Writer ist vorhanden, um Such Indexdateien aus Schatten Kopien nach der Erstellung zu löschen. Dadurch wird die Auswirkung der e/a-Vorgänge für die e/a-Kopiervorgänge während der regulären e/a-Vorgänge auf den Dateien auf dem schattenkopierten Volume minimiert.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Um diesen Writer auf dem Server zu installieren, müssen Sie die Rolle "Dateidienste" installieren und den Windows-Suchdienst aktivieren.

Die Zeichenfolge des Writer-namens für diesen Writer ist "MSSearch-dienstwriter".

Die Writer-ID für den MSSearch-Dienst Schreiber lautet CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>NPS-VSS-Writer

Der NPS-Writer ist für das Auflisten der Netzwerk Richtlinien Server-Konfigurationsdateien (Network Policy Server, NPS) für Server zuständig, auf denen die Rolle "Netzwerk Richtlinien-und Zugriffs Dienste" installiert ist.

**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "NPS VSS Writer".

Die Writer-ID für den NPS-VSS Writer lautet 0x35e81631-13e1-48dB-97fc-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Leistungsindikatoren Writer

Dieser Writer meldet die Konfigurationsdateien des Leistungs Zählers. Diese Dateien werden nur während der Anwendungs Installation geändert und sollten während der Sicherung und Wiederherstellung des Systemstatus gesichert und wieder hergestellt werden.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt. Anfordernde Personen müssen diese Dateien manuell sichern. (Weitere Informationen finden [Sie unter Sichern und Wiederherstellen des System Status](locating-additional-system-files.md).)

Die Zeichenfolge des Writer-namens für diesen Writer ist "Performance Counters Writer".

Die Writer-ID für den leistungsindikatwriter lautet 0bada1bin-01A9-4625-8278-69e735fi39dd2.

## <a name="registry-writer"></a>Registrierungswriter

Der registrierungswriter meldet die Windows-Registrierungsdateien, um direkte Sicherungen und Wiederherstellungen der Registrierung zu ermöglichen. Benutzer Strukturen werden nicht gemeldet.

**Windows Server 2003:** In Windows Server 2003 verwendet dieser Writer eine zwischenrepository-Datei (manchmal auch als "Spit file" bezeichnet) zum Speichern von Registrierungsdaten. (Weitere Informationen finden Sie [unter Registrierungs Sicherungs-und Wiederherstellungs Vorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)

**Windows XP:** Dieser Writer wird nicht unterstützt. (Weitere Informationen finden Sie [unter Registrierungs Sicherungs-und Wiederherstellungs Vorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)

Die Zeichenfolge des Writer-namens für diesen Writer ist "Registry Writer".

Die Writer-ID für den Registrierungs Schreiber lautet AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer

Dieser Writer ist dafür verantwortlich, die Remotedesktopdienste (Terminaldienstegateway)-Gatewaydateien für Server aufzulisten, die Remotedesktop Gateway, eine unter Rolle Remotedesktopdienste Rolle, installiert haben.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

Das Remotedesktopdienste Gateway hängt von mehreren Registrierungs Schlüsseln ab, die gesichert werden und daher mit der Registrierung gesichert und wieder hergestellt werden müssen.

Die Zeichenfolge des Writer-namens für diesen Writer ist "Terminaldienstegateway-Writer".

Die Writer-ID für diesen Writer lautet 368753ec-572e-4fc7-b4b9-ccd9bdc624cb.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer

Dieser Writer ist für das Auflisten der Remotedesktopdienste Lizenzierungs Dateien (RD-Lizenzierung) bzw. Terminaldienstelizenzierungs-Dateien (Terminaldienstelizenzierung) für Server zuständig, die Remotedesktop Lizenzierung, eine unter Rolle Remotedesktopdienste Rolle, installiert haben.

**Windows Server 2003:** Dieser Writer wird nicht unterstützt.

Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.

Remotedesktopdienste Lizenzierung hängt von mehreren Registrierungs Schlüsseln ab, die gesichert werden, und muss daher mit der Registrierung gesichert und wieder hergestellt werden.

Die Zeichenfolge des Writer-namens für diesen Writer ist "termservlicensing".

Die Writer-ID für diesen Writer lautet 5382579c-98df-47a7-ac6c-98a6d7106e09.

## <a name="shadow-copy-optimization-writer"></a>Writer zur Optimierung der Schatten Kopie

Dieser Writer löscht bestimmte Dateien aus Volumeschattenkopien. Dadurch wird die Auswirkung der e/a-Vorgänge für die e/a-Kopiervorgänge während der regulären e/a-Vorgänge auf den Dateien auf dem schattenkopierten Volume minimiert. Bei den gelöschten Dateien handelt es sich in der Regel um temporäre Dateien oder Dateien, die keinen Benutzer-oder Systemstatus enthalten.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "schattenkopieoptimierungs-Writer".

Die Writer-ID für den Writer der schattenkopieoptimierung lautet 4dc3bdd4-AB48-4d07-adb0-3bee2926berd7f.

## <a name="sync-share-service-writer"></a>Synchronisierungs Freigabe Dienst-Writer

**Windows Server 2012 R2:** Dieser Writer ist in Windows Server 2012 R2 und neueren Server Versionen enthalten. Es ist nicht kompatibel mit Desktop Versionen.

Dieser Writer ist verantwortlich für das Auflisten der Synchronisierungs Freigaben auf Servern, auf denen der Synchronisierungs Freigabe Dienst installiert ist, und um sicherzustellen, dass Ihre Metadaten und Daten während der Sicherung und Wiederherstellung konsistent bleiben.

Dieser Writer ist nur vorhanden, wenn der Synchronisierungs Freigabe Dienst installiert ist und ausgeführt wird.

Es gibt eine VSS Writer Komponente für jede Synchronisierungs Freigabe. Dies schließt die Metadaten und Daten Pfade ein. Diese müssen aus Gründen der Konsistenz gesichert werden.

Die Zeichenfolge des Writer-namens lautet "Sync Share Service VSS Writer".

Die Writer-ID ist D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Systemwriter

Der System-Writer listet alle Binärdateien des Betriebssystems und des Treibers auf und ist für eine Systemstatus Sicherung erforderlich.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Dieser Writer wird als Teil des Kryptografiediensts (crypzvc) ausgeführt. Der System Schreiber generiert eine Datei Liste, die die folgenden Dateien enthält:

-   Alle statischen Dateien, die installiert wurden. Eine statische Datei ist eine Datei, die im Komponenten Manifest aufgelistet ist, wobei das Attribut " **Write Type** file" auf "static" oder "" festgelegt ist. Statische Dateien enthalten alle Dateien, die durch Windows-Ressourcenschutz (WRP) geschützt sind. Allerdings sind nicht alle statischen Dateien durch WRP geschützte Dateien. Beispielsweise sind Spieldateien statisch, aber nicht durch WRP geschützt, sodass Administratoren die Einstellungen für die Jugend Steuerung ändern können.
-   Der Inhalt des parallelen Windows-Verzeichnisses (WinSxS), einschließlich aller Manifeste, optionaler Komponenten und Win32-Dateien von Drittanbietern.
    > [!Note]  
    > Viele Dateien im Verzeichnis% windir% \\ system32 sind feste Links zu Dateien im WinSxS-Verzeichnis.

     

-   Alle PNP-Dateien für installierte Treiber (im Besitz von PNP).
-   Alle benutzermodusdienste und nicht-PnP-Treiber.
-   Alle Kataloge im Besitz von CRYP-VC.

Die Wiederherstellungs Anwendung ist dafür verantwortlich, die Dateien und die Registrierung zu schließen und die ACLs so festzulegen, dass Sie der System Schatten Kopie entsprechen. Die entsprechenden Hardlinks müssen auch erstellt werden, damit eine Systemstatus Wiederherstellung erfolgreich ist.

Die Zeichenfolge des Writer-namens für diesen Writer ist "System-Writer".

Die Writer-ID für den System Schreiber lautet E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Taskplaner Writer

Dieser Writer meldet die Aufgaben Dateien des Aufgaben Planers.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt. Anfordernde Personen müssen diese Dateien manuell sichern. (Weitere Informationen finden [Sie unter Sichern und Wiederherstellen des System Status](locating-additional-system-files.md).)

Die Zeichenfolge des Writer-namens für diesen Writer ist "Taskplaner Writer".

Die Writer-ID für den Writer ist D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>VSS-Metadatenspeicher-Writer

Dieser Writer meldet die Writer-Metadatendateien für alle VSS Express-Writer.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "VSS Express Writer Metadata Store Writer".

Die Writer-ID für den Writer ist 75dfb225-e2e4-4d39-9ac9-ffaff65ddf06.

## <a name="windows-deployment-services-wds-writer"></a>Windows-Bereitstellungs Dienste (WDS) Writer

Dieser Writer meldet die Datendateien der Windows-Bereitstellungs Dienste (WDS).

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer lautet "WDS VSS Writer".

Die Writer-ID für diesen Writer ist 82cb5521-68dB-4626-83a4-7fc6f 88853e9.

## <a name="windows-internal-database-wid-writer"></a>Interner Windows-Daten Bank Schreiber (WID)

Dieser Writer meldet die internen Windows-Daten Bank Datendateien (WID).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "widwriter".

Die Writer-ID für diesen Writer lautet 8d5194e1-e455-434a-b2e5-51296cce67df.

## <a name="windows-internet-name-service-wins-writer"></a>WINS-Writer (Windows Internet Name Service)

Dieser Writer ist für das Auflisten der für WINS erforderlichen Dateien verantwortlich.

**Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "WINS Jet Writer".

Die Writer-ID für diesen Writer ist F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>WMI-Writer

Dieser Writer wird zum Identifizieren des WMI-spezifischen Zustands und der Daten während Sicherungs Vorgängen verwendet. Die Daten enthalten Dateien aus dem WBEM-Repository.

**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.

Die Zeichenfolge des Writer-namens für diesen Writer ist "WMI Writer".

Die Writer-ID für diesen Writer ist A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
