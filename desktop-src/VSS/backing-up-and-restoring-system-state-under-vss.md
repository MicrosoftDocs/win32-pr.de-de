---
description: Hinweis Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960737"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a><span data-ttu-id="16801-103">Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="16801-103">Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1</span></span>

> [!Note]  
> <span data-ttu-id="16801-104">Dieses Thema gilt nur für Windows Server 2003 R2 und Windows Server 2003 mit Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="16801-104">This topic only applies to Windows Server 2003 R2 and Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="16801-105">Informationen zu anderen Betriebssystemversionen finden Sie unter [Sichern und Wiederherstellen des Systemstatus](locating-additional-system-files.md).</span><span class="sxs-lookup"><span data-stu-id="16801-105">For information about other operating system versions, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="16801-106">Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen).</span><span class="sxs-lookup"><span data-stu-id="16801-106">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="16801-107">Weitere Informationen zur Verwendung von von Microsoft bereitgestellten APIs und Prozeduren zum Implementieren von Online-Systemstatus Wiederherstellungen finden Sie in den Communityressourcen im [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="16801-107">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

<span data-ttu-id="16801-108">Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="16801-108">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="16801-109">Diese Elemente sollten immer von Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="16801-109">These elements should always be treated by backup and restore operations as a unit.</span></span>

<span data-ttu-id="16801-110">In Windows Server 2003 R2 und Windows Server 2003 mit SP1 gibt es keine Windows-API, mit der diese Objekte als eins behandelt werden. Daher wird empfohlen, dass die anfordernde Personen über ein eigenes Systemstatus Objekt verfügen, damit diese Komponenten konsistent verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="16801-110">In Windows Server 2003 R2 and Windows Server 2003 with SP1, there is no Windows API designed to treat these objects as one, so it is recommended that requesters have their own system state object so that they can process these components in a consistent manner.</span></span>

<span data-ttu-id="16801-111">Da VSS unter Versionen von Windows ausgeführt wird, auf denen der [*Systemdatei Schutz*](vssgloss-s.md) (WFP) Systemstatus Dateien vor Beschädigungen schützt, sind spezielle Schritte erforderlich, um den Systemstatus zu sichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="16801-111">Because VSS runs on versions of Windows where [*System File Protection*](vssgloss-s.md) (WFP) protects system state files from corruption, special steps are needed to back up and restore system state.</span></span>

<span data-ttu-id="16801-112">Der System Status besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="16801-112">System state consists of the following:</span></span>

-   <span data-ttu-id="16801-113">Alle durch WFP geschützten Dateien, Startdateien einschließlich NTLDR-, ntdetect-und leistungsindikatorenkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="16801-113">All files protected by WFP, boot files including ntldr, ntdetect, and performance counter configurations</span></span>
-   <span data-ttu-id="16801-114">Die Active Directory (ADSI) (auf Systemen, die Domänen Controller sind)</span><span class="sxs-lookup"><span data-stu-id="16801-114">The Active Directory (ADSI) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="16801-115">Der Ordner "System Volume" (SYSVOL), der vom Datei Replikations Dienst (File Replication Service, FRS) repliziert wird (auf Systemen mit Domänen Controllern</span><span class="sxs-lookup"><span data-stu-id="16801-115">The System Volume Folder (SYSVOL) that is replicated by the File Replication Service (FRS) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="16801-116">Zertifikat Server (auf Systemen, die eine Zertifizierungsstelle bereitstellen)</span><span class="sxs-lookup"><span data-stu-id="16801-116">Certificate server (on systems that provide Certification Authority)</span></span>
-   <span data-ttu-id="16801-117">Cluster Datenbank (auf Systemen, die ein Knoten eines Windows-Clusters sind)</span><span class="sxs-lookup"><span data-stu-id="16801-117">Cluster database (on systems that are a node of a Windows cluster)</span></span>
-   <span data-ttu-id="16801-118">Registrierungsdienst</span><span class="sxs-lookup"><span data-stu-id="16801-118">Registry service</span></span>
-   <span data-ttu-id="16801-119">Com+-Klassen Registrierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="16801-119">COM+ class registration database</span></span>

<span data-ttu-id="16801-120">Der Systemstatus kann in beliebiger Reihenfolge gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="16801-120">The system state can be backed up in any order.</span></span>

<span data-ttu-id="16801-121">Allerdings sollte die Wiederherstellung des Systemstatus zuerst Startdateien ersetzen und den System Abschnitt (Hive) der Registrierung als letzten Schritt im Prozess ausführen und kann in der folgenden Reihenfolge vorkommen:</span><span class="sxs-lookup"><span data-stu-id="16801-121">However, the restoration of the system state should replace boot files first and commit the system section (hive) of the registry as a final step in the process, and might occur in the following order:</span></span>

1.  <span data-ttu-id="16801-122">Stellen Sie die Startdateien wieder her.</span><span class="sxs-lookup"><span data-stu-id="16801-122">Restore the boot files.</span></span>
2.  <span data-ttu-id="16801-123">Com+-Klassen Registrierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="16801-123">COM+ class registration database</span></span>
3.  <span data-ttu-id="16801-124">Stellen Sie SYSVOL, den Zertifikat Server und die Cluster Datenbanken (falls erforderlich) wieder her.</span><span class="sxs-lookup"><span data-stu-id="16801-124">Restore SYSVOL, Certificate Server, and Cluster databases (if needed).</span></span>
4.  <span data-ttu-id="16801-125">Restore Active Directory (falls erforderlich).</span><span class="sxs-lookup"><span data-stu-id="16801-125">Restore Active Directory (if needed).</span></span>
5.  <span data-ttu-id="16801-126">Stellen Sie die Registrierung wieder her.</span><span class="sxs-lookup"><span data-stu-id="16801-126">Restore the registry.</span></span>

<span data-ttu-id="16801-127">Einige Systemdienste, z. b. die Zertifizierungsstelle, haben konventionelle VSS-Writer und befolgen die VSS-Sicherungs-und-Wiederherstellungs Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="16801-127">Some system services, such as the Certification Authority, have conventional VSS writers and follow the VSS backup and restore algorithms.</span></span> <span data-ttu-id="16801-128">Andere, wie z. b. die Registrierung, erfordern benutzerdefinierte Sicherungs-oder Wiederherstellungs Vorgänge. Weitere Informationen finden Sie unter [benutzerdefinierte Sicherungen und](custom-backups-and-restores.md)Wiederherstellungen.</span><span class="sxs-lookup"><span data-stu-id="16801-128">Others, such as the registry, require custom backup or restore operations; for more information, see [Custom Backups and Restores](custom-backups-and-restores.md).</span></span>

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a><span data-ttu-id="16801-129">VSS-Sicherung und-Wiederherstellung von Start-und System Dateien</span><span class="sxs-lookup"><span data-stu-id="16801-129">VSS Backup and Restores of Boot and System Files</span></span>

<span data-ttu-id="16801-130">Die Start-und Systemdateien sollten nur als einzelne Entität gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="16801-130">The boot and system files should be backed up and restored only as a single entity.</span></span>

<span data-ttu-id="16801-131">Ein Anforderer kann auf sichere Weise schattenkopierte Versionen dieser Dateien verwenden und muss sicherstellen, dass das System Volume und das Startgerät als [*Schatten kopiert*](vssgloss-s.md)werden.</span><span class="sxs-lookup"><span data-stu-id="16801-131">A requester can safely use shadow-copied versions of these files, and should be sure that the system volume and boot device are [*shadow copied*](vssgloss-s.md).</span></span>

<span data-ttu-id="16801-132">Die System-und Startdateien umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16801-132">The system and boot files include:</span></span>

-   <span data-ttu-id="16801-133">Die Core-Startdateien:</span><span class="sxs-lookup"><span data-stu-id="16801-133">The core boot files:</span></span> <dl> <span data-ttu-id="16801-134">NtLdr.exe</span><span class="sxs-lookup"><span data-stu-id="16801-134">NtLdr.exe</span></span>  
    <span data-ttu-id="16801-135">Boot.ini</span><span class="sxs-lookup"><span data-stu-id="16801-135">Boot.ini</span></span>  
    <span data-ttu-id="16801-136">NtDetect.com</span><span class="sxs-lookup"><span data-stu-id="16801-136">NtDetect.com</span></span>  
    <span data-ttu-id="16801-137">NtBootDD.sys (sofern vorhanden)</span><span class="sxs-lookup"><span data-stu-id="16801-137">NtBootDD.sys (if present)</span></span>  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> <span data-ttu-id="16801-138">% SystemRoot% System32-Stammverzeichnis \\ \\ \\ {F750E6C3-38EE-11d1-85E5-00C04FC295EE}</span><span class="sxs-lookup"><span data-stu-id="16801-138">%SystemRoot%\\System32\\CatRoot\\{F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span></span> </dl><span data-ttu-id="16801-139">
-   Alle Dateien, die vom [\*System Datei Schutz*](vssgloss-s.md) geschützt und durch [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) aufgelistet werden (siehe VSS-Wiederherstellungs Vorgänge von WFP-geschützten Dateien) -   :</span><span class="sxs-lookup"><span data-stu-id="16801-139">
-   All files protected by [\*System File Protection*](vssgloss-s.md) and enumerated by [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (see VSS Restore Operations of WFP Protected Files) -   The Performance Counter Configuration files:</span></span> <dl> <span data-ttu-id="16801-140">% Systemroot% \\ system32 \\ perf? 00?. Hütte</span><span class="sxs-lookup"><span data-stu-id="16801-140">%SystemRoot%\\System32\\Perf?00?.dat</span></span>  
    <span data-ttu-id="16801-141">% Systemroot% \\ system32 \\ perf? 00?. BAK</span><span class="sxs-lookup"><span data-stu-id="16801-141">%SystemRoot%\\System32\\Perf?00?.bak</span></span> </dl><span data-ttu-id="16801-142">
-   Falls vorhanden, sollte die Internet Information Server (IIS)-Metabasisdatei in Sicherungs-und Wiederherstellungs Vorgänge eingeschlossen werden, da Sie einen von Microsoft Exchange und anderen Netzwerkanwendungen verwendeten Status enthält.</span><span class="sxs-lookup"><span data-stu-id="16801-142">
-   If present, the Internet Information Server (IIS) metabase file should be included in backup and restore operations because it contains state that is used by Microsoft Exchange and other network applications.</span></span> <span data-ttu-id="16801-143">Diese Datei befindet sich unter:</span><span class="sxs-lookup"><span data-stu-id="16801-143">This file can be found at:</span></span> <dl> <span data-ttu-id="16801-144">% Systemroot% \\ system32 \\ inetsrv \\ MetaBase. bin</span><span class="sxs-lookup"><span data-stu-id="16801-144">%SystemRoot%\\System32\\InetSrv\\Metabase.bin</span></span> </dl><span data-ttu-id="16801-145">
-   Wenn die IIS-Metabasisdatei gesichert ist, sollten Schlüssel zum Aktivieren von Anwendungen zum Lesen bestimmter verschlüsselter Einträge als Teil des Systemstatus wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="16801-145">
-   If the IIS metabase file is backed up, keys to enable applications to read certain encrypted entries should be restored as part of the system state.</span></span> <span data-ttu-id="16801-146">Die Dateien finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="16801-146">The files can be found under:</span></span> <dl> <span data-ttu-id="16801-147">% Systemroot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="16801-147">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
    <span data-ttu-id="16801-148">% ALLUSERSPROFILE% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="16801-148">%AllUsersProfile%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span> </dl><span data-ttu-id="16801-149">
-Beim Sichern von Start-und Systemdateien ist es möglicherweise erforderlich, das DOS-Startgerät zu ermitteln, indem Sie die folgenden Schritte ausführen: 1. Suchen der Systempartition unter \*\*HKEY \_ local \_ Machine*\* \\ \*\*System*\* \\ \*\*Setup*\* \\ \*\*Systempartition\**.</span><span class="sxs-lookup"><span data-stu-id="16801-149">
-   When backing up boot and system files, it may become necessary to determine the DOS boot device by doing the following: 1.  Find the system partition under \*\*HKEY\_LOCAL\_MACHINE\*\*\\*\*System\*\*\\*\*Setup\*\*\\*\*SystemPartition\**.</span></span>
    <span data-ttu-id="16801-150">2.  Übergeben Sie die System Stamm-Umgebungsvariable (% SystemRoot%). zum Abrufen des NT-Geräte namens an den Mount Manager.</span><span class="sxs-lookup"><span data-stu-id="16801-150">2.  Pass the System Root environment variable (%SystemRoot%) to the mount manager to obtain the NT device name.</span></span>

## <a name="vss-restore-operations-of-wfp-protected-files"></a><span data-ttu-id="16801-151">VSS-Wiederherstellungs Vorgänge von WFP-geschützten Dateien</span><span class="sxs-lookup"><span data-stu-id="16801-151">VSS Restore Operations of WFP Protected Files</span></span>

<span data-ttu-id="16801-152">Der WFP-Dienst ist so konzipiert, dass die versehentliche oder schrittweise Ersetzung von Systemdateien verhindert wird.</span><span class="sxs-lookup"><span data-stu-id="16801-152">The WFP service is designed to prevent accidental or piecemeal replacement of system files.</span></span> <span data-ttu-id="16801-153">Daher müssen spezielle Schritte ausgeführt werden, um WFP-Daten wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="16801-153">Therefore, special steps need to be undertaken to restore WFP data.</span></span>

<span data-ttu-id="16801-154">Der bedeutet, dass der WFP-Writer beim Definieren seines Writer-Metadatendokuments die **VSS- \_ RME- \_ Wiederherstellung \_ beim \_** Wiederherstellen des Dokuments angeben soll.</span><span class="sxs-lookup"><span data-stu-id="16801-154">The means the WFP writer should specify the **VSS\_RME\_RESTORE\_AT\_REBOOT** restore method when defining its Writer Metadata Document.</span></span> <span data-ttu-id="16801-155">Wenn ein Anforderer feststellt, dass der WFP-Writer diese Wiederherstellungsmethode nicht angeben konnte, weist dies auf einen Writer-Fehler hin.</span><span class="sxs-lookup"><span data-stu-id="16801-155">If a requester determines that the WFP writer has failed to specify this restore method, it indicates a writer error.</span></span>

<span data-ttu-id="16801-156">Ein Anforderer muss beim Neustart eine Wiederherstellungsmethode der **VSS- \_ RME- \_ Wiederherstellung \_ \_** implementieren, indem er die Win32-Funktion " [**muvefileex**](/windows/win32/api/winbase/nf-winbase-movefileexa) " mit dem Parameter "verzögertes Verschieben von" in " **muvefile \_ \_ \_** "</span><span class="sxs-lookup"><span data-stu-id="16801-156">A requester should implement a restore method of **VSS\_RME\_RESTORE\_AT\_REBOOT** using the Win32 function [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) with the **MOVEFILE\_DELAY\_UNTIL\_REBOOT** parameter to replace system files.</span></span> <span data-ttu-id="16801-157">Die wiederhergestellten Dateien werden erst nach dem Neustart des Systems in die eigentlichen System Dateiverzeichnisse kopiert.</span><span class="sxs-lookup"><span data-stu-id="16801-157">The restored files are not copied into the actual system file directories until after system reboot.</span></span> <span data-ttu-id="16801-158">Das Überschreiben geschützter Systemdateien findet nur statt, wenn der Wert des folgenden Registrierungs Eintrags von **reg \_ Word** auf 1 festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="16801-158">The overwriting of protected system files will occur only if the value of the following **REG\_WORD** registry entry is set to 1:</span></span>

<span data-ttu-id="16801-159">**HKEY \_ Lokaler \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **allowprotectedrenames** = 1</span><span class="sxs-lookup"><span data-stu-id="16801-159">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**AllowProtectedRenames** = 1</span></span>

<span data-ttu-id="16801-160">Dieser Wert muss vor jedem Start festgelegt werden, bei dem geschützte Dateien über " [**muvefileex**](/windows/win32/api/winbase/nf-winbase-movefileexa) " ersetzt und nach dem Neustart gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="16801-160">This value must be set before any boot where protected files are to be replaced via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and is deleted after reboot.</span></span>

<span data-ttu-id="16801-161">Das System-dllcache-Verzeichnis sollte auch mit der Sicherung und Wiederherstellung des Start Datentyps gesichert oder wieder hergestellt werden, und es befindet sich in dem Registrierungs Eintrag **reg \_ Expand \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="16801-161">The system dllcache directory should also be backed up or restored, with boot volume backup and restore, and is located by examining the **REG\_EXPAND\_SZ** registry entry:</span></span>

<span data-ttu-id="16801-162">**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **sfcdllcache**</span><span class="sxs-lookup"><span data-stu-id="16801-162">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**SfcDllCache**</span></span><dl> <dt>

                  Data type
</dt> <dd>                  <span data-ttu-id="16801-163">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="16801-163">REG\_EXPAND\_SZ</span></span></dd> </dl>

<span data-ttu-id="16801-164">Der Inhalt des Verzeichnisses System dllcache wird mithilfe der Systemdatei Prüfung (SFC) an der Eingabeaufforderung neu erstellt:</span><span class="sxs-lookup"><span data-stu-id="16801-164">The contents of the system dllcache directory are rebuilt by using the System File Checker (SFC) from the command prompt:</span></span>

-   <span data-ttu-id="16801-165">Die Option **/scanonce** scannt alle geschützten Dateien beim nächsten Systemstart.</span><span class="sxs-lookup"><span data-stu-id="16801-165">The **/SCANONCE** option scans all protected files at the next system boot.</span></span>
-   <span data-ttu-id="16801-166">Die Option **/scannow** scannt alle geschützten Dateien sofort.</span><span class="sxs-lookup"><span data-stu-id="16801-166">The **/SCANNOW** option scans all protected files immediately.</span></span>

<span data-ttu-id="16801-167">Alle geschützten Dateien werden überprüft, und alle ungültigen Versionen werden im Verzeichnis und im Dllcache-Speicherort ersetzt.</span><span class="sxs-lookup"><span data-stu-id="16801-167">All protected files will be scanned, and any versions that are not valid will be replaced in both the directory and dllcache location.</span></span>

<span data-ttu-id="16801-168">Es gibt vier Dateien, die Teil des WFP sind und nicht mit den WFP-Dateien wieder hergestellt werden können:</span><span class="sxs-lookup"><span data-stu-id="16801-168">There are four files that are part of the WFP that cannot be restored with the WFP files:</span></span>

<dl> <span data-ttu-id="16801-169">Ctl3dv2.dll</span><span class="sxs-lookup"><span data-stu-id="16801-169">Ctl3dv2.dll</span></span>  
<span data-ttu-id="16801-170">DtcSetup.exe</span><span class="sxs-lookup"><span data-stu-id="16801-170">DtcSetup.exe</span></span>  
<span data-ttu-id="16801-171">NtDll.dll</span><span class="sxs-lookup"><span data-stu-id="16801-171">NtDll.dll</span></span>  
<span data-ttu-id="16801-172">Smss.exe</span><span class="sxs-lookup"><span data-stu-id="16801-172">Smss.exe</span></span>  
</dl>

<span data-ttu-id="16801-173">Diese Dateien helfen bei der Wiederherstellung der WFP-Dateien, sodass eine zirkuläre Abhängigkeit vorliegt.</span><span class="sxs-lookup"><span data-stu-id="16801-173">These files help in the process of restoring the WFP files and as such there is a circular dependency.</span></span> <span data-ttu-id="16801-174">Zurzeit gibt es keine Möglichkeit, diese Dateien wiederherzustellen, außer um Windows neu zu installieren.</span><span class="sxs-lookup"><span data-stu-id="16801-174">Currently, there is no way to restore these files except to reinstall Windows.</span></span>

 

 
