---
description: BETest ist ein VSS-Anforderer, der erweiterte Sicherungs-und Wiederherstellungs Vorgänge testet.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Test Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7559c304532b337214108435b740595897694f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868768"
---
# <a name="betest-tool"></a><span data-ttu-id="00fc6-103">Test Tool</span><span class="sxs-lookup"><span data-stu-id="00fc6-103">BETest Tool</span></span>

<span data-ttu-id="00fc6-104">BETest ist ein VSS-Anforderer, der erweiterte Sicherungs-und Wiederherstellungs Vorgänge testet.</span><span class="sxs-lookup"><span data-stu-id="00fc6-104">BETest is a VSS requester that tests advanced backup and restore operations.</span></span> <span data-ttu-id="00fc6-105">Dieses Tool kann verwendet werden, um die Verwendung komplexer VSS-Funktionen einer Anwendung zu testen, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="00fc6-105">This tool can be used to test an application's use of complex VSS features such as the following:</span></span>

-   <span data-ttu-id="00fc6-106">Inkrementelle Sicherung</span><span class="sxs-lookup"><span data-stu-id="00fc6-106">Incremental and differential backup</span></span>
-   <span data-ttu-id="00fc6-107">Komplexe Wiederherstellungsoptionen wie autorisierende Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="00fc6-107">Complex restore options, such as authoritative restore</span></span>
-   <span data-ttu-id="00fc6-108">Roll Forward-Optionen</span><span class="sxs-lookup"><span data-stu-id="00fc6-108">Rollforward options</span></span>

> [!Note]  
> <span data-ttu-id="00fc6-109">BETest ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="00fc6-109">BETest is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="00fc6-110">Das VSS 7,2 SDK enthält eine Version von "BETest", die nur unter Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00fc6-110">The VSS 7.2 SDK includes a version of BETest that runs only on Windows Server 2003.</span></span> <span data-ttu-id="00fc6-111">In diesem Thema wird die Windows SDK Version von BETest und nicht die Windows Server 2003-Version beschrieben, die im VSS 7,2 SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="00fc6-111">This topic describes the Windows SDK version of BETest, not the Windows Server 2003 version included in the VSS 7.2 SDK.</span></span> <span data-ttu-id="00fc6-112">Weitere Informationen zum Herunterladen der Windows SDK und des VSS 7,2 SDK finden Sie unter [Volumeschattenkopie-Dienst](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="00fc6-112">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="00fc6-113">In der Windows SDK-Installation befindet sich das Tool "BETest" unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).</span><span class="sxs-lookup"><span data-stu-id="00fc6-113">In the Windows SDK installation, the BETest tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="running-the-betest-tool"></a><span data-ttu-id="00fc6-114">Ausführen des Tools "BETest"</span><span class="sxs-lookup"><span data-stu-id="00fc6-114">Running the BETest Tool</span></span>

<span data-ttu-id="00fc6-115">Verwenden Sie die folgende Syntax, um das Tool "BETest" über die Befehlszeile auszuführen:</span><span class="sxs-lookup"><span data-stu-id="00fc6-115">To run the BETest tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="00fc6-116">*Befehlszeilenoptionen* für **BETest**</span><span class="sxs-lookup"><span data-stu-id="00fc6-116">**BETest** *command-line-options*</span></span>

<span data-ttu-id="00fc6-117">Im folgenden Verwendungs Beispiel wird gezeigt, wie das Tool "BETest" mit dem [VSS-testwriter-Tool](vss-test-writer-tool.md)verwendet wird, das eine VSS Writer ist.</span><span class="sxs-lookup"><span data-stu-id="00fc6-117">The following usage example shows how to use the BETest tool together with the [VSS Test Writer tool](vss-test-writer-tool.md), which is a VSS writer.</span></span>

<span data-ttu-id="00fc6-118">**Verwendungs Beispiel für das BETest-Tool**</span><span class="sxs-lookup"><span data-stu-id="00fc6-118">**BETest Tool Usage Example**</span></span>

1.  <span data-ttu-id="00fc6-119">Erstellen Sie ein Test Verzeichnis mit dem Namen C: \\ BETest.</span><span class="sxs-lookup"><span data-stu-id="00fc6-119">Create a test directory named C:\\BETest.</span></span> <span data-ttu-id="00fc6-120">Kopieren Sie die folgenden Dateien in dieses Verzeichnis:</span><span class="sxs-lookup"><span data-stu-id="00fc6-120">Copy the following files into this directory:</span></span>
    -   <span data-ttu-id="00fc6-121">betest.exe</span><span class="sxs-lookup"><span data-stu-id="00fc6-121">betest.exe</span></span>
    -   <span data-ttu-id="00fc6-122">vswriter.exe</span><span class="sxs-lookup"><span data-stu-id="00fc6-122">vswriter.exe</span></span>
    -   [<span data-ttu-id="00fc6-123">BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="00fc6-123">BetestSample.xml</span></span>](#sample-xml-configuration-file-betestsamplexml)
    -   [<span data-ttu-id="00fc6-124">VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="00fc6-124">VswriterSample.xml</span></span>](#sample-xml-configuration-file-vswritersamplexml)
2.  <span data-ttu-id="00fc6-125">Erstellen Sie ein Verzeichnis mit dem Namen C: \\ TestPath.</span><span class="sxs-lookup"><span data-stu-id="00fc6-125">Create a directory named C:\\TestPath.</span></span> <span data-ttu-id="00fc6-126">Fügen Sie einige Test Datendateien in dieses Verzeichnis ein.</span><span class="sxs-lookup"><span data-stu-id="00fc6-126">Put some test data files in this directory.</span></span>
3.  <span data-ttu-id="00fc6-127">Erstellen Sie ein Verzeichnis mit dem Namen "C: \\ backupdestination".</span><span class="sxs-lookup"><span data-stu-id="00fc6-127">Create a directory named C:\\BackupDestination.</span></span> <span data-ttu-id="00fc6-128">Lassen Sie dieses Verzeichnis leer.</span><span class="sxs-lookup"><span data-stu-id="00fc6-128">Leave this directory empty.</span></span>
4.  <span data-ttu-id="00fc6-129">Öffnen Sie zwei Befehlsfenster mit erhöhten Rechten, und legen Sie für das Arbeitsverzeichnis jeweils C: \\ BETest fest.</span><span class="sxs-lookup"><span data-stu-id="00fc6-129">Open two elevated command windows and set the working directory in each to C:\\BETest.</span></span>
5.  <span data-ttu-id="00fc6-130">Starten Sie im ersten Befehlsfenster das [VSS-testwriter-Tool](vss-test-writer-tool.md) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="00fc6-130">In the first command window, start the [VSS Test Writer tool](vss-test-writer-tool.md) as follows:</span></span>

    <span data-ttu-id="00fc6-131">**vswriter.exe VswriterSample.xml**</span><span class="sxs-lookup"><span data-stu-id="00fc6-131">**vswriter.exe VswriterSample.xml**</span></span>

    <span data-ttu-id="00fc6-132">Die vswriterSample.xml Datei konfiguriert das VSS-testwriter-Tool (vswriter) so, dass der Inhalt des Verzeichnisses "c: \\ TestPath" als Vorbereitung für einen Sicherungs Vorgang gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="00fc6-132">The vswriterSample.xml file configures the VSS Test Writer tool (vswriter) to report the contents of the c:\\TestPath directory in preparation for a backup operation.</span></span> <span data-ttu-id="00fc6-133">Beachten Sie, dass das VSS-testwriter-Tool erst dann eine Ausgabe erzeugt, wenn es eine Aktivität von einer Anforderer wie z. b. betest</span><span class="sxs-lookup"><span data-stu-id="00fc6-133">Note that the VSS Test Writer tool will not produce output until it detects activity from a requester such as BETest.</span></span> <span data-ttu-id="00fc6-134">Um das VSS-testwriter-Tool anzuhalten, drücken Sie STRG + C.</span><span class="sxs-lookup"><span data-stu-id="00fc6-134">To stop the VSS Test Writer tool, press CTRL+C.</span></span>

6.  <span data-ttu-id="00fc6-135">Verwenden Sie im zweiten Befehlsfenster das Tool "BETest", um einen Sicherungs Vorgang wie folgt auszuführen:</span><span class="sxs-lookup"><span data-stu-id="00fc6-135">In the second command window, use the BETest tool to perform a backup operation as follows:</span></span>

    <span data-ttu-id="00fc6-136">**betest.exe/B/S backup.xml/D C: \\ backupdestination/X BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="00fc6-136">**betest.exe /B /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

    <span data-ttu-id="00fc6-137">Mit "BETest" werden die Dateien aus dem Verzeichnis "c: \\ TestPath" in das Verzeichnis "c: \\ backupdestination" gesichert.</span><span class="sxs-lookup"><span data-stu-id="00fc6-137">BETest will back up the files from the C:\\TestPath directory to the C:\\BackupDestination directory.</span></span> <span data-ttu-id="00fc6-138">Das Sicherungs Komponenten Dokument wird in C: \\ BETest- \\backup.xml gespeichert.</span><span class="sxs-lookup"><span data-stu-id="00fc6-138">It will save the backup component document to C:\\BETest\\backup.xml.</span></span>

7.  <span data-ttu-id="00fc6-139">Wenn der Sicherungs Vorgang erfolgreich ist, löschen Sie den Inhalt des Verzeichnisses "C: \\ TestPath", und verwenden Sie das Tool "BETest", um einen Wiederherstellungs Vorgang wie folgt auszuführen:</span><span class="sxs-lookup"><span data-stu-id="00fc6-139">If the backup operation is successful, delete the contents of the C:\\TestPath directory, and use the BETest tool to perform a restore operation as follows:</span></span>

    <span data-ttu-id="00fc6-140">**betest.exe/R/S backup.xml/D C: \\ backupdestination/X BetestSample.xml**</span><span class="sxs-lookup"><span data-stu-id="00fc6-140">**betest.exe /R /S backup.xml /D C:\\BackupDestination /X BetestSample.xml**</span></span>

## <a name="betest-tool-command-line-options"></a><span data-ttu-id="00fc6-141">Command-Line Optionen für das betesttool</span><span class="sxs-lookup"><span data-stu-id="00fc6-141">BETest Tool Command-Line Options</span></span>

<span data-ttu-id="00fc6-142">Das Tool "BETest" verwendet die folgenden Befehlszeilenoptionen zur Identifizierung der auszuführenden Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="00fc6-142">The BETest tool uses the following command-line options to identify the work to perform.</span></span>

<dl> <dt>

<span data-ttu-id="00fc6-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span><span class="sxs-lookup"><span data-stu-id="00fc6-143"><span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-144">Führt einen autorisierenden Wiederherstellungs Vorgang für Active Directory oder Active Directory Anwendungsmodus aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-144">Performs an authoritative restore operation for Active Directory or Active Directory Application Mode.</span></span>

<span data-ttu-id="00fc6-145">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-145">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-146"><span id="_B"></span><span id="_b"></span>**/B**</span><span class="sxs-lookup"><span data-stu-id="00fc6-146"><span id="_B"></span><span id="_b"></span>**/B**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-147">Führt einen Sicherungs Vorgang aus, führt jedoch keine Wiederherstellung aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-147">Performs a backup operation but does not perform a restore.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span><span class="sxs-lookup"><span data-stu-id="00fc6-148"><span id="_BC"></span><span id="_bc"></span>**/BC**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-149">Führt nur den Vorgang zum Abschluss der Sicherung aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-149">Performs only the backup complete operation.</span></span>

<span data-ttu-id="00fc6-150">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-150">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="00fc6-151"><span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span>**/C** *Filename*</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="00fc6-152">Diese Befehlszeilenoption wird nur aus Gründen der Abwärtskompatibilität bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-152">This command-line option is provided only for backward compatibility.</span></span> <span data-ttu-id="00fc6-153">Stattdessen sollte die Befehlszeilenoption **/X** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00fc6-153">The **/X** command-line option should be used instead.</span></span>

 

<span data-ttu-id="00fc6-154">Wählt die zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der durch *filename* angegebenen Konfigurationsdatei aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-154">Selects the components to be backed up or restored based on the contents of the configuration file specified by *Filename*.</span></span> <span data-ttu-id="00fc6-155">Diese Datei darf nur ANSI-Zeichen im Bereich zwischen 0 und 127 enthalten und darf nicht größer als 1 MB sein.</span><span class="sxs-lookup"><span data-stu-id="00fc6-155">This file must contain only ANSI characters in the range from 0 through 127, and it must be no larger than 1 MB.</span></span> <span data-ttu-id="00fc6-156">Jede Zeile in der Datei muss das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="00fc6-156">Each line in the file must use the following format:</span></span>

<span data-ttu-id="00fc6-157">" *Write ID* ": " *componentname*;"</span><span class="sxs-lookup"><span data-stu-id="00fc6-157">*WriterId* : *ComponentName*;</span></span>

<span data-ttu-id="00fc6-158">Dabei ist " *Write ID* " die Writer-ID und " *componentname* " der Name einer der Writer-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="00fc6-158">Where *WriterId* is the writer ID, and *ComponentName* is the name of one of the writer's components.</span></span> <span data-ttu-id="00fc6-159">Die Writer-ID und die Komponentennamen müssen in Anführungszeichen stehen, und es muss Leerzeichen vor und nach dem Doppelpunkt (:).</span><span class="sxs-lookup"><span data-stu-id="00fc6-159">The writer ID and component names must be in quotation marks, and there must be spaces before and after the colon (:).</span></span> <span data-ttu-id="00fc6-160">Wenn mindestens zwei Komponenten angegeben sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="00fc6-160">If two or more components are specified, they must be separated by commas.</span></span> <span data-ttu-id="00fc6-161">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="00fc6-161">For example:</span></span>

<span data-ttu-id="00fc6-162">"5affb034-969f -4919-8875-88f 830d0ef89": "TestFiles1", "TestFiles2", "TestFiles3";</span><span class="sxs-lookup"><span data-stu-id="00fc6-162">"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** - *Pfad*</span><span class="sxs-lookup"><span data-stu-id="00fc6-163"><span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *Path*</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-164">Speichern Sie die gesicherten Dateien, oder stellen Sie Sie aus dem durch *path* angegebenen Sicherungs Verzeichnis wieder her.</span><span class="sxs-lookup"><span data-stu-id="00fc6-164">Save the backed-up files to or restore them from the backup directory specified by *Path*.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span><span class="sxs-lookup"><span data-stu-id="00fc6-165"><span id="_NBC"></span><span id="_nbc"></span>**/NBC**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-166">Lässt den Vorgang zum Abschluss der Sicherung aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-166">Omits the backup complete operation.</span></span>

<span data-ttu-id="00fc6-167">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-167">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-168"><span id="_O"></span><span id="_o"></span>**/O**</span><span class="sxs-lookup"><span data-stu-id="00fc6-168"><span id="_O"></span><span id="_o"></span>**/O**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-169">Gibt an, dass die Sicherung einen Start fähigen Systemstatus enthält.</span><span class="sxs-lookup"><span data-stu-id="00fc6-169">Specifies that the backup includes a bootable system state.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-170"><span id="_P"></span><span id="_p"></span>**/P**</span><span class="sxs-lookup"><span data-stu-id="00fc6-170"><span id="_P"></span><span id="_p"></span>**/P**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-171">Erstellt eine persistente Schatten Kopie.</span><span class="sxs-lookup"><span data-stu-id="00fc6-171">Creates a persistent shadow copy.</span></span>

<span data-ttu-id="00fc6-172">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-172">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="00fc6-173"><span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span>**/Pre** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-174">Wenn der in der Befehlszeilenoption **/T** angegebene Sicherungstyp inkrementell oder Differenziell ist, legen Sie das Sicherungs Dokument auf die Datei fest, die für eine vorherige vollständige oder inkrementelle Sicherung von *filename*</span><span class="sxs-lookup"><span data-stu-id="00fc6-174">If the backup type specified in the **/T** command-line option is INCREMENTAL or DIFFERENTIAL, set the backup document to the file specified by *Filename* for previous full or incremental backup.</span></span>

<span data-ttu-id="00fc6-175">**Windows Server 2003 und Windows XP:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-175">**Windows Server 2003 and Windows XP:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-176"><span id="_R"></span><span id="_r"></span>**/R**</span><span class="sxs-lookup"><span data-stu-id="00fc6-176"><span id="_R"></span><span id="_r"></span>**/R**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-177">Führt eine Wiederherstellung durch, führt jedoch keine Sicherung aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-177">Performs restore but does not perform backup.</span></span> <span data-ttu-id="00fc6-178">Muss in Verbindung mit der Befehlszeilenoption **/S** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00fc6-178">Must be used together with the **/S** command-line option.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span><span class="sxs-lookup"><span data-stu-id="00fc6-179"><span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-180">Erstellt eine Schatten Kopie, die für das Anwendungs Rollback verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00fc6-180">Creates a shadow copy that can be used for application rollback.</span></span>

<span data-ttu-id="00fc6-181">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-181">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="00fc6-182"><span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-183">Bei der Sicherung speichert das Sicherungs Dokument in der durch *filename* angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="00fc6-183">In case of backup, saves the backup document to the file specified by *Filename*.</span></span> <span data-ttu-id="00fc6-184">Bei nur Restore wird das Sicherungs Dokument aus dieser Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="00fc6-184">In case of restore only, loads the backup document from this file.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span><span class="sxs-lookup"><span data-stu-id="00fc6-185"><span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-186">Erstellt eine Volumeschattenkopie, führt aber keine Sicherung oder Wiederherstellung aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-186">Creates a volume shadow copy but does not perform backup or restore.</span></span>

<span data-ttu-id="00fc6-187">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-187">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span><span class="sxs-lookup"><span data-stu-id="00fc6-188"><span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-189">Beendet Tests, wenn der erste Writer-Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-189">Stops BETest when the first writer error is encountered.</span></span>

<span data-ttu-id="00fc6-190">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-190">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *backuptype*</span><span class="sxs-lookup"><span data-stu-id="00fc6-191"><span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-192">Gibt den Sicherungstyp an.</span><span class="sxs-lookup"><span data-stu-id="00fc6-192">Specifies the backup type.</span></span> <span data-ttu-id="00fc6-193">*Backuptype* kann vollständig, protokolliert, kopiert, inkrementell oder Differenziell sein.</span><span class="sxs-lookup"><span data-stu-id="00fc6-193">*BackupType* can be FULL, LOG, COPY, INCREMENTAL, or DIFFERENTIAL.</span></span> <span data-ttu-id="00fc6-194">Weitere Informationen zu Sicherungs Typen finden Sie unter [**VSS \_ - \_ Sicherungstyp**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span><span class="sxs-lookup"><span data-stu-id="00fc6-194">For more information about backup types, see [**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-195"><span id="_V"></span><span id="_v"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="00fc6-195"><span id="_V"></span><span id="_v"></span>**/V**</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-196">Generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00fc6-196">Generates verbose output that can be used for troubleshooting.</span></span>

<span data-ttu-id="00fc6-197">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-197">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="00fc6-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="00fc6-198"><span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *Filename*</span></span>
</dt> <dd>

<span data-ttu-id="00fc6-199">Wählt die zu sichernden oder wiederherzustellenden Komponenten basierend auf dem Inhalt der durch *filename* angegebenen XML-Konfigurationsdatei aus.</span><span class="sxs-lookup"><span data-stu-id="00fc6-199">Selects the components to be backed up or restored based on the contents of the XML configuration file specified by *Filename*.</span></span> <span data-ttu-id="00fc6-200">Diese Datei darf nur ANSI-Zeichen im Bereich von 0 bis 127 enthalten.</span><span class="sxs-lookup"><span data-stu-id="00fc6-200">This file must contain only ANSI characters in the range from 0 through 127.</span></span> <span data-ttu-id="00fc6-201">Das Format der XML-Datei wird durch das Schema in der BETest.xml-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="00fc6-201">The format of the XML file is defined by the schema in the BETest.xml file.</span></span> <span data-ttu-id="00fc6-202">Eine Beispielkonfigurationsdatei finden Sie unter BetestSample.xml.</span><span class="sxs-lookup"><span data-stu-id="00fc6-202">For a sample configuration file, see BetestSample.xml.</span></span> <span data-ttu-id="00fc6-203">Beide Dateien befinden sich im vshocker-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="00fc6-203">Both of these files are in the vsstools directory.</span></span>

> [!Note]  
> <span data-ttu-id="00fc6-204">Sie können die BETest.xml Datei in Internet Explorer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="00fc6-204">You can view the BETest.xml file in Internet Explorer.</span></span> <span data-ttu-id="00fc6-205">Bevor Sie diese Datei öffnen, stellen Sie sicher, dass sich die Datei XDR-Schema. xsl im gleichen Verzeichnis wie BETest.xml befindet.</span><span class="sxs-lookup"><span data-stu-id="00fc6-205">Before you open this file, make sure that the xdr-schema.xsl file is in the same directory as BETest.xml.</span></span> <span data-ttu-id="00fc6-206">Die Datei XDR-Schema. xsl enthält Renderinganweisungen, mit denen die BETest.xml-Datei besser lesbar wird.</span><span class="sxs-lookup"><span data-stu-id="00fc6-206">The xdr-schema.xsl file contains rendering instructions that make the BETest.xml file more readable.</span></span>

 

<span data-ttu-id="00fc6-207">**Windows Server 2003:** Diese Befehlszeilenoption wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-207">**Windows Server 2003:** This command-line option is not supported.</span></span>

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a><span data-ttu-id="00fc6-208">Beispiel-XML-Konfigurationsdatei: BetestSample.xml</span><span class="sxs-lookup"><span data-stu-id="00fc6-208">Sample XML Configuration File: BetestSample.xml</span></span>

<span data-ttu-id="00fc6-209">Die folgende Beispielkonfigurationsdatei (BetestSample.xml) finden Sie im vshocker-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="00fc6-209">The following sample configuration file, BetestSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

<span data-ttu-id="00fc6-210">Dieses Beispiel einer einfachen Konfigurationsdatei wählt eine Komponente aus, die gesichert oder wieder hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00fc6-210">This example of a simple configuration file selects one component to be backed up or restored.</span></span>

## <a name="sample-xml-configuration-file-vswritersamplexml"></a><span data-ttu-id="00fc6-211">Beispiel-XML-Konfigurationsdatei: VswriterSample.xml</span><span class="sxs-lookup"><span data-stu-id="00fc6-211">Sample XML Configuration File: VswriterSample.xml</span></span>

<span data-ttu-id="00fc6-212">Die folgende Beispielkonfigurationsdatei (VswriterSample.xml) finden Sie im vshocker-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="00fc6-212">The following sample configuration file, VswriterSample.xml, can be found in the Vsstools directory.</span></span>

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

<span data-ttu-id="00fc6-213">Das Stamm Element in dieser Konfigurationsdatei hat den Namen testwriter.</span><span class="sxs-lookup"><span data-stu-id="00fc6-213">The root element in this configuration file is named TestWriter.</span></span> <span data-ttu-id="00fc6-214">Alle anderen Elemente werden unter dem testwriter-Element angeordnet.</span><span class="sxs-lookup"><span data-stu-id="00fc6-214">All other elements are arranged under the TestWriter element.</span></span>

<span data-ttu-id="00fc6-215">Das erste Attribut, das testwriter zugeordnet ist, ist das Usage-Attribut.</span><span class="sxs-lookup"><span data-stu-id="00fc6-215">The first attribute associated with TestWriter is the usage attribute.</span></span> <span data-ttu-id="00fc6-216">Dieses Attribut gibt den Verwendungstyp an, der über die [**ivssexaminewrite Metadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) -Methode gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="00fc6-216">This attribute specifies the usage type reported through the [**IVssExamineWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) method.</span></span> <span data-ttu-id="00fc6-217">Einer der möglichen Werte für dieses Attribut sind Benutzer \_ Daten.</span><span class="sxs-lookup"><span data-stu-id="00fc6-217">One of the possible values for this attribute is USER\_DATA.</span></span>

<span data-ttu-id="00fc6-218">Das zweite Attribut ist das DeleteFiles-Attribut.</span><span class="sxs-lookup"><span data-stu-id="00fc6-218">The second attribute is the deleteFiles attribute.</span></span> <span data-ttu-id="00fc6-219">Dieses Attribut wird unter [Konfigurieren von Writer-Attributen](vss-test-writer-tool.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="00fc6-219">This attribute is described in [Configuring Writer Attributes](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="00fc6-220">Das erste untergeordnete Element des Root-Elements ist ein restoremethod-Element.</span><span class="sxs-lookup"><span data-stu-id="00fc6-220">The first child element of the root element is a RestoreMethod element.</span></span> <span data-ttu-id="00fc6-221">Dieses Element gibt Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="00fc6-221">This element specifies the following:</span></span>

-   <span data-ttu-id="00fc6-222">Die Restore-Methode (in diesem Fall Restore \_ , \_ Wenn \_ ersetzt werden kann \_ )</span><span class="sxs-lookup"><span data-stu-id="00fc6-222">The restore method (in this case, RESTORE\_IF\_CAN\_BE\_REPLACED)</span></span>
-   <span data-ttu-id="00fc6-223">Gibt an, ob der Writer Wiederherstellungs Ereignisse erfordert (in diesem Fall immer).</span><span class="sxs-lookup"><span data-stu-id="00fc6-223">Whether the writer requires restore events (in this case, always)</span></span>
-   <span data-ttu-id="00fc6-224">Gibt an, ob ein Neustart erforderlich ist, nachdem der Writer wieder hergestellt wurde (in diesem Fall Nein).</span><span class="sxs-lookup"><span data-stu-id="00fc6-224">Whether a reboot is required after the writer is restored (in this case, no)</span></span>

<span data-ttu-id="00fc6-225">Dieses Element kann optional eine Zuordnung alternativer Orte angeben.</span><span class="sxs-lookup"><span data-stu-id="00fc6-225">This element can optionally specify an alternate-location mapping.</span></span> <span data-ttu-id="00fc6-226">(In diesem Fall wird kein alternativer Speicherort angegeben.) Weitere Informationen finden Sie unter [angeben](vss-test-writer-tool.md)von Zuordnungen für Alternative Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="00fc6-226">(In this case, no alternate location is specified.) For more information, see [Specifying Alternate Location Mappings](vss-test-writer-tool.md).</span></span>

<span data-ttu-id="00fc6-227">Das zweite untergeordnete Element ist ein Komponenten Element.</span><span class="sxs-lookup"><span data-stu-id="00fc6-227">The second child element is a Component element.</span></span> <span data-ttu-id="00fc6-228">Dieses Element bewirkt, dass der Writer seinen Metadaten eine Komponente hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="00fc6-228">This element causes the writer to add a component to its metadata.</span></span> <span data-ttu-id="00fc6-229">Ein Component-Element enthält Attribute, mit denen die Komponente und die untergeordneten Elemente beschrieben werden, um den Inhalt der Komponente zu beschreiben, wie z. b. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="00fc6-229">A Component element contains attributes to describe the component and child elements to describe the content of the component, such as the following:</span></span>

-   <span data-ttu-id="00fc6-230">componentType, um anzugeben, ob es sich um eine Datei Gruppe oder eine Datenbank handelt (in diesem Fall eine Datei Gruppe)</span><span class="sxs-lookup"><span data-stu-id="00fc6-230">componentType to indicate whether this is a filegroup or a database (in this case, a filegroup)</span></span>
-   <span data-ttu-id="00fc6-231">LogicalPath für den logischen Pfad der Komponente (in diesem Fall ist keine angegeben)</span><span class="sxs-lookup"><span data-stu-id="00fc6-231">logicalPath for the component logical path (in this case, none is specified)</span></span>
-   <span data-ttu-id="00fc6-232">componentname für den Namen der Komponente (in diesem Fall "testfiles")</span><span class="sxs-lookup"><span data-stu-id="00fc6-232">componentName for the name of the component (in this case, "TestFiles")</span></span>
-   <span data-ttu-id="00fc6-233">auswählbar zum Angeben des Status für die auswählbare Sicherung</span><span class="sxs-lookup"><span data-stu-id="00fc6-233">selectable to indicate selectable-for-backup status</span></span>

<span data-ttu-id="00fc6-234">Das Component-Element weist auch ein untergeordnetes Element mit dem Namen "componentfile" auf, um dieser Komponente eine Datei Spezifikation hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="00fc6-234">The Component element also has a child element named ComponentFile to add a file specification to this component.</span></span> <span data-ttu-id="00fc6-235">(Ein Komponenten Element kann eine beliebige Anzahl von componentfile-Elementen aufweisen, die für jede Komponente angegeben werden können.) Dieses componentfile-Element weist die folgenden Attribute auf:</span><span class="sxs-lookup"><span data-stu-id="00fc6-235">(A Component element can have an arbitrary number of ComponentFile elements that can be specified for each component.) This ComponentFile element has the following attributes:</span></span>

-   <span data-ttu-id="00fc6-236">Path = "c: \\ TestPath"</span><span class="sxs-lookup"><span data-stu-id="00fc6-236">path="c:\\TestPath"</span></span>
-   <span data-ttu-id="00fc6-237">file spec = " \* "</span><span class="sxs-lookup"><span data-stu-id="00fc6-237">filespec="\*"</span></span>
-   <span data-ttu-id="00fc6-238">rekursiv = "Nein"</span><span class="sxs-lookup"><span data-stu-id="00fc6-238">recursive="no"</span></span>

 

 



