---
description: WinMgmt ist der WMI-Dienst innerhalb des svchost-Prozesses, der unter dem &\# 0034; ausgeführt wird. LocalSystem&\# 0034; Konto.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: WinMgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351536"
---
# <a name="winmgmt"></a><span data-ttu-id="b25e0-103">WinMgmt</span><span class="sxs-lookup"><span data-stu-id="b25e0-103">winmgmt</span></span>

<span data-ttu-id="b25e0-104">WinMgmt ist der WMI-Dienst innerhalb des svchost-Prozesses, der unter dem Konto "LocalSystem" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b25e0-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="b25e0-105">In jedem Fall wird der WMI-Dienst automatisch gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace anfordert.</span><span class="sxs-lookup"><span data-stu-id="b25e0-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="b25e0-106">Weitere Informationen finden Sie unter [Starten und Beenden des WMI-Diensts](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="b25e0-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="b25e0-107">WMI ist eine Kernkomponente des Windows-Betriebssystems, mit der Entwickler und IT-Administratoren Skripts und Anwendungen schreiben können, um bestimmte Aufgaben zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="b25e0-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="b25e0-108">Winmgmt.exe ist der Dienst, mit dem WMI auf dem lokalen Computer ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b25e0-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="b25e0-109">Weitere Informationen zur Verwendung von WMI finden Sie unter [Verwenden von WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b25e0-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="b25e0-110">Wenn Sie eine Fehlermeldung bezüglich winmgmt.exe erhalten haben, finden Sie weitere Informationen unter [WMI-Problem](wmi-troubleshooting.md)Behandlung.</span><span class="sxs-lookup"><span data-stu-id="b25e0-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="b25e0-111">Weitere Informationen zu Winmgmt.exe finden Sie unter [Verwenden von WMI-Verwaltungs Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="b25e0-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="b25e0-112">Wenn der WMI-Dienst von der Eingabeaufforderung aus ausgeführt wird, verfügt er über die folgenden Schalter.</span><span class="sxs-lookup"><span data-stu-id="b25e0-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="b25e0-113">Switches</span><span class="sxs-lookup"><span data-stu-id="b25e0-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="b25e0-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/Backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="b25e0-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="b25e0-115">Bewirkt, dass WMI das Repository im angegebenen Dateinamen sichert.</span><span class="sxs-lookup"><span data-stu-id="b25e0-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="b25e0-116">Das *filename* -Argument sollte den vollständigen Pfad zum Speicherort der Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="b25e0-117">Dieser Vorgang erfordert eine Schreibsperre für das Repository, damit Schreibvorgänge in das Repository angehalten werden, bis der Sicherungs Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b25e0-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="b25e0-118">Wenn Sie keinen Pfad für die Datei angeben, wird diese im Verzeichnis% windir% \\ system32 abgelegt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="b25e0-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="b25e0-120">Stellt das WMI-Repository manuell aus der angegebenen Sicherungsdatei wieder her.</span><span class="sxs-lookup"><span data-stu-id="b25e0-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="b25e0-121">Das *filename* -Argument sollte den vollständigen Pfad zum Speicherort der Sicherungsdatei enthalten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="b25e0-122">Um den Wiederherstellungs Vorgang auszuführen, speichert WMI das vorhandene Repository, um zurückschreiben, wenn der Vorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="b25e0-123">Anschließend wird das Repository aus der Sicherungsdatei wieder hergestellt, die im *filename* -Argument angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b25e0-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="b25e0-124">Wenn exklusiver Zugriff auf das Repository nicht möglich ist, werden vorhandene Clients von WMI getrennt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="b25e0-125">Das *Flag* -Argument muss 1 (die Trennung von Benutzern und Wiederherstellung erzwingen) oder 0 (Standard Wiederherstellung, wenn keine Benutzer verbunden sind) und der Wiederherstellungs Modus sein.</span><span class="sxs-lookup"><span data-stu-id="b25e0-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<WinMgmt-Service-Process-ID>*</span><span class="sxs-lookup"><span data-stu-id="b25e0-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="b25e0-127">Registriert die Leistungs Bibliotheken des Computers bei WMI.</span><span class="sxs-lookup"><span data-stu-id="b25e0-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="b25e0-128">WMI-PID ist die Prozess-ID für den WMI-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b25e0-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="b25e0-129">Nur erforderlich, wenn die System Monitor Klassen keine zuverlässigen Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b25e0-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="b25e0-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="b25e0-131">Verschiebt den WinMgmt-Dienst in einen eigenständigen Svchost-Prozess, der über einen DCOM-Endpunkt mit fester Größe verfügt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="b25e0-132">Der Standard Endpunkt ist "ncacn \_ IP \_ TCP. 0.24158".</span><span class="sxs-lookup"><span data-stu-id="b25e0-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="b25e0-133">Der Endpunkt kann jedoch durch Ausführen von Dcomcnfg.exe geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b25e0-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="b25e0-134">Weitere Informationen zum Einrichten eines festgelegten Ports für WMI finden Sie unter [Einrichten eines Fixed-Ports für WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b25e0-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="b25e0-135">Das *Level* -Argument ist die Authentifizierungs Ebene für den Svchost-Prozess.</span><span class="sxs-lookup"><span data-stu-id="b25e0-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="b25e0-136">WMI wird normalerweise als Teil eines Hosts für gemeinsame Dienste ausgeführt, und Sie können die Authentifizierungs Ebene für WMI nicht allein erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="b25e0-137">Wenn *Level* nicht angegeben wird, lautet der Standardwert 4 (**RPC-C- \_ \_ authn- \_ Ebene \_ Pkt** oder **wbemauthenticationlevelpkt**).</span><span class="sxs-lookup"><span data-stu-id="b25e0-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="b25e0-138">Sie können WMI sicherer ausführen, indem Sie die Authentifizierungs Ebene auf Paket Datenschutz (**RPC- \_ C- \_ authn- \_ Ebene \_ Pkt \_ Privacy** oder **wbemauthenticationlevelpktprivacy**) erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="b25e0-139">Die Authentifizierungs Ebenen für Visual Basic und Skripts werden in [**wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b25e0-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="b25e0-140">Informationen zu C++ finden [Sie unter Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="b25e0-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="b25e0-141">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="b25e0-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="b25e0-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="b25e0-143">Verschiebt den WinMgmt-Dienst in den freigegebenen Svchost-Prozess.</span><span class="sxs-lookup"><span data-stu-id="b25e0-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="b25e0-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="b25e0-145">Führt eine Konsistenzprüfung für das WMI-Repository aus.</span><span class="sxs-lookup"><span data-stu-id="b25e0-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="b25e0-146">Wenn Sie den Schalter **/verifyrepository** ohne das- *<path>* Argument hinzufügen, wird das liverepository überprüft, das zurzeit von WMI verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b25e0-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="b25e0-147">Wenn Sie das *path* -Argument angeben, können Sie eine beliebige gespeicherte Kopie des Repository überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="b25e0-148">In diesem Fall sollte das path-Argument den vollständigen Pfad zur gespeicherten Repository-Kopie enthalten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="b25e0-149">Beim gespeicherten Repository sollte es sich um eine Kopie des gesamten Repository-Ordners handeln.</span><span class="sxs-lookup"><span data-stu-id="b25e0-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="b25e0-150">Weitere Informationen zu den von diesem Befehl zurückgegebenen Fehlern finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b25e0-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="b25e0-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="b25e0-152">Führt eine Konsistenzprüfung für das WMI-Repository aus. Wenn eine Inkonsistenz festgestellt wird, wird das Repository neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="b25e0-153">Der Inhalt des inkonsistenten Repository wird in das neu erstellte Repository zusammengeführt, wenn es gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b25e0-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="b25e0-154">Der Vorgang "retten" funktioniert immer mit dem Repository, das vom WMI-Dienst zurzeit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b25e0-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="b25e0-155">Weitere Informationen zu den von diesem Befehl zurückgegebenen Fehlern finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b25e0-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="b25e0-156">% MOF-Dateien, die die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung enthalten, werden im Repository wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="b25e0-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="b25e0-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="b25e0-158">Das Repository wird bei der Erstinstallation des Betriebssystems auf den ursprünglichen Zustand zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="b25e0-159">MOF-Dateien, die die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung enthalten, werden im Repository wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b25e0-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b25e0-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b25e0-160">Remarks</span></span>

<span data-ttu-id="b25e0-161">Dieses Tool befindet sich im Verzeichnis% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="b25e0-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="b25e0-162">Geben Sie `WinMgmt /?` an der Eingabeaufforderung ein, um eine Liste der verfügbaren Switches zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="b25e0-163">Das WMI-Repository, das auch als CIM-Repository bezeichnet wird, ist nicht nur eine einzelne Datei, sondern eine Sammlung von Dateien im Repository-Ordner, die als Datenbank zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="b25e0-164">Wenn Sie den **/Backup** -Schalter verwenden, um das Repository zu sichern, ist die resultierende Sicherung eine einzelne komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="b25e0-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="b25e0-165">WMI gibt die Fehler **Meldung \_ interner \_ \_** Daten Bank Beschädigung (net helpmsg 1358) zurück, wenn bei einem Überprüfungs Vorgang angegeben ist, dass sich das Repository nicht in einem konsistenten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="b25e0-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="b25e0-166">Dieser Fehler kann von jedem Befehl zurückgegeben werden, der die Repository-Überprüfung ausführt, z. b. **/verifyrepository** oder **/salvagerepository**.</span><span class="sxs-lookup"><span data-stu-id="b25e0-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="b25e0-167">Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="b25e0-168">Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten.</span><span class="sxs-lookup"><span data-stu-id="b25e0-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="b25e0-169">Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.</span><span class="sxs-lookup"><span data-stu-id="b25e0-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="b25e0-170">Weitere Informationen zur Ursache des Problems erhalten Sie, indem Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="b25e0-171">Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b25e0-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="b25e0-172">Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="b25e0-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="b25e0-173">Sie können den [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="b25e0-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b25e0-174">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b25e0-174">Requirements</span></span>



| <span data-ttu-id="b25e0-175">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b25e0-175">Requirement</span></span> | <span data-ttu-id="b25e0-176">Wert</span><span class="sxs-lookup"><span data-stu-id="b25e0-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b25e0-177">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b25e0-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b25e0-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b25e0-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b25e0-179">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b25e0-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b25e0-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b25e0-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b25e0-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b25e0-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25e0-182">WMI-Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="b25e0-182">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b25e0-183">Remote Verbindung mit WMI ab Vista</span><span class="sxs-lookup"><span data-stu-id="b25e0-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

