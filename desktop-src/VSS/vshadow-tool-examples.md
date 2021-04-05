---
description: 'Weitere Informationen: Beispiele für den vshadow-Tool'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Beispiele für den vshadow-Tool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751569"
---
# <a name="vshadow-tool-examples"></a><span data-ttu-id="72319-103">Beispiele für den vshadow-Tool</span><span class="sxs-lookup"><span data-stu-id="72319-103">VShadow Tool Examples</span></span>

<span data-ttu-id="72319-104">In den folgenden Beispielen wird veranschaulicht, wie das vshadow-Tool verwendet wird, um die gängigsten Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="72319-104">The following examples show how to use the VShadow tool to perform the most common tasks:</span></span>

-   [<span data-ttu-id="72319-105">Zugreifen auf schattenkopieeigenschaften aus einem cmd-Skript</span><span class="sxs-lookup"><span data-stu-id="72319-105">Accessing Shadow Copy Properties from a CMD Script</span></span>](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [<span data-ttu-id="72319-106">Zugreifen auf nicht persistente Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="72319-106">Accessing Nonpersistent Shadow Copies</span></span>](#accessing-nonpersistent-shadow-copies)
-   [<span data-ttu-id="72319-107">Kopieren einer Datei aus einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="72319-107">Copying a File from a Shadow Copy</span></span>](#copying-a-file-from-a-shadow-copy)
-   [<span data-ttu-id="72319-108">Auflisten aller Dateien auf einem schattenkopiespeichergerät</span><span class="sxs-lookup"><span data-stu-id="72319-108">Enumerating All Files on a Shadow Copy Device</span></span>](#enumerating-all-files-on-a-shadow-copy-device)
-   [<span data-ttu-id="72319-109">Importieren einer transportable-Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="72319-109">Importing a Transportable Shadow Copy</span></span>](#importing-a-transportable-shadow-copy)
-   [<span data-ttu-id="72319-110">Einschließen von Writern oder Komponenten</span><span class="sxs-lookup"><span data-stu-id="72319-110">Including Writers or Components</span></span>](#including-writers-or-components)
-   [<span data-ttu-id="72319-111">Ausschließen von Writern oder Komponenten</span><span class="sxs-lookup"><span data-stu-id="72319-111">Excluding Writers or Components</span></span>](#excluding-writers-or-components)
-   [<span data-ttu-id="72319-112">Unterbrechen von schattenkopiesätzen mithilfe der breaksnapshotsetex-Methode</span><span class="sxs-lookup"><span data-stu-id="72319-112">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

<span data-ttu-id="72319-113">Eine umfassende Liste der Befehlszeilenoptionen und deren Verwendung finden Sie unter [vshadow-Tool und-Beispiel](vshadow-tool-and-sample.md).</span><span class="sxs-lookup"><span data-stu-id="72319-113">For a complete list of command-line options and their use, see [VShadow Tool and Sample](vshadow-tool-and-sample.md).</span></span>

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a><span data-ttu-id="72319-114">Zugreifen auf schattenkopieeigenschaften aus einem cmd-Skript</span><span class="sxs-lookup"><span data-stu-id="72319-114">Accessing Shadow Copy Properties from a CMD Script</span></span>

<span data-ttu-id="72319-115">Wenn Sie das optionale Flag **-Script** verwenden, wenn Sie Schatten Kopien erstellen, erstellt vshadow eine cmd-Skriptdatei, die Umgebungsvariablen enthält, die sich auf die neu erstellten Schatten Kopien beziehen, wie z. b. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="72319-115">If you use the **-script** optional flag when you create shadow copies, VShadow creates a CMD script file containing environment variables related to the newly created shadow copies, such as the following:</span></span>

-   <span data-ttu-id="72319-116">Die ID des schattenkopiesatzes, der in der% vshadow \_ Set \_ ID%-Umgebungsvariablen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="72319-116">The shadow copy set ID, which is stored in the %VSHADOW\_SET\_ID% environment variable</span></span>
-   <span data-ttu-id="72319-117">Die schattenkopienids, die in Variablen der Form% vshadow \_ ID \_ *nnn*% gespeichert sind, wobei *nnn* den Index des Quell Volumens in der vshadow-Befehlszeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="72319-117">The shadow copy IDs, which are stored in variables of the form %VSHADOW\_ID\_*NNN*%, where *NNN* represents the index of the source volume in the VShadow command line</span></span>
-   <span data-ttu-id="72319-118">Die Namen der Schatten Kopie-Geräte, die in Variablen der Form% vshadow- \_ Gerät \_ *nnn*% gespeichert sind, wobei *nnn* der Index des Quell Volumens in der vshadow-Befehlszeile ist.</span><span class="sxs-lookup"><span data-stu-id="72319-118">The shadow copy device names, which are stored in variables of the form %VSHADOW\_DEVICE\_*NNN*%, where *NNN* is the index of the source volume in the VShadow command line</span></span>

<span data-ttu-id="72319-119">Mit der generierten cmd-Datei können Sie eingeschränkte Verwaltungsvorgänge für die Schatten Kopien durchführen.</span><span class="sxs-lookup"><span data-stu-id="72319-119">You can use the generated CMD file to perform limited management operations on the shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="72319-120">Das [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer-Ereignis wird gesendet, nachdem das **-exec-** Skript ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="72319-120">The [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) writer event is sent after the **-exec** script is executed.</span></span> <span data-ttu-id="72319-121">VSS ruft die **IVssBackupComponents:: BackupComplete** -Methode auf, um den Writern zu signalisieren, dass die Sicherung abgeschlossen ist, und die Writer können an diesem Punkt möglicherweise Protokolle abschneiden.</span><span class="sxs-lookup"><span data-stu-id="72319-121">VSS calls the **IVssBackupComponents::BackupComplete** method to signal to the writers that the backup is completed, and the writers can potentially truncate logs at this point.</span></span> <span data-ttu-id="72319-122">Daher ist es wichtig, zu überprüfen, ob der Schatten/die Sicherung tatsächlich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="72319-122">Therefore, it is important to verify that the shadow/backup actually completed.</span></span> <span data-ttu-id="72319-123">Wenn bei der Sicherung ein Fehler aufgetreten ist, können Sie den Erstellungs Prozess Abbrechen, indem Sie einen Exitcode ungleich NULL im ausgeführten Skript/Befehl zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="72319-123">If the backup failed, you can cancel the creation process by returning a nonzero exit code in the executed script/command.</span></span> <span data-ttu-id="72319-124">(Weitere Informationen finden Sie in der Dokumentation für den Exit-Befehl in der [Windows-Befehlszeilen Referenz](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Wenn der benutzerdefinierte Befehl mit einem Exitcode ungleich 0 (null) zurückgegeben wird, wird die Erstellung der Schatten Kopie abgebrochen, und **IVssBackupComponents:: BackupComplete** wird nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72319-124">(See the documentation for the exit command in the [Windows Command Line Reference](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) If the custom command returns with a nonzero exit code, then the shadow copy creation is canceled and **IVssBackupComponents::BackupComplete** will not be called.</span></span>

 

<span data-ttu-id="72319-125">Im folgenden Beispiel wird gezeigt, wie Sie eine persistente Schatten Kopie in der Befehlszeile erstellen und das cmd-Skript verwenden, um Sie verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="72319-125">The following example shows how to create a persistent shadow copy from the command line and use the CMD script to expose it.</span></span>

1.  <span data-ttu-id="72319-126">**vshadow-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="72319-126">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
2.  <span data-ttu-id="72319-127">**SETVAR1. cmd aufzurufen**</span><span class="sxs-lookup"><span data-stu-id="72319-127">**call SETVAR1.cmd**</span></span>
3.  <span data-ttu-id="72319-128">**C: \\>vshadow-El =% vshadow- \_ ID \_ 1%, c: \\ directory1**</span><span class="sxs-lookup"><span data-stu-id="72319-128">**C:\\>vshadow -el=%VSHADOW\_ID\_1%,c:\\directory1**</span></span>

## <a name="accessing-nonpersistent-shadow-copies"></a><span data-ttu-id="72319-129">Zugreifen auf nicht persistente Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="72319-129">Accessing Nonpersistent Shadow Copies</span></span>

<span data-ttu-id="72319-130">Nicht persistente Schatten Kopien werden automatisch gelöscht, wenn das Programm, das Sie erstellt, (in diesem Fall vshadow) beendet wird.</span><span class="sxs-lookup"><span data-stu-id="72319-130">Nonpersistent shadow copies are automatically deleted when the program that creates them (in this case, VShadow) exits.</span></span> <span data-ttu-id="72319-131">Für den Zugriff auf den Inhalt dieser Schatten Kopien ermöglicht vshadow das Ausführen eines Skripts, nachdem die Schatten Kopien erstellt wurden, aber bevor das vshadow-Programm beendet wird.</span><span class="sxs-lookup"><span data-stu-id="72319-131">To access the contents of these shadow copies, VShadow allows you to execute a script after the shadow copies are created but before the VShadow program exits.</span></span>

<span data-ttu-id="72319-132">Im folgenden Beispiel wird gezeigt, wie die Befehlszeilenoption-Exec zum Ausführen eines Skripts mit dem Namen "Enum. cmd" verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="72319-132">The following example shows how to use the -exec command-line option to run a script called "enum.cmd":</span></span>

<span data-ttu-id="72319-133">**vshadow-NW-Exec = Aufzählung. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="72319-133">**vshadow -nw -exec=enum.cmd c:**</span></span>

<span data-ttu-id="72319-134">Im ausgeführten Skript können Sie auch das generierte SETVAR-Skript in diesem benutzerdefinierten Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="72319-134">In the executed script, you can also run the generated SETVAR script in this custom command.</span></span> <span data-ttu-id="72319-135">Dadurch kann das Skript direkt auf den Inhalt der Schatten Kopien zugreifen.</span><span class="sxs-lookup"><span data-stu-id="72319-135">This allows the script to access the contents of the shadow copies directly.</span></span> <span data-ttu-id="72319-136">Beachten Sie, dass das Schatten Gerät von der \_ nnn-Umgebungsvariable des vshadow-Geräts abgerufen werden kann \_ .</span><span class="sxs-lookup"><span data-stu-id="72319-136">Remember that the shadow device can be retrieved from the VSHADOW\_DEVICE\_NNN environment variable.</span></span>

<span data-ttu-id="72319-137">Im folgenden finden Sie ein Beispielskript für "cmd":</span><span class="sxs-lookup"><span data-stu-id="72319-137">Here is an example enum.cmd script:</span></span>

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

<span data-ttu-id="72319-138">Hier ist die Befehlszeile zum Ausführen des Skripts "Enum. cmd":</span><span class="sxs-lookup"><span data-stu-id="72319-138">Here is the command line to execute the enum.cmd script:</span></span>

<span data-ttu-id="72319-139">**vshadow-NW-Exec = c: \\ Umum. CMD-Script = setvar1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="72319-139">**vshadow -nw -exec=c:\\enum.cmd -script=setvar1.cmd c:**</span></span>

## <a name="copying-a-file-from-a-shadow-copy"></a><span data-ttu-id="72319-140">Kopieren einer Datei aus einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="72319-140">Copying a File from a Shadow Copy</span></span>

<span data-ttu-id="72319-141">Im folgenden Beispiel wird gezeigt, wie eine Datei aus einer Schatten Kopie kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="72319-141">The following example shows how to copy a file from a shadow copy.</span></span>

1.  <span data-ttu-id="72319-142">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="72319-142">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="72319-143">**vshadow-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="72319-143">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="72319-144">**SETVAR1. cmd aufzurufen**</span><span class="sxs-lookup"><span data-stu-id="72319-144">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="72319-145">**Kopieren Sie% vshadow- \_ Gerät \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**</span><span class="sxs-lookup"><span data-stu-id="72319-145">**copy %VSHADOW\_DEVICE\_1%\\somefile.txt c:\\somefile\_bak.txt**</span></span>

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a><span data-ttu-id="72319-146">Auflisten aller Dateien auf einem schattenkopiespeichergerät</span><span class="sxs-lookup"><span data-stu-id="72319-146">Enumerating All Files on a Shadow Copy Device</span></span>

<span data-ttu-id="72319-147">Im folgenden Beispiel wird gezeigt, wie alle Dateien auf einem schattenkopiesgerät aus einer Batchdatei aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="72319-147">The following example shows how to enumerate all files on a shadow copy device from a batch file.</span></span>

1.  <span data-ttu-id="72319-148">**dir > c: \\somefile.txt**</span><span class="sxs-lookup"><span data-stu-id="72319-148">**dir > c:\\somefile.txt**</span></span>
2.  <span data-ttu-id="72319-149">**vshadow-p-NW-Script = SETVAR1. cmd c:**</span><span class="sxs-lookup"><span data-stu-id="72319-149">**vshadow -p -nw -script=SETVAR1.cmd c:**</span></span>
3.  <span data-ttu-id="72319-150">**SETVAR1. cmd aufzurufen**</span><span class="sxs-lookup"><span data-stu-id="72319-150">**call SETVAR1.cmd**</span></span>
4.  <span data-ttu-id="72319-151">**für/R% vshadow- \_ Gerät \_ 1% \\ %% i in ( \* ) führen Sie @echo %% i aus.**</span><span class="sxs-lookup"><span data-stu-id="72319-151">**for /R %VSHADOW\_DEVICE\_1%\\ %%i in (\*) do @echo %%i**</span></span>

## <a name="importing-a-transportable-shadow-copy"></a><span data-ttu-id="72319-152">Importieren einer transportable-Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="72319-152">Importing a Transportable Shadow Copy</span></span>

<span data-ttu-id="72319-153">Um eine austauschen-Schatten Kopie auf einem Computer zu erstellen und auf einen anderen Computer zu importieren, müssen Sie über zwei Computer verfügen, die (über eine SAN-Konfiguration) mit einem Speicher Array verbunden sind, das VSS-Hardware Schatten Kopien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="72319-153">To create a transportable shadow copy on one machine and import it to another machine, you must have two computers that are connected (through a SAN configuration) to a storage array that supports VSS hardware shadow copies.</span></span> <span data-ttu-id="72319-154">Ein VSS-Hardware Anbieter muss auf jedem Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="72319-154">A VSS hardware provider must be installed on each computer.</span></span>

<span data-ttu-id="72319-155">Im folgenden Beispiel wird gezeigt, wie die Schatten Kopie erstellt und importiert wird.</span><span class="sxs-lookup"><span data-stu-id="72319-155">The following example shows how to create and import the shadow copy.</span></span>

1.  <span data-ttu-id="72319-156">Erstellen Sie die auf Computer A (dem Produktionsserver) festgelegte Schatten Kopie, indem Sie den folgenden Befehl nach der Eingabeaufforderung eingeben:</span><span class="sxs-lookup"><span data-stu-id="72319-156">Create the shadow copy set on computer A (the production server) by typing the following command after the command prompt:</span></span>

    <span data-ttu-id="72319-157">**vshadow-p-t =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="72319-157">**vshadow -p -t=bc1.xml**</span></span>

    <span data-ttu-id="72319-158">Dadurch werden keine schattenkopiegeräte auf Computer A verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="72319-158">This will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="72319-159">Kopieren Sie das Dokument mit den Sicherungs Komponenten (bc1.xml) von Computer A auf Computer B.</span><span class="sxs-lookup"><span data-stu-id="72319-159">Copy the backup components document (bc1.xml) from computer A to computer B.</span></span>
3.  <span data-ttu-id="72319-160">Importieren Sie den Schatten Satz auf Computer B, indem Sie den folgenden Befehl eingeben:</span><span class="sxs-lookup"><span data-stu-id="72319-160">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="72319-161">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="72319-161">**vshadow -i=bc1.xml**</span></span>

<span data-ttu-id="72319-162">Optional können Sie diese Schatten Kopien als Laufwerksbuchstaben oder eingebundene Ordner verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="72319-162">Optionally, you could expose these shadow copies as drive letters or mounted folders.</span></span> <span data-ttu-id="72319-163">Außerdem könnten Sie den Schatten Satz möglicherweise unterbrechen, damit die neuen Schattenkopievolumes Lese-/Schreibzugriff erhalten.</span><span class="sxs-lookup"><span data-stu-id="72319-163">Also, you could potentially break the shadow set to make the new shadow copy volumes read-write.</span></span>

<span data-ttu-id="72319-164">Zum Automatisieren des Schattensatz-Verwaltungsprozesses können Sie die Befehlszeilenoption " **-Script** " verwenden, um das cmd-Skript zu generieren, das die schattenkopieids enthält.</span><span class="sxs-lookup"><span data-stu-id="72319-164">To automate the shadow set management process you might use the **-script** command-line option to generate the CMD script containing the shadow copy IDs.</span></span> <span data-ttu-id="72319-165">Anschließend können Sie das generierte Skript zusammen mit den Sicherungs Komponenten auf den anderen Computer kopieren.</span><span class="sxs-lookup"><span data-stu-id="72319-165">Then you can copy the generated script along with the backup components to the other computer.</span></span>

<span data-ttu-id="72319-166">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von CMD-Skripts austauschen-Schatten Kopien erstellen, verfügbar machen und unterbrechen können.</span><span class="sxs-lookup"><span data-stu-id="72319-166">The following example shows how to create, expose, and break transportable shadow copies using CMD scripts.</span></span>

1.  <span data-ttu-id="72319-167">Erstellen Sie die auf Computer A (dem Produktionsserver) festgelegte Schatten Kopie wie folgt über die Befehlszeile:</span><span class="sxs-lookup"><span data-stu-id="72319-167">Create the shadow copy set on computer A (the production server) from the command line as follows:</span></span>

    <span data-ttu-id="72319-168">**vshadow-p-t =bc1.xml-Script = SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="72319-168">**vshadow -p -t=bc1.xml -script=sc1.cmd**</span></span>

    <span data-ttu-id="72319-169">Geben Sie die Option **-Script** an, um das Skript zu generieren, das die entsprechenden Umgebungsvariablen Definitionen enthält.</span><span class="sxs-lookup"><span data-stu-id="72319-169">Specify the **-script** option to generate the script containing the proper environment variable definitions.</span></span> <span data-ttu-id="72319-170">Beachten Sie, dass dadurch keine schattenkopiegeräte auf Computer A verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="72319-170">Note that this will not expose any shadow copy devices on computer A.</span></span>

2.  <span data-ttu-id="72319-171">Kopieren Sie das Dokument mit den Sicherungs Komponenten (bc1.xml) und das generierte Skript (SC1. cmd) von Computer A auf Computer B.</span><span class="sxs-lookup"><span data-stu-id="72319-171">Copy the backup components document (bc1.xml) and the generated script (sc1.cmd) from computer A to computer B.</span></span>
3.  <span data-ttu-id="72319-172">Importieren Sie den Schatten Satz auf Computer B, indem Sie den folgenden Befehl eingeben:</span><span class="sxs-lookup"><span data-stu-id="72319-172">Import the shadow set on machine B by typing the following command:</span></span>

    <span data-ttu-id="72319-173">**vshadow-i =bc1.xml**</span><span class="sxs-lookup"><span data-stu-id="72319-173">**vshadow -i=bc1.xml**</span></span>

    <span data-ttu-id="72319-174">Hierdurch werden die erstellten Geräte auf Computer B angezeigt.</span><span class="sxs-lookup"><span data-stu-id="72319-174">This will surface the created devices on computer B.</span></span>

4.  <span data-ttu-id="72319-175">Führen Sie das generierte Skript aus, um die Umgebungsvariablen für den Schattenkopiesatz festzulegen, indem Sie den Dateinamen an der Eingabeaufforderung eingeben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="72319-175">Run the generated script to set the environment variables for the shadow copy set by typing the file name at the command prompt as in the following example:</span></span>

    <span data-ttu-id="72319-176">**SC1. cmd**</span><span class="sxs-lookup"><span data-stu-id="72319-176">**sc1.cmd**</span></span>

    <span data-ttu-id="72319-177">Dadurch werden die relevanten Umgebungsvariablen festgelegt, wie unter Zugreifen auf Schatten Kopier Eigenschaften aus einem cmd-Skript beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72319-177">This will set the relevant environment variables as described in Access Shadow Copy Properties from a CMD Script.</span></span>

5.  <span data-ttu-id="72319-178">Machen Sie die Schatten Kopien auf Computer B verfügbar, indem Sie die folgenden Befehle eingeben:</span><span class="sxs-lookup"><span data-stu-id="72319-178">Expose the shadow copies on computer B by typing the following commands:</span></span>
    1.  <span data-ttu-id="72319-179">**rmdir/s c: \\ \_ Einfügepunkt**</span><span class="sxs-lookup"><span data-stu-id="72319-179">**rmdir /s c:\\mount\_point**</span></span>
    2.  <span data-ttu-id="72319-180">**mkdir c: \\ \_ Einfügepunkt**</span><span class="sxs-lookup"><span data-stu-id="72319-180">**mkdir c:\\mount\_point**</span></span>
    3.  <span data-ttu-id="72319-181">**vshadow – El =% vshadow- \_ ID \_ 1%, c: Einfügepunkt \\ \_**</span><span class="sxs-lookup"><span data-stu-id="72319-181">**vshadow –el=%VSHADOW\_ID\_1%,c:\\mount\_point**</span></span>

    <span data-ttu-id="72319-182">Hierdurch werden die erstellten schattenkopiegeräte auf Computer B angezeigt.</span><span class="sxs-lookup"><span data-stu-id="72319-182">This will surface the created shadow copy devices on computer B.</span></span>
6.  <span data-ttu-id="72319-183">Unterbrechen Sie den Schattenkopiesatz, damit die Volumes beschreibbar sind, indem Sie den folgenden Befehl eingeben:**C: \\>vshadow – BW =% vshadow \_ Set \_ ID%**</span><span class="sxs-lookup"><span data-stu-id="72319-183">Break the shadow copy set to make the volumes writable by typing the following command:**C:\\>vshadow –bw=%VSHADOW\_SET\_ID%**</span></span>

<span data-ttu-id="72319-184">Beachten Sie, dass nicht persistente austauschen-Schatten Kopien ebenfalls importiert werden können, aber Sie werden automatisch gelöscht, wenn der **vshadow** **-i-** Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="72319-184">Note that nonpersistent transportable shadow copies can also be imported, but they are automatically deleted when the **vshadow** **-i** process exits.</span></span> <span data-ttu-id="72319-185">Wenn Sie die Schatten Kopien vor dem Löschen importieren möchten, müssen Sie die Befehlszeilenoption **-exec** verwenden, wie unter Zugriff auf nicht persistente Schatten Kopien beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72319-185">To import the shadow copies before they are deleted, you must use the **-exec** command-line option as described in Access Nonpersistent Shadow Copies.</span></span>

## <a name="including-writers-or-components"></a><span data-ttu-id="72319-186">Einschließen von Writern oder Komponenten</span><span class="sxs-lookup"><span data-stu-id="72319-186">Including Writers or Components</span></span>

<span data-ttu-id="72319-187">Standardmäßig nehmen alle Writer an der Erstellung von Schatten Kopien Teil.</span><span class="sxs-lookup"><span data-stu-id="72319-187">By default, all writers participate in shadow copy creation.</span></span> <span data-ttu-id="72319-188">Wenn Sie bestimmen möchten, welche Writer und Komponenten in einen Schattenkopiesatz eingeschlossen werden sollen, verwenden Sie die Befehlszeilenoption **-WM** oder **-wm2** , wie in [Auflisten von Writer-Status und-Metadaten](vshadow-tool-and-sample.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="72319-188">To determine which writers and components will be included in a shadow copy set, use the **-wm** or **-wm2** command-line option as described in [Listing Writer Status and Metadata](vshadow-tool-and-sample.md).</span></span>

<span data-ttu-id="72319-189">Um sicherzustellen, dass alle Komponenten eines Writers enthalten sind, verwenden Sie das optionale **-Wi-** Flag in einem der folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="72319-189">To verify that all of a writer's components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="72319-190">**vshadow** **-Wi-** *beschreibname*</span><span class="sxs-lookup"><span data-stu-id="72319-190">**vshadow** **-wi** *WriterName*</span></span>
-   <span data-ttu-id="72319-191">**vshadow** **-Wi** **"**_Writer-namens Zeichenfolge_*_"_*</span><span class="sxs-lookup"><span data-stu-id="72319-191">**vshadow** **-wi** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="72319-192">**vshadow** **-Wi** **{**_beschreiterid_*_}_*</span><span class="sxs-lookup"><span data-stu-id="72319-192">**vshadow** **-wi** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="72319-193">**vshadow** **-Wi** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="72319-193">**vshadow** **-wi** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="72319-194">Verwenden Sie das optionale **-Wi-** Flag in einem der folgenden Formate, um zu überprüfen, ob bestimmte Komponenten eingeschlossen sind:</span><span class="sxs-lookup"><span data-stu-id="72319-194">To verify that specific components are included, use the **-wi** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="72319-195">**vshadow** **-Wi-** \*Schreib Name \***: \\**_LogicalPath_\* _\\_ \* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-195">**vshadow** **-wi** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="72319-196">**vshadow** **-Wi** **"**_Writer-namens Zeichenfolge_*_": \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-196">**vshadow** **-wi** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="72319-197">**vshadow** **-Wi** **{**_beschreiterid_*_}: \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-197">**vshadow** **-wi** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="72319-198">**vshadow** **-Wi** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-198">**vshadow** **-wi** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="72319-199">In den folgenden Beispielen wird gezeigt, wie das optionale **-Flag-Wi** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72319-199">The following examples show how to use the **-wi** optional flag.</span></span>

-   <span data-ttu-id="72319-200">Angeben von " *Write Name*: \\ *LogicalPath* \\ *componentname*":</span><span class="sxs-lookup"><span data-stu-id="72319-200">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="72319-201">**vshadow-Wi = "registrierungswriter: \\ Registrierung"**</span><span class="sxs-lookup"><span data-stu-id="72319-201">**vshadow -wi="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="72319-202">Angeben von {*Write ID*}:</span><span class="sxs-lookup"><span data-stu-id="72319-202">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="72319-203">**vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="72319-203">**vshadow -wi={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="72319-204">Angeben von mehr als einem Writer oder einer Komponente:</span><span class="sxs-lookup"><span data-stu-id="72319-204">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="72319-205">**vshadow-Wi = "Registry Writer: \\ Registry"-Wi = "com+ RegDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="72319-205">**vshadow -wi="Registry Writer:\\Registry" -wi="COM+ REGDB Writer"**</span></span>

## <a name="excluding-writers-or-components"></a><span data-ttu-id="72319-206">Ausschließen von Writern oder Komponenten</span><span class="sxs-lookup"><span data-stu-id="72319-206">Excluding Writers or Components</span></span>

<span data-ttu-id="72319-207">Um alle Writer auszuschließen, verwenden Sie das optionale Flag **-NW** , wenn Sie die Schatten Kopie erstellen.</span><span class="sxs-lookup"><span data-stu-id="72319-207">To exclude all writers, use the **-nw** optional flag when creating the shadow copy.</span></span>

<span data-ttu-id="72319-208">Um alle Komponenten eines Writers auszuschließen, verwenden Sie das optionale **-WX-** Flag in einem der folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="72319-208">To exclude all of a writer's components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="72319-209">**vshadow** **-WX-** *beschreitername*</span><span class="sxs-lookup"><span data-stu-id="72319-209">**vshadow** **-wx** *WriterName*</span></span>
-   <span data-ttu-id="72319-210">**vshadow** **-WX** **"**_Writer-namens Zeichenfolge_*_"_*</span><span class="sxs-lookup"><span data-stu-id="72319-210">**vshadow** **-wx** **"**_Writer Name String_*_"_*</span></span>
-   <span data-ttu-id="72319-211">**vshadow** **-WX** **{**_beschreiterid_*_}_*</span><span class="sxs-lookup"><span data-stu-id="72319-211">**vshadow** **-wx** **{**_WriterID_*_}_*</span></span>
-   <span data-ttu-id="72319-212">**vshadow** **-WX** **{**_InstanceId_*_}_*</span><span class="sxs-lookup"><span data-stu-id="72319-212">**vshadow** **-wx** **{**_InstanceID_*_}_*</span></span>

<span data-ttu-id="72319-213">Um bestimmte Komponenten auszuschließen, verwenden Sie das optionale **-WX-** Flag in einem der folgenden Formate:</span><span class="sxs-lookup"><span data-stu-id="72319-213">To exclude specific components, use the **-wx** optional flag in any of the following formats:</span></span>

-   <span data-ttu-id="72319-214">**vshadow** **-WX-** \*Schreib Name \***: \\**_LogicalPath_\* _\\_ \* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-214">**vshadow** **-wx** *WriterName\***:\\**_LogicalPath_*_\\_\*_ComponentName_</span></span>
-   <span data-ttu-id="72319-215">**vshadow** **-WX** **"**_Writer-namens Zeichenfolge_*_": \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-215">**vshadow** **-wx** **"**_Writer Name String_*_":\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="72319-216">**vshadow** **-WX** **{**_beschreiterid_*_}: \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-216">**vshadow** **-wx** **{**_WriterID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>
-   <span data-ttu-id="72319-217">**vshadow** **-WX** **{**_InstanceId_*_}: \\_*_LogicalPath_ *_\\_* _componentname_</span><span class="sxs-lookup"><span data-stu-id="72319-217">**vshadow** **-wx** **{**_InstanceID_*_}:\\_*_LogicalPath_*_\\_*_ComponentName_</span></span>

<span data-ttu-id="72319-218">In den folgenden Beispielen wird gezeigt, wie Sie das optionale Flag **-WX** verwenden.</span><span class="sxs-lookup"><span data-stu-id="72319-218">The following examples show how to use the **-wx** optional flag.</span></span>

-   <span data-ttu-id="72319-219">Angeben von " *Write Name*: \\ *LogicalPath* \\ *componentname*":</span><span class="sxs-lookup"><span data-stu-id="72319-219">Specifying *WriterName*:\\*LogicalPath*\\*ComponentName*:</span></span>

    <span data-ttu-id="72319-220">**vshadow-WX = "registrierungswriter: \\ Registrierung"**</span><span class="sxs-lookup"><span data-stu-id="72319-220">**vshadow -wx="Registry Writer:\\Registry"**</span></span>

-   <span data-ttu-id="72319-221">Angeben von {*Write ID*}:</span><span class="sxs-lookup"><span data-stu-id="72319-221">Specifying {*WriterID*}:</span></span>

    <span data-ttu-id="72319-222">**vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span><span class="sxs-lookup"><span data-stu-id="72319-222">**vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**</span></span>

-   <span data-ttu-id="72319-223">Angeben von mehr als einem Writer oder einer Komponente:</span><span class="sxs-lookup"><span data-stu-id="72319-223">Specifying more than one writer or component:</span></span>

    <span data-ttu-id="72319-224">**vshadow-WX = "Registry Writer: \\ Registry"-WX = "com+ RegDB Writer"**</span><span class="sxs-lookup"><span data-stu-id="72319-224">**vshadow -wx="Registry Writer:\\Registry" -wx="COM+ REGDB Writer"**</span></span>

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="72319-225">Unterbrechen von schattenkopiesätzen mithilfe der breaksnapshotsetex-Methode</span><span class="sxs-lookup"><span data-stu-id="72319-225">Breaking Shadow Copy Sets Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="72319-226">In den folgenden Beispielen wird gezeigt, wie die Befehlszeilenoption **-BEx** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="72319-226">The following examples show how to use the **-bex** command-line option.</span></span>

-   <span data-ttu-id="72319-227">Angeben, dass die LUN der Schatten Kopie vom Host maskiert werden soll:</span><span class="sxs-lookup"><span data-stu-id="72319-227">Specifying that the shadow copy LUN will be masked from the host:</span></span>

    <span data-ttu-id="72319-228">**vshadow** **-BEx** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="72319-228">**vshadow** **-bex** **-mask**</span></span>

-   <span data-ttu-id="72319-229">Angeben, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht werden soll:</span><span class="sxs-lookup"><span data-stu-id="72319-229">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume:</span></span>

    <span data-ttu-id="72319-230">**vshadow** **-BEx** **-RW**</span><span class="sxs-lookup"><span data-stu-id="72319-230">**vshadow** **-bex** **-rw**</span></span>

-   <span data-ttu-id="72319-231">Angeben, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht wird, und dass keine der Datenträger Signaturen in den schattenkopieluns auf die der ursprünglichen LUNs zurückgesetzt werden:</span><span class="sxs-lookup"><span data-stu-id="72319-231">Specifying that the shadow copy LUN will be exposed to the host as a read/write volume, and that none of the disk signatures on the shadow copy LUNs will be reverted to that of the original LUNs:</span></span>

    <span data-ttu-id="72319-232">**vshadow** **-BEx** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="72319-232">**vshadow** **-bex** **-norevert**</span></span>

 

 
