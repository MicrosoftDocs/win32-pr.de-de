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
# <a name="in-box-vss-writers"></a><span data-ttu-id="d70c6-104">In-Box-VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-104">In-Box VSS Writers</span></span>

<span data-ttu-id="d70c6-105">Das Windows-Betriebssystem enthält eine Reihe von VSS-Writern, die für das Auflisten der Daten verantwortlich sind, die für die verschiedenen Windows-Features erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d70c6-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="d70c6-106">Diese werden als "in-Box"-Writer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d70c6-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="d70c6-107">Der MSDE-in-Box-Writer ist in Windows Vista, Windows Server 2008 und höher nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d70c6-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="d70c6-108">Stattdessen sollte der SQL Writer verwendet werden, um SQL Server-Datenbanken zu sichern.</span><span class="sxs-lookup"><span data-stu-id="d70c6-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="d70c6-109">Nur SQL Server 2005 SP2 und höher werden unter Windows Vista, Windows Server 2008 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="d70c6-110">Active Directory Domain Services (NTDS) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="d70c6-111">Active Directory-Verbunddienste (AD FS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="d70c6-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="d70c6-113">Active Directory Rights Management Services (AD RMS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="d70c6-114">ASR-Writer (Automated System Recovery)</span><span class="sxs-lookup"><span data-stu-id="d70c6-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="d70c6-115">Background Intelligent Transfer Service (Bits) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="d70c6-116">Zertifikatauthority-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="d70c6-117">Cluster Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d70c6-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="d70c6-118">Freigegebenes Clustervolume (CSV) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="d70c6-119">Datenbank-Writer der com+-Klassen Registrierung</span><span class="sxs-lookup"><span data-stu-id="d70c6-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="d70c6-120">Datendeduplizierungswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="d70c6-121">DFS-Replikation (DFSR)</span><span class="sxs-lookup"><span data-stu-id="d70c6-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="d70c6-122">DHCP-Writer (Dynamic Host Configuration-Protokoll)</span><span class="sxs-lookup"><span data-stu-id="d70c6-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="d70c6-123">Dateireplikationsdienst (File Replication Service, FRS)</span><span class="sxs-lookup"><span data-stu-id="d70c6-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="d70c6-124">Datei Server Ressourcen-Manager Writer (File Server, f)</span><span class="sxs-lookup"><span data-stu-id="d70c6-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="d70c6-125">Hyper-V-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="d70c6-126">IIS-konfigurationswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="d70c6-127">IIS-metabasiswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="d70c6-128">Microsoft Message Queuing (MSMQ) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="d70c6-129">MSSearch-dienstwriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="d70c6-130">NPS-VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="d70c6-131">Leistungsindikatoren Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="d70c6-132">Registrierungswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="d70c6-133">Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="d70c6-134">Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="d70c6-135">Writer zur Optimierung der Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="d70c6-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="d70c6-136">Synchronisierungs Freigabe Dienst-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="d70c6-137">Systemwriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="d70c6-138">Taskplaner Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="d70c6-139">VSS-Metadatenspeicher-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="d70c6-140">Windows-Bereitstellungs Dienste (WDS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="d70c6-141">Interner Windows-Daten Bank Schreiber (WID)</span><span class="sxs-lookup"><span data-stu-id="d70c6-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="d70c6-142">WINS-Writer (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="d70c6-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="d70c6-143">WMI-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="d70c6-144">Active Directory Domain Services (NTDS) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="d70c6-145">Dieser Writer meldet die NTDS-Datenbankdatei (NTDS. dit) und die zugehörigen Protokolldateien.</span><span class="sxs-lookup"><span data-stu-id="d70c6-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="d70c6-146">Diese Dateien sind erforderlich, um die Active Directory ordnungsgemäß wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="d70c6-147">Pro Domänen Controller ist nur eine NTDS. dit-Datei vorhanden, und Sie wird in den Writer-Metadaten wie im folgenden Beispiel berichtet:</span><span class="sxs-lookup"><span data-stu-id="d70c6-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="d70c6-148">Es folgt ein Beispiel, das zeigt, wie Sie Komponenten in den Metadaten des Writers auflisten:</span><span class="sxs-lookup"><span data-stu-id="d70c6-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

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

<span data-ttu-id="d70c6-149">Zum Zeitpunkt der Sicherung legt der Writer den Ablauf Zeitpunkt der Sicherung in den Sicherungs Metadaten des Writers fest.</span><span class="sxs-lookup"><span data-stu-id="d70c6-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="d70c6-150">Anforderer sollten diese Metadaten mithilfe von [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="d70c6-151">Abgelaufene Datenbanken können nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="d70c6-152">Wenn es sich bei dem Computer, der die NTDS-Datenbank enthält, um einen Domänen Controller handelt, sollte die Sicherungs Anwendung immer eine Systemstatus Sicherung auf allen Volumes mit kritischen Systemstatus Informationen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="d70c6-153">Zum Zeitpunkt der Wiederherstellung sollte die Anwendung den Computer zunächst im Verzeichnisdienst-Wiederherstellungs Modus neu starten und dann eine Systemstatus Wiederherstellung durchführen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="d70c6-154">Die Zeichenfolge des Writer-namens für diesen Writer ist "NTDS".</span><span class="sxs-lookup"><span data-stu-id="d70c6-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="d70c6-155">Die Writer-ID für diesen Writer ist B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="d70c6-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="d70c6-156">Active Directory-Verbunddienste (AD FS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="d70c6-157">Dieser Writer meldet die Active Directory-Verbunddienste (AD FS) (ADFS)-Datendateien.</span><span class="sxs-lookup"><span data-stu-id="d70c6-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="d70c6-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-159">Die Zeichenfolge des Writer-namens für diesen Writer ist "ADFS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="d70c6-160">Die Writer-ID für diesen Writer lautet 772c45b8-AE01-4l94-940c-94961864acad.</span><span class="sxs-lookup"><span data-stu-id="d70c6-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="d70c6-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="d70c6-162">Dieser Writer meldet die Adam-Datenbankdatei (Adamntds. dit) und die zugehörigen Protokolldateien für jede Instanz in% Program Files% \\ Microsoft Adam \\ instance *N* \\ Data, wobei *N* für die Adam-Instanznummer steht.</span><span class="sxs-lookup"><span data-stu-id="d70c6-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="d70c6-163">Diese Daten Bank Protokolldateien sind erforderlich, um ADAM-Instanzen wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="d70c6-164">**Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-165">Es folgt ein Beispiel, das zeigt, wie Sie Komponenten in den Metadaten des Writers auflisten:</span><span class="sxs-lookup"><span data-stu-id="d70c6-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

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

<span data-ttu-id="d70c6-166">Zum Zeitpunkt der Sicherung legt der Writer den Ablauf Zeitpunkt der Sicherung in den Sicherungs Metadaten fest.</span><span class="sxs-lookup"><span data-stu-id="d70c6-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="d70c6-167">Sicherungs Anwendungen sollten diese Metadaten mithilfe der [**IVssComponent:: getbackupmetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) -Methode abrufen, um zu bestimmen, ob die Datenbank abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="d70c6-168">Abgelaufene Datenbanken können nicht wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="d70c6-169">Die Zeichenfolge des Writer-namens für diesen Writer ist "Adam (Instance *N*) Writer", wobei *N* die Adam-Instanznummer ist, z. b. "Adam (instance1) Writer", "Adam (Instance2) Writer" usw.</span><span class="sxs-lookup"><span data-stu-id="d70c6-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="d70c6-170">Die Writer-ID für diesen Writer ist DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="d70c6-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="d70c6-171">Diese Writer-ID ist für alle Instanzen identisch.</span><span class="sxs-lookup"><span data-stu-id="d70c6-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="d70c6-172">Active Directory Rights Management Services (AD RMS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="d70c6-173">Dieser Writer meldet die Datendateien des Active Directory Rights Management-Diensts (AD RMS).</span><span class="sxs-lookup"><span data-stu-id="d70c6-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="d70c6-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-175">Die Zeichenfolge des Writer-namens für diesen Writer ist "AD RMS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="d70c6-176">Die Writer-ID für diesen Writer lautet 886c43b1-D455-4428-a37b-4d6b9e43f.</span><span class="sxs-lookup"><span data-stu-id="d70c6-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="d70c6-177">ASR-Writer (Automated System Recovery)</span><span class="sxs-lookup"><span data-stu-id="d70c6-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="d70c6-178">Der ASR Writer speichert die Konfiguration der Datenträger auf dem System.</span><span class="sxs-lookup"><span data-stu-id="d70c6-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="d70c6-179">Dieser Writer meldet die Start Konfigurations Datenbank (Boot Configuration Database, BCD) und ist auch für das Aufheben der Bereitstellung der Registrierungs Struktur zuständig, die die BCD während der Erstellung von Schatten Kopien darstellt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="d70c6-180">Der ASR Writer muss in alle Sicherungen eingeschlossen werden, die für die Bare-Metal-Wiederherstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d70c6-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="d70c6-181">Weitere Informationen zu ASR finden Sie unter [Verwenden der automatisierten VSS-System Wiederherstellung für die Notfall Wiederherstellung](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="d70c6-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="d70c6-182">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-183">Die Zeichenfolge des Writer-namens für diesen Writer ist "ASR Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="d70c6-184">Die Writer-ID für den ASR-Writer lautet BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="d70c6-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="d70c6-185">Background Intelligent Transfer Service (Bits) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="d70c6-186">Der Bits-Writer verwendet den Registrierungsschlüssel **FilesNotToBackup** , um Dateien aus dem Bits-Cache Ordner auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="d70c6-187">Der Standard Cache Speicherort ist% ALLUSERSPROFILE% \\ Microsoft \\ Network \\ Downloader \\ Cache.</span><span class="sxs-lookup"><span data-stu-id="d70c6-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="d70c6-188">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-189">Außerdem schließt der Bits-Writer die folgenden Dateien von der Sicherung aus: die Bits-Zustands Dateien (qmgr0. dat und qmgr1. dat), die Bits-Debugprotokolldatei und die Bits-Dateien, die teilweise heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="d70c6-190">Wenn es sich bei der Bits-Download Zieldatei um eine SMB-Datei handelt, muss das Client Konto eine Vertrauensstellung mit dem Server aufweisen, andernfalls können Sicherungen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="d70c6-191">Die Zeichenfolge des Writer-namens für diesen Writer ist "Bits Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="d70c6-192">Die Writer-ID für den Bits-Writer lautet 4969d978-be47-48b0-b100f 328l07ac1e0.</span><span class="sxs-lookup"><span data-stu-id="d70c6-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="d70c6-193">Zertifikatauthority-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-193">Certificate Authority Writer</span></span>

<span data-ttu-id="d70c6-194">Dieser Writer ist für das Auflisten der Datendateien für den Zertifikat Server zuständig.</span><span class="sxs-lookup"><span data-stu-id="d70c6-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="d70c6-195">Die Zeichenfolge des Writer-namens für diesen Writer ist "Zertifizierungsstelle".</span><span class="sxs-lookup"><span data-stu-id="d70c6-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="d70c6-196">**Windows XP:** Die Zeichenfolge des Writer-namens für diesen Writer ist "Certificate Server Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="d70c6-197">Die Writer-ID für den Writer ist 6b5b15b5-da24-4d88-B737-63063e3a1f.</span><span class="sxs-lookup"><span data-stu-id="d70c6-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="d70c6-198">Cluster Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d70c6-198">Cluster Service Writer</span></span>

<span data-ttu-id="d70c6-199">Der Cluster Dienst VSS Writer ist in der Dokumentation zur [Cluster Dienst](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) -API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="d70c6-200">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird erst ab Windows Vista mit Service Pack 1 (SP1) und Windows Server 2008 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="d70c6-201">Freigegebenes Clustervolume (CSV) VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="d70c6-202">Dieser Writer meldet die freigegebenes Clustervolume (CSV)-Datendateien.</span><span class="sxs-lookup"><span data-stu-id="d70c6-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="d70c6-203">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-204">**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-205">Die Zeichenfolge des Writer-namens für diesen Writer ist "freigegebenes Clustervolume VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="d70c6-206">Die Writer-ID für den Writer lautet 1072ae1c-e5a7-4ea1-9e4a-6l7964656570.</span><span class="sxs-lookup"><span data-stu-id="d70c6-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="d70c6-207">Datenbank-Writer der com+-Klassen Registrierung</span><span class="sxs-lookup"><span data-stu-id="d70c6-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="d70c6-208">Dieser Writer ist verantwortlich für den Inhalt des Registrierungs Verzeichnisses% systemroot% \\ .</span><span class="sxs-lookup"><span data-stu-id="d70c6-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="d70c6-209">Der com+-Katalog ist eine Datei in der% systemroot%- \\ Registrierung mit einem Namen, der dem Muster R *xxxxxxxxxxxx*. CLB folgt, wobei *xxxxxxxxxxxx* eine 12-stellige hexadezimal Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="d70c6-210">Es können möglicherweise mehrere Dateien vorhanden sein, wenn com+-Anwendungen auf dem Computer konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="d70c6-211">Die Datei, die den aktuellen com+-Katalog enthält, ist die Datei mit dem größten Wert *xxxxxxxxxxxx*.</span><span class="sxs-lookup"><span data-stu-id="d70c6-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="d70c6-212">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-213">Die com+-Klassen Registrierungsdatenbank hängt von einem Registrierungsschlüssel ab, der gesichert wird, und muss daher zusammen mit der Registrierung gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="d70c6-214">Zum Wiederherstellen der COM+-Registrierungsdatenbank muss eine Sicherungs Anwendung (Requester) die [**icomadmincatalog:: restoreregdb**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="d70c6-215">Die Zeichenfolge des Writer-namens für diesen Writer ist "com+ RegDB Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="d70c6-216">Die Writer-ID für den Datenbank-Writer der com+-Klassen Registrierung lautet 542da469-d3e1-473c-9F 4f -7847s01fc64f.</span><span class="sxs-lookup"><span data-stu-id="d70c6-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="d70c6-217">Datendeduplizierungswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-217">Data Deduplication Writer</span></span>

<span data-ttu-id="d70c6-218">Die VSS Writer für die Datendeduplizierung ist in der Dokumentation zur [Datendeduplizierung](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) -API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="d70c6-219">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-220">**Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="d70c6-221">DFS-Replikation (DFSR)</span><span class="sxs-lookup"><span data-stu-id="d70c6-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="d70c6-222">Die folgende Komponente enthält eine VSS Writer: [verteiltes Dateisystem Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders) .</span><span class="sxs-lookup"><span data-stu-id="d70c6-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="d70c6-223">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="d70c6-224">DHCP-Writer (Dynamic Host Configuration-Protokoll)</span><span class="sxs-lookup"><span data-stu-id="d70c6-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="d70c6-225">Dieser Writer ist für das Auflisten von Dateien zuständig, die für die DHCP-Server Rolle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d70c6-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="d70c6-226">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-227">Die Zeichenfolge des Writer-namens für diesen Writer ist "DHCP Jet Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="d70c6-228">Die Writer-ID für diesen Writer ist BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="d70c6-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="d70c6-229">Dateireplikationsdienst (File Replication Service, FRS)</span><span class="sxs-lookup"><span data-stu-id="d70c6-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="d70c6-230">Der Datei Replikations Dienst-Writer ist in [Sichern und Wiederherstellen eines FRS-Replicated SYSVOL-Ordners](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="d70c6-231">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="d70c6-232">Datei Server Ressourcen-Manager Writer (File Server, f)</span><span class="sxs-lookup"><span data-stu-id="d70c6-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="d70c6-233">Dieser Writer listet die für die Systemstatus Sicherung verwendeten f-Konfigurationsdateien auf.</span><span class="sxs-lookup"><span data-stu-id="d70c6-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="d70c6-234">Während des Wiederherstellungs Vorgangs wird verhindert, dass Änderungen an der Konfiguration der voll Funktions Konfiguration vorgenommen werden und die Erzwingung von Kontingenten</span><span class="sxs-lookup"><span data-stu-id="d70c6-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="d70c6-235">Nachdem die Wiederherstellung durchgeführt wurde, aktualisiert der Writer den vollständigen Dienst mit der wiederhergestellten Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d70c6-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="d70c6-236">Dieser Writer ist nur vorhanden, wenn "f" (Teil der Rolle "Dateidienste") installiert ist und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d70c6-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="d70c6-237">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-238">**Windows Server 2003:** Dieser Writer wird bis Windows Server 2003 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="d70c6-239">Die Zeichenfolge des Writer-namens für diesen Writer ist "f-Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="d70c6-240">Die Writer-ID für diesen Writer ist 12ce4370-5bb7-4C58-a76a-e5d5097e3674.</span><span class="sxs-lookup"><span data-stu-id="d70c6-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="d70c6-241">Hyper-V-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-241">Hyper-V Writer</span></span>

<span data-ttu-id="d70c6-242">Die Hyper-v-VSS Writer ist in der Dokumentation zur [Hyper-v-](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="d70c6-243">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-244">**Windows Server 2003:** Dieser Writer wird bis Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="d70c6-245">IIS-konfigurationswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-245">IIS Configuration Writer</span></span>

<span data-ttu-id="d70c6-246">Der IIS-konfigurationswriter ist für das Auflisten der IIS-Konfigurationsdateien verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d70c6-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="d70c6-247">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="d70c6-248">Anforderer ist erforderlich, um die IIS-Konfigurationsdateien zu sichern, einschließlich der .net FX machine.config-Datei oder der ASP.net-Stamm web.config Datei.</span><span class="sxs-lookup"><span data-stu-id="d70c6-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="d70c6-249">Dieser Writer sichert keine Sicherungskopie der .net FX-machine.config Datei oder der ASP.net-Stamm web.config Datei, da diese Dateien vom System-Writer aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="d70c6-250">Dieser Writer sichert alle Dateien, die sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config \\ und% windir% \\ system32 \\ inetsrv \\ config befinden, mit Ausnahme der Dateien, die vom System-Writer aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="d70c6-251">Die Writer-ID für den IIS-konfigurationswriter ist 2a40f D15-dfca-4aa8-a654-1F 8c654603.</span><span class="sxs-lookup"><span data-stu-id="d70c6-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="d70c6-252">IIS-metabasiswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-252">IIS Metabase Writer</span></span>

<span data-ttu-id="d70c6-253">Der IIS-metabasewriter (Internet Information Server) ist für das Auflisten der IIS-Metabasisdatei verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d70c6-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="d70c6-254">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="d70c6-255">Anforderer ist erforderlich, um die IIS-Metabasisdatei zu sichern.</span><span class="sxs-lookup"><span data-stu-id="d70c6-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="d70c6-256">Die Writer-ID für den IIS-metabasiswriter lautet 59b1f0cf-90EF-465F-9609-6ca8b2938366.</span><span class="sxs-lookup"><span data-stu-id="d70c6-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="d70c6-257">Microsoft Message Queuing (MSMQ) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="d70c6-258">Dieser Writer meldet die Microsoft Message Queuing Datendateien (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="d70c6-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="d70c6-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-260">Die Zeichenfolge des Writer-namens für diesen Writer lautet "MSMQ Writer (*SvcName*)", wobei *SvcName* der Name des MSMQ-Diensts ist, dem der Writer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="d70c6-261">Bei der Standardinstallation lautet der Dienst Name "MSMQ".</span><span class="sxs-lookup"><span data-stu-id="d70c6-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="d70c6-262">Bei gruppierten Instanzen lautet der Dienst Name MSMQ $*resourceName*, wobei *resourceName* der geclusterte MSMQ-Ressourcen Name ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="d70c6-263">Die Writer-ID für diesen Writer lautet 7e47b561-971a-46e6-96b9-696eeaa53b2a.</span><span class="sxs-lookup"><span data-stu-id="d70c6-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="d70c6-264">MSSearch-dienstwriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-264">MSSearch Service Writer</span></span>

<span data-ttu-id="d70c6-265">Dieser Writer ist vorhanden, um Such Indexdateien aus Schatten Kopien nach der Erstellung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="d70c6-266">Dadurch wird die Auswirkung der e/a-Vorgänge für die e/a-Kopiervorgänge während der regulären e/a-Vorgänge auf den Dateien auf dem schattenkopierten Volume minimiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="d70c6-267">**Windows Server 2003:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-268">Um diesen Writer auf dem Server zu installieren, müssen Sie die Rolle "Dateidienste" installieren und den Windows-Suchdienst aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d70c6-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="d70c6-269">Die Zeichenfolge des Writer-namens für diesen Writer ist "MSSearch-dienstwriter".</span><span class="sxs-lookup"><span data-stu-id="d70c6-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="d70c6-270">Die Writer-ID für den MSSearch-Dienst Schreiber lautet CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="d70c6-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="d70c6-271">NPS-VSS-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-271">NPS VSS Writer</span></span>

<span data-ttu-id="d70c6-272">Der NPS-Writer ist für das Auflisten der Netzwerk Richtlinien Server-Konfigurationsdateien (Network Policy Server, NPS) für Server zuständig, auf denen die Rolle "Netzwerk Richtlinien-und Zugriffs Dienste" installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="d70c6-273">**Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird bis Windows Vista mit SP1 und Windows Server 2008 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="d70c6-274">Die Zeichenfolge des Writer-namens für diesen Writer ist "NPS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="d70c6-275">Die Writer-ID für den NPS-VSS Writer lautet 0x35e81631-13e1-48dB-97fc-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="d70c6-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="d70c6-276">Leistungsindikatoren Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-276">Performance Counters Writer</span></span>

<span data-ttu-id="d70c6-277">Dieser Writer meldet die Konfigurationsdateien des Leistungs Zählers.</span><span class="sxs-lookup"><span data-stu-id="d70c6-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="d70c6-278">Diese Dateien werden nur während der Anwendungs Installation geändert und sollten während der Sicherung und Wiederherstellung des Systemstatus gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="d70c6-279">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="d70c6-280">Anfordernde Personen müssen diese Dateien manuell sichern.</span><span class="sxs-lookup"><span data-stu-id="d70c6-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="d70c6-281">(Weitere Informationen finden [Sie unter Sichern und Wiederherstellen des System Status](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="d70c6-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="d70c6-282">Die Zeichenfolge des Writer-namens für diesen Writer ist "Performance Counters Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="d70c6-283">Die Writer-ID für den leistungsindikatwriter lautet 0bada1bin-01A9-4625-8278-69e735fi39dd2.</span><span class="sxs-lookup"><span data-stu-id="d70c6-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="d70c6-284">Registrierungswriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-284">Registry Writer</span></span>

<span data-ttu-id="d70c6-285">Der registrierungswriter meldet die Windows-Registrierungsdateien, um direkte Sicherungen und Wiederherstellungen der Registrierung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="d70c6-286">Benutzer Strukturen werden nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="d70c6-286">It does not report user hives.</span></span>

<span data-ttu-id="d70c6-287">**Windows Server 2003:** In Windows Server 2003 verwendet dieser Writer eine zwischenrepository-Datei (manchmal auch als "Spit file" bezeichnet) zum Speichern von Registrierungsdaten.</span><span class="sxs-lookup"><span data-stu-id="d70c6-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="d70c6-288">(Weitere Informationen finden Sie [unter Registrierungs Sicherungs-und Wiederherstellungs Vorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="d70c6-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="d70c6-289">**Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="d70c6-290">(Weitere Informationen finden Sie [unter Registrierungs Sicherungs-und Wiederherstellungs Vorgänge unter VSS](registry-backup-and-restore-operations-under-vss.md).)</span><span class="sxs-lookup"><span data-stu-id="d70c6-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="d70c6-291">Die Zeichenfolge des Writer-namens für diesen Writer ist "Registry Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="d70c6-292">Die Writer-ID für den Registrierungs Schreiber lautet AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="d70c6-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="d70c6-293">Remotedesktopdienste (Terminal Dienste) Gateway VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="d70c6-294">Dieser Writer ist dafür verantwortlich, die Remotedesktopdienste (Terminaldienstegateway)-Gatewaydateien für Server aufzulisten, die Remotedesktop Gateway, eine unter Rolle Remotedesktopdienste Rolle, installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d70c6-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="d70c6-295">**Windows Server 2003:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-296">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-297">Das Remotedesktopdienste Gateway hängt von mehreren Registrierungs Schlüsseln ab, die gesichert werden und daher mit der Registrierung gesichert und wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="d70c6-298">Die Zeichenfolge des Writer-namens für diesen Writer ist "Terminaldienstegateway-Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="d70c6-299">Die Writer-ID für diesen Writer lautet 368753ec-572e-4fc7-b4b9-ccd9bdc624cb.</span><span class="sxs-lookup"><span data-stu-id="d70c6-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="d70c6-300">Remotedesktopdienste (Terminal Dienste) Lizenzierungs-VSS Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="d70c6-301">Dieser Writer ist für das Auflisten der Remotedesktopdienste Lizenzierungs Dateien (RD-Lizenzierung) bzw. Terminaldienstelizenzierungs-Dateien (Terminaldienstelizenzierung) für Server zuständig, die Remotedesktop Lizenzierung, eine unter Rolle Remotedesktopdienste Rolle, installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d70c6-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="d70c6-302">**Windows Server 2003:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-303">Dieser Writer ist ein in-Box-Writer für Windows Server-Betriebssystemversionen. Er wird nicht im Windows-Client ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="d70c6-304">Remotedesktopdienste Lizenzierung hängt von mehreren Registrierungs Schlüsseln ab, die gesichert werden, und muss daher mit der Registrierung gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="d70c6-305">Die Zeichenfolge des Writer-namens für diesen Writer ist "termservlicensing".</span><span class="sxs-lookup"><span data-stu-id="d70c6-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="d70c6-306">Die Writer-ID für diesen Writer lautet 5382579c-98df-47a7-ac6c-98a6d7106e09.</span><span class="sxs-lookup"><span data-stu-id="d70c6-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="d70c6-307">Writer zur Optimierung der Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="d70c6-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="d70c6-308">Dieser Writer löscht bestimmte Dateien aus Volumeschattenkopien.</span><span class="sxs-lookup"><span data-stu-id="d70c6-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="d70c6-309">Dadurch wird die Auswirkung der e/a-Vorgänge für die e/a-Kopiervorgänge während der regulären e/a-Vorgänge auf den Dateien auf dem schattenkopierten Volume minimiert.</span><span class="sxs-lookup"><span data-stu-id="d70c6-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="d70c6-310">Bei den gelöschten Dateien handelt es sich in der Regel um temporäre Dateien oder Dateien, die keinen Benutzer-oder Systemstatus enthalten.</span><span class="sxs-lookup"><span data-stu-id="d70c6-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="d70c6-311">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-312">Die Zeichenfolge des Writer-namens für diesen Writer ist "schattenkopieoptimierungs-Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="d70c6-313">Die Writer-ID für den Writer der schattenkopieoptimierung lautet 4dc3bdd4-AB48-4d07-adb0-3bee2926berd7f.</span><span class="sxs-lookup"><span data-stu-id="d70c6-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="d70c6-314">Synchronisierungs Freigabe Dienst-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-314">Sync Share Service Writer</span></span>

<span data-ttu-id="d70c6-315">**Windows Server 2012 R2:** Dieser Writer ist in Windows Server 2012 R2 und neueren Server Versionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d70c6-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="d70c6-316">Es ist nicht kompatibel mit Desktop Versionen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="d70c6-317">Dieser Writer ist verantwortlich für das Auflisten der Synchronisierungs Freigaben auf Servern, auf denen der Synchronisierungs Freigabe Dienst installiert ist, und um sicherzustellen, dass Ihre Metadaten und Daten während der Sicherung und Wiederherstellung konsistent bleiben.</span><span class="sxs-lookup"><span data-stu-id="d70c6-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="d70c6-318">Dieser Writer ist nur vorhanden, wenn der Synchronisierungs Freigabe Dienst installiert ist und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d70c6-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="d70c6-319">Es gibt eine VSS Writer Komponente für jede Synchronisierungs Freigabe.</span><span class="sxs-lookup"><span data-stu-id="d70c6-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="d70c6-320">Dies schließt die Metadaten und Daten Pfade ein.</span><span class="sxs-lookup"><span data-stu-id="d70c6-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="d70c6-321">Diese müssen aus Gründen der Konsistenz gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="d70c6-322">Die Zeichenfolge des Writer-namens lautet "Sync Share Service VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="d70c6-323">Die Writer-ID ist D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="d70c6-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="d70c6-324">Systemwriter</span><span class="sxs-lookup"><span data-stu-id="d70c6-324">System Writer</span></span>

<span data-ttu-id="d70c6-325">Der System-Writer listet alle Binärdateien des Betriebssystems und des Treibers auf und ist für eine Systemstatus Sicherung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d70c6-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="d70c6-326">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-327">Dieser Writer wird als Teil des Kryptografiediensts (crypzvc) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="d70c6-328">Der System Schreiber generiert eine Datei Liste, die die folgenden Dateien enthält:</span><span class="sxs-lookup"><span data-stu-id="d70c6-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="d70c6-329">Alle statischen Dateien, die installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d70c6-329">All static files that have been installed.</span></span> <span data-ttu-id="d70c6-330">Eine statische Datei ist eine Datei, die im Komponenten Manifest aufgelistet ist, wobei das Attribut " **Write Type** file" auf "static" oder "" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="d70c6-331">Statische Dateien enthalten alle Dateien, die durch Windows-Ressourcenschutz (WRP) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="d70c6-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="d70c6-332">Allerdings sind nicht alle statischen Dateien durch WRP geschützte Dateien.</span><span class="sxs-lookup"><span data-stu-id="d70c6-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="d70c6-333">Beispielsweise sind Spieldateien statisch, aber nicht durch WRP geschützt, sodass Administratoren die Einstellungen für die Jugend Steuerung ändern können.</span><span class="sxs-lookup"><span data-stu-id="d70c6-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="d70c6-334">Der Inhalt des parallelen Windows-Verzeichnisses (WinSxS), einschließlich aller Manifeste, optionaler Komponenten und Win32-Dateien von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="d70c6-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="d70c6-335">Viele Dateien im Verzeichnis% windir% \\ system32 sind feste Links zu Dateien im WinSxS-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d70c6-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="d70c6-336">Alle PNP-Dateien für installierte Treiber (im Besitz von PNP).</span><span class="sxs-lookup"><span data-stu-id="d70c6-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="d70c6-337">Alle benutzermodusdienste und nicht-PnP-Treiber.</span><span class="sxs-lookup"><span data-stu-id="d70c6-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="d70c6-338">Alle Kataloge im Besitz von CRYP-VC.</span><span class="sxs-lookup"><span data-stu-id="d70c6-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="d70c6-339">Die Wiederherstellungs Anwendung ist dafür verantwortlich, die Dateien und die Registrierung zu schließen und die ACLs so festzulegen, dass Sie der System Schatten Kopie entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d70c6-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="d70c6-340">Die entsprechenden Hardlinks müssen auch erstellt werden, damit eine Systemstatus Wiederherstellung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d70c6-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="d70c6-341">Die Zeichenfolge des Writer-namens für diesen Writer ist "System-Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="d70c6-342">Die Writer-ID für den System Schreiber lautet E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="d70c6-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="d70c6-343">Taskplaner Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-343">Task Scheduler Writer</span></span>

<span data-ttu-id="d70c6-344">Dieser Writer meldet die Aufgaben Dateien des Aufgaben Planers.</span><span class="sxs-lookup"><span data-stu-id="d70c6-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="d70c6-345">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="d70c6-346">Anfordernde Personen müssen diese Dateien manuell sichern.</span><span class="sxs-lookup"><span data-stu-id="d70c6-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="d70c6-347">(Weitere Informationen finden [Sie unter Sichern und Wiederherstellen des System Status](locating-additional-system-files.md).)</span><span class="sxs-lookup"><span data-stu-id="d70c6-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="d70c6-348">Die Zeichenfolge des Writer-namens für diesen Writer ist "Taskplaner Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="d70c6-349">Die Writer-ID für den Writer ist D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="d70c6-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="d70c6-350">VSS-Metadatenspeicher-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="d70c6-351">Dieser Writer meldet die Writer-Metadatendateien für alle VSS Express-Writer.</span><span class="sxs-lookup"><span data-stu-id="d70c6-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="d70c6-352">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-353">Die Zeichenfolge des Writer-namens für diesen Writer ist "VSS Express Writer Metadata Store Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="d70c6-354">Die Writer-ID für den Writer ist 75dfb225-e2e4-4d39-9ac9-ffaff65ddf06.</span><span class="sxs-lookup"><span data-stu-id="d70c6-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="d70c6-355">Windows-Bereitstellungs Dienste (WDS) Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="d70c6-356">Dieser Writer meldet die Datendateien der Windows-Bereitstellungs Dienste (WDS).</span><span class="sxs-lookup"><span data-stu-id="d70c6-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="d70c6-357">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-358">Die Zeichenfolge des Writer-namens für diesen Writer lautet "WDS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="d70c6-359">Die Writer-ID für diesen Writer ist 82cb5521-68dB-4626-83a4-7fc6f 88853e9.</span><span class="sxs-lookup"><span data-stu-id="d70c6-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="d70c6-360">Interner Windows-Daten Bank Schreiber (WID)</span><span class="sxs-lookup"><span data-stu-id="d70c6-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="d70c6-361">Dieser Writer meldet die internen Windows-Daten Bank Datendateien (WID).</span><span class="sxs-lookup"><span data-stu-id="d70c6-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="d70c6-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-363">Die Zeichenfolge des Writer-namens für diesen Writer ist "widwriter".</span><span class="sxs-lookup"><span data-stu-id="d70c6-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="d70c6-364">Die Writer-ID für diesen Writer lautet 8d5194e1-e455-434a-b2e5-51296cce67df.</span><span class="sxs-lookup"><span data-stu-id="d70c6-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="d70c6-365">WINS-Writer (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="d70c6-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="d70c6-366">Dieser Writer ist für das Auflisten der für WINS erforderlichen Dateien verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="d70c6-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="d70c6-367">**Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-368">Die Zeichenfolge des Writer-namens für diesen Writer ist "WINS Jet Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="d70c6-369">Die Writer-ID für diesen Writer ist F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="d70c6-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="d70c6-370">WMI-Writer</span><span class="sxs-lookup"><span data-stu-id="d70c6-370">WMI Writer</span></span>

<span data-ttu-id="d70c6-371">Dieser Writer wird zum Identifizieren des WMI-spezifischen Zustands und der Daten während Sicherungs Vorgängen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d70c6-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="d70c6-372">Die Daten enthalten Dateien aus dem WBEM-Repository.</span><span class="sxs-lookup"><span data-stu-id="d70c6-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="d70c6-373">**Windows Server 2003 und Windows XP:** Dieser Writer wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d70c6-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="d70c6-374">Die Zeichenfolge des Writer-namens für diesen Writer ist "WMI Writer".</span><span class="sxs-lookup"><span data-stu-id="d70c6-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="d70c6-375">Die Writer-ID für diesen Writer ist A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="d70c6-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
