---
description: Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert. Diese Elemente sollten bei Sicherungs-und Wiederherstellungs Vorgängen immer als Einheit behandelt werden.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Sichern und Wiederherstellen des System Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755544"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="e0f88-104">Sichern und Wiederherstellen des System Status</span><span class="sxs-lookup"><span data-stu-id="e0f88-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="e0f88-105">Dieses Thema gilt für Windows Vista, Windows Server 2008 und höher.</span><span class="sxs-lookup"><span data-stu-id="e0f88-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="e0f88-106">Informationen zu Windows Server 2003 finden Sie unter [Sichern und Wiederherstellen des System Status in Windows Server 2003 R2 und Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md) .</span><span class="sxs-lookup"><span data-stu-id="e0f88-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="e0f88-107">Beim Ausführen einer VSS-Sicherung oder-Wiederherstellung wird der Windows-Systemstatus als eine Sammlung mehrerer wichtiger Betriebssystem Elemente und der zugehörigen Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="e0f88-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="e0f88-108">Diese Elemente sollten bei Sicherungs-und Wiederherstellungs Vorgängen immer als Einheit behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="e0f88-109">Microsoft bietet keinen technischen Support für Entwickler oder IT-Experten für die Implementierung von Online-Systemstatus Wiederherstellungen unter Windows (alle Versionen).</span><span class="sxs-lookup"><span data-stu-id="e0f88-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="e0f88-110">Wenn Sie den Systemstatus sichern und wiederherstellen, empfiehlt es sich, zusätzlich zu den Dateien, die von den systemstatuswritern aufgelistet werden, die System-und Startvolumes zu sichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="e0f88-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="e0f88-111">Systemstatuswriter sind Writer, für die das [**VSS \_ Usage \_ Type**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) -Attribut entweder auf VSS- \_ UT \_ bootablesystemstate oder VSS \_ UT \_ Systemservice festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0f88-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0f88-112">Wenn ein VSS-Writer durch seinen [**VSS- \_ \_ Verwendungstyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) als systemstatuswriter identifiziert wird, muss er in eine Systemstatus Sicherung eingeschlossen werden, auch wenn er auswählbar ist.</span><span class="sxs-lookup"><span data-stu-id="e0f88-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="e0f88-113">Zusätzlich zu den aufgelisteten Betriebssystem-und Treiber Binärdateien, die vom Systemstatus Schreiber aufgelistet werden, gibt es bestimmte andere Dateien, die als Teil des Systemstatus gesichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e0f88-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="e0f88-114">Alle von einem VSS-systemstatuswriter gemeldeten Komponenten sind Teil des Systemstatus, außer denen, für die das VSS \_ CF- \_ Flag "nicht- \_ Systemstatus" \_ festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0f88-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="e0f88-115">Sicherungs Programme sollten auch den **lastrestoreid** -Registrierungsschlüssel festlegen.</span><span class="sxs-lookup"><span data-stu-id="e0f88-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="e0f88-116">Weitere Informationen finden Sie unter [Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="e0f88-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="e0f88-117">In Windows Vista, Windows Server 2008 und höher wurden die Namen und Speicherorte einiger Systemdateien wie folgt geändert.</span><span class="sxs-lookup"><span data-stu-id="e0f88-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="e0f88-118">Systemstatus</span><span class="sxs-lookup"><span data-stu-id="e0f88-118">System State</span></span>

<span data-ttu-id="e0f88-119">Für Windows Server 2012 und höher müssen zusätzlich zu den Dateien, die von den verschiedenen VSS-Systemstatus-Writern gemeldet werden, nur die folgenden Lizenzierungs Dateien explizit eingeschlossen werden, und die folgenden DRM-Dateien müssen explizit ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="e0f88-120">Digitale Rights Management Dateien für Windows Media</span><span class="sxs-lookup"><span data-stu-id="e0f88-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="e0f88-121">In Windows Server 2008 und höher sind die folgenden Dateien, einschließlich aller Unterverzeichnisse unter folgendem Pfad, aus dem Systemstatus ausgeschlossen und dürfen nicht gesichert werden:</span><span class="sxs-lookup"><span data-stu-id="e0f88-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="e0f88-122">% Program Data% \\ Microsoft \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="e0f88-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="e0f88-123">Dies ersetzt die Informationen im Abschnitt Windows Media Digital Rights Management unter [Arbeiten mit Datei System-und Sicherheits Features](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="e0f88-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="e0f88-124">Leistungsindikatationsdateien</span><span class="sxs-lookup"><span data-stu-id="e0f88-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="e0f88-125">Die Leistungsdaten-Konfigurationsdateien befinden sich im Verzeichnis% systemroot% \\ system32 \\ und haben die folgenden Namen:</span><span class="sxs-lookup"><span data-stu-id="e0f88-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="e0f88-126">Leistung? 00?. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-126">Perf?00?.dat</span></span>  
<span data-ttu-id="e0f88-127">Perfc0??. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-127">Perfc0??.dat</span></span>  
<span data-ttu-id="e0f88-128">Perfd0??. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-128">Perfd0??.dat</span></span>  
<span data-ttu-id="e0f88-129">Perfh0??. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-129">Perfh0??.dat</span></span>  
<span data-ttu-id="e0f88-130">Perfi0??. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-130">Perfi0??.dat</span></span>  
<span data-ttu-id="e0f88-131">Prfc0???. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-131">Prfc0???.dat</span></span>  
<span data-ttu-id="e0f88-132">Prfd0???. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-132">Prfd0???.dat</span></span>  
<span data-ttu-id="e0f88-133">Prfh0???. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-133">Prfh0???.dat</span></span>  
<span data-ttu-id="e0f88-134">Prfi0???. Hütte</span><span class="sxs-lookup"><span data-stu-id="e0f88-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="e0f88-135">Diese Dateien werden nur während der Anwendungs Installation geändert und sollten während der Sicherung und Wiederherstellung des Systemstatus gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="e0f88-136">IIS-Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="e0f88-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="e0f88-137">In Windows Vista mit Service Pack 1 (SP1) und höher sollten Sie diese Dateien nicht sichern.</span><span class="sxs-lookup"><span data-stu-id="e0f88-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="e0f88-138">Verwenden Sie stattdessen den in-Box-IIS-konfigurationswriter.</span><span class="sxs-lookup"><span data-stu-id="e0f88-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="e0f88-139">Weitere Informationen zu diesem Writer finden Sie unter [in-Box-VSS-Writer](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="e0f88-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="e0f88-140">Die relevanten IIS-Konfigurationsdateien und ihre Speicherorte sind unten aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="e0f88-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="e0f88-141">Die .net FX-machine.config Datei befindet sich im Framework Version-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e0f88-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="e0f88-142">Die ASP.net-Stamm web.config Datei befindet sich im Framework-Versions Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e0f88-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="e0f88-143">Die Konfigurationsdateien für .net FX und ASP.net befinden sich im Framework Version-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="e0f88-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="e0f88-144">Wenn mehrere Versionen des Frameworks auf dem Computer installiert sind, enthält dieses Verzeichnis eine Konfigurationsdatei für jede installierte Version.</span><span class="sxs-lookup"><span data-stu-id="e0f88-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="e0f88-145">Die IIS-applicationHost.config zentrale Konfigurationsdatei befindet sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="e0f88-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="e0f88-146">Damit der Server diese Konfigurationsdatei versteht, sind Schema Dateien vorhanden, die die Grammatik und Struktur bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e0f88-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="e0f88-147">Diese Dateien befinden sich im Verzeichnis% windir% \\ system32 \\ inetsrv \\ config \\ Schema.</span><span class="sxs-lookup"><span data-stu-id="e0f88-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="e0f88-148">Der Verzeichnispfad der Frameworkversion ist im folgenden Registrierungsschlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="e0f88-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="e0f88-149">**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ . NETFramework- \\ InstallRoot**</span><span class="sxs-lookup"><span data-stu-id="e0f88-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="e0f88-150">Außerdem müssen die folgenden Kryptografieschlüssel gesichert werden:</span><span class="sxs-lookup"><span data-stu-id="e0f88-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="e0f88-151">% Program Data% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="e0f88-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="e0f88-152">% Systemroot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="e0f88-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="e0f88-153">Frameworkdateien</span><span class="sxs-lookup"><span data-stu-id="e0f88-153">Framework Files</span></span>

<span data-ttu-id="e0f88-154">Alle Versionen von .NET Framework müssen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="e0f88-155">Die Dateien befinden sich in einem oder beiden der folgenden Verzeichnisse:</span><span class="sxs-lookup"><span data-stu-id="e0f88-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="e0f88-156">% windir% \\ Microsoft.net \\ Framework</span><span class="sxs-lookup"><span data-stu-id="e0f88-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="e0f88-157">% windir% \\ Microsoft.net \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="e0f88-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="e0f88-158">Außerdem müssen die Assemblydateien gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="e0f88-159">Diese Dateien befinden sich im folgenden Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="e0f88-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="e0f88-160">% windir% \\ Assembly</span><span class="sxs-lookup"><span data-stu-id="e0f88-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="e0f88-161">Taskplaner von Aufgaben Dateien</span><span class="sxs-lookup"><span data-stu-id="e0f88-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="e0f88-162">Die Aufgaben Dateien des Aufgaben Planers müssen gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="e0f88-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="e0f88-163">Die Dateien befinden sich an einem oder beiden der folgenden Speicherorte:</span><span class="sxs-lookup"><span data-stu-id="e0f88-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="e0f88-164">% windir% \\ system32 \\ Tasks und alle Unterverzeichnisse (rekursiv)</span><span class="sxs-lookup"><span data-stu-id="e0f88-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="e0f88-165">% windir% \\ Tasks (keine Unterverzeichnisse)</span><span class="sxs-lookup"><span data-stu-id="e0f88-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
