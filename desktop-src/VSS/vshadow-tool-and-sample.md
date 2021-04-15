---
description: Vshadow ist ein Befehlszeilen Tool, das Sie zum Erstellen und Verwalten von Volumeschattenkopien verwenden können.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Vshadow-Tool und-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485027"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="7916a-103">Vshadow-Tool und-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7916a-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="7916a-104">Vshadow ist ein Befehlszeilen Tool, das Sie zum Erstellen und Verwalten von Volumeschattenkopien verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7916a-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-105">Vshadow ist im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="7916a-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="7916a-106">Das VSS 7,2 SDK enthält eine Version von vshadow, die nur unter Windows Server 2003 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="7916a-107">Weitere Informationen zum Herunterladen der Windows SDK und des VSS 7,2 SDK finden Sie unter [Volumeschattenkopie-Dienst](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="7916a-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="7916a-108">Das vshadow-Tool verwendet Befehlszeilenoptionen und optionale Flags, um die auszuführenden Aufgaben zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7916a-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="7916a-109">Bei Verwendung ohne Befehlszeilenoptionen erstellt der vshadow-Befehl einen neuen Schattenkopiesatz.</span><span class="sxs-lookup"><span data-stu-id="7916a-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="7916a-110">Vshadow-Befehle führen die folgenden Vorgänge aus:</span><span class="sxs-lookup"><span data-stu-id="7916a-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="7916a-111">Erstellen eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="7916a-112">Importieren eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="7916a-113">Abfragen von schattenkopieeigenschaften</span><span class="sxs-lookup"><span data-stu-id="7916a-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="7916a-114">Löschen von Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="7916a-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="7916a-115">Unterbrechen eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="7916a-116">Unterbrechen eines schattenkopiessets mithilfe der breaksnapshotsetex-Methode</span><span class="sxs-lookup"><span data-stu-id="7916a-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="7916a-117">Lokales verfügbar machen einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="7916a-118">Remote verfügbar machen einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="7916a-119">Auflisten des Writer-Status und der Metadaten</span><span class="sxs-lookup"><span data-stu-id="7916a-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="7916a-120">Ausführen von Wiederherstellungsoperationen</span><span class="sxs-lookup"><span data-stu-id="7916a-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="7916a-121">Zurücksetzen auf eine vorherige Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="7916a-122">Neusynchronisierung von LUNs</span><span class="sxs-lookup"><span data-stu-id="7916a-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="7916a-123">Erstellen eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="7916a-124">**vshadow** \[ Optionalflags \] *volumelist*</span><span class="sxs-lookup"><span data-stu-id="7916a-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="7916a-125">Dieser Befehl erstellt einen neuen Schattenkopiesatz.</span><span class="sxs-lookup"><span data-stu-id="7916a-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="7916a-126">*Volumelist* ist eine Liste von Volumenamen.</span><span class="sxs-lookup"><span data-stu-id="7916a-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="7916a-127">Vshadow erstellt eine Schatten Kopie für jedes Volume in der Liste.</span><span class="sxs-lookup"><span data-stu-id="7916a-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="7916a-128">Ein Volumename kann optional mit einem umgekehrten Schrägstrich ( \\ ) beendet werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="7916a-129">Beispielsweise sind "c:" und "c:" \\ gültige Volumenamen.</span><span class="sxs-lookup"><span data-stu-id="7916a-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="7916a-130">Sie können auch bereitgestellte Ordner (z. b. C: \\ Directoren Name) oder VolumeGuid-Namen angeben (z. b. \\ \\ ? \\ Volume {edbed95e-7e8d-11d8-9d01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="7916a-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="7916a-131">*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7916a-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7916a-132">Optionaler Flagwert</span><span class="sxs-lookup"><span data-stu-id="7916a-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="7916a-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7916a-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7916a-134"><span id="-ad"></span><span id="-AD"></span><strong>-AD</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-135">Dieses optionale Flag gibt differenzielle Hardware Schatten Kopien an.</span><span class="sxs-lookup"><span data-stu-id="7916a-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="7916a-136">Dieses Flag und das <strong>-AP-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-137">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-139">Dieses optionale Flag gibt Plex-Hardware Schatten Kopien an.</span><span class="sxs-lookup"><span data-stu-id="7916a-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="7916a-140">Dieses Flag und das <strong>-AD-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-141">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>File</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-143">Dieses optionale Flag gibt nicht transportable-Schatten Kopien an und speichert das Dokument mit den Sicherungs Komponenten in der angegebenen Datei.</span><span class="sxs-lookup"><span data-stu-id="7916a-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="7916a-144">Diese Datei kann in einem nachfolgenden Wiederherstellungs Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="7916a-145">Dieses Flag und das <strong>-t-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-146">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec =</strong><em>Befehl</em></span><span class="sxs-lookup"><span data-stu-id="7916a-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="7916a-148">Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schatten Kopien erstellt wurden, aber bevor das vshadow-Tool beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="7916a-149">Der <em>Befehl</em> kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="7916a-150">Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-151">Aus Sicherheitsgründen und um die Implementierung einfach zu halten, akzeptiert das optionale Flag <strong>-exec</strong> keine Parameter, die an den Befehl oder das Skript weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="7916a-152">Die gesamte Zeichenfolge, die an das optionale Flag <strong>-exec</strong> übergeben wird, wird als einzelne cmd-oder exe-Datei behandelt.</span><span class="sxs-lookup"><span data-stu-id="7916a-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="7916a-153">Weitere Informationen zu dieser Einschränkung finden Sie im vshadow-Quellcode.</span><span class="sxs-lookup"><span data-stu-id="7916a-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-155">Dieses optionale Flag gibt an, dass der Schattenkopievorgang nur dann abgeschlossen werden soll, wenn alle Datenträger Signaturen wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7916a-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-156">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-157"><strong>Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-158"><span id="-mask"></span><span id="-MASK"></span><strong>-Mask</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-159">Dieses optionale Flag gibt an, dass die schattenkopieluns vom Computer maskiert werden sollen, wenn der Schattenkopiesatz beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-160">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-161"><strong>Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-162"><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-163">Dieses optionale Flag gibt Schatten Kopien ohne automatische Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="7916a-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="7916a-164">Weitere Informationen zu dieser Option finden Sie in der Dokumentation für das VSS_VOLSNAP_ATTR_NO_AUTORECOVERY-Flag der <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="7916a-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-166">Dieses optionale Flag gibt an, dass Datenträger Signaturen nicht rückgängig gemacht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7916a-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-167">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-168"><strong>Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-170">Dieses optionale Flag gibt Schatten Kopien an, ohne dass Writer einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="7916a-171">Weitere Informationen zu Schatten Kopien ohne Writer-Beteiligung finden Sie unter <a href="shadow-copy-creation-details.md">Details zur Erstellung von Schatten</a>Kopien.</span><span class="sxs-lookup"><span data-stu-id="7916a-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="7916a-172">Dieses Flag und die Flags " <strong>-Wi</strong> " und " <strong>-WX</strong> " schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-174">Dieses optionale Flag gibt <a href="vssgloss-p.md"><em>persistente Schatten Kopien</em></a>an.</span><span class="sxs-lookup"><span data-stu-id="7916a-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-175">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-177">Dieses optionale Flag gibt an, dass die schattenkopieluns als Lese-/Schreibzugriff festgelegt werden, wenn der Schattenkopiesatz</span><span class="sxs-lookup"><span data-stu-id="7916a-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-178">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-179"><strong>Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-SCSF</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-181">Dieses optionale Flag gibt die <a href="vssgloss-c.md"><em>Client zugänglichen Schatten Kopien</em></a>an.</span><span class="sxs-lookup"><span data-stu-id="7916a-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-182">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-Script =</strong><em>File</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-184">Dieses optionale Flag generiert eine cmd-Datei, die Umgebungsvariablen enthält, die sich auf die erstellten Schatten Kopien beziehen, z. b. schattenkopienids und IDs von Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="7916a-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>File</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-186">Dieses optionale Flag gibt austauschen-Schatten Kopien an und speichert das Dokument mit den Sicherungs Komponenten in der Datei, die durch den <em>File.xml</em> -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="7916a-187">Diese Datei kann in einem nachfolgenden Import-und/oder Wiederherstellungs Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="7916a-188">Dieses Flag und das <strong>-BC-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="7916a-189"><strong>Windows Server 2003, Standard Edition und Windows Server 2003, Web Edition:</strong> Transportable-Schatten Kopien werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="7916a-190">Alle Editionen von Windows Server 2003 mit Service Pack 1 (SP1) unterstützen austauschen-Schatten Kopien.</span><span class="sxs-lookup"><span data-stu-id="7916a-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-192">Dieses optionale Flag gibt an, dass die TxF-Wiederherstellung während der Erstellung von Schatten Kopien erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7916a-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-193">Dieses Flag wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-Ablauf Verfolgung</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-195">Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7916a-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-Wait</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-197">Dieses optionale Flag bewirkt, dass das vshadow-Tool vor dem Beenden auf eine Benutzer Bestätigung wartet.</span><span class="sxs-lookup"><span data-stu-id="7916a-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>Writer</em></span><span class="sxs-lookup"><span data-stu-id="7916a-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="7916a-199">Dieses optionale Flag überprüft, ob der angegebene Writer oder die angegebene Komponente in der Schatten Kopie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="7916a-200">Der <em>Writer</em> kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="7916a-201">Dieses Flag und das <strong>-NW-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7916a-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>Writer</em></span><span class="sxs-lookup"><span data-stu-id="7916a-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="7916a-203">Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente von der Schatten Kopie ausgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="7916a-204">Der <em>Writer</em> kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="7916a-205">Dieses Flag und das <strong>-NW-</strong> Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="7916a-206">Importieren eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="7916a-207">**vshadow** \[ Optionalflags \] **-i =**_File_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="7916a-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="7916a-208">Mit der Befehlszeilenoption **-i** wird ein austauschen-Schattenkopiesatz importiert.</span><span class="sxs-lookup"><span data-stu-id="7916a-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-209">Diese Befehlszeilenoption wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="7916a-210">Bei der *File.xml* -Datei muss es sich um eine Sicherungs Komponenten-Dokument Datei für einen austauschen-Schatten Kopier Satz handeln, der mit dem optionalen **-t-** oder **-BC-** Flag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7916a-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="7916a-211">Ein Schattenkopiesatz ist eine [*persistente Schatten Kopie*](vssgloss-p.md) , wenn er mit dem optionalen **-p-** Flag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7916a-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="7916a-212">Wenn der über austauschen Schattenkopiesatz nicht persistent ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schatten Kopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="7916a-213">Sie können nicht persistente Schatten Kopien nur während der Erstellung von Schatten Kopien importieren, indem Sie den Schattenkopiesatz erstellen, indem Sie das optionale Flag **-exec** zum Ausführen einer cmd-Datei verwenden, die vshadow **-i** aufruft.</span><span class="sxs-lookup"><span data-stu-id="7916a-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="7916a-214">Die Befehlszeilenoption " **-i** " kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="7916a-215">*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7916a-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="7916a-216">Optionaler Flagwert</span><span class="sxs-lookup"><span data-stu-id="7916a-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="7916a-217">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7916a-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7916a-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_Befehl_</span><span class="sxs-lookup"><span data-stu-id="7916a-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="7916a-219">Dieses optionale Flag führt einen Befehl oder ein Skript aus, nachdem die Schatten Kopien importiert wurden, aber bevor das vshadow-Tool beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="7916a-220">Der *Befehl* kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="7916a-221">Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="7916a-222"><span id="-tracing"></span><span id="-TRACING"></span>**-Ablauf Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="7916a-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="7916a-223">Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7916a-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="7916a-224"><span id="-wait"></span><span id="-WAIT"></span>**-Wait**</span><span class="sxs-lookup"><span data-stu-id="7916a-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="7916a-225">Dieses optionale Flag bewirkt, dass das vshadow-Tool vor dem Beenden auf eine Benutzer Bestätigung wartet.</span><span class="sxs-lookup"><span data-stu-id="7916a-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="7916a-226">Abfragen von schattenkopieeigenschaften</span><span class="sxs-lookup"><span data-stu-id="7916a-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="7916a-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="7916a-227">**vshadow** **-q**</span></span>

<span data-ttu-id="7916a-228">**vshadow** **-qx =**_Shadowcopy\* TID_</span><span class="sxs-lookup"><span data-stu-id="7916a-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="7916a-229">**vshadow** **-s =**_shadowcopyid_</span><span class="sxs-lookup"><span data-stu-id="7916a-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="7916a-230">Die Befehlszeilenoption **-q** listet die Eigenschaften aller Schatten Kopien auf dem Computer auf.</span><span class="sxs-lookup"><span data-stu-id="7916a-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="7916a-231">Die Befehlszeilenoption **-qx** listet die Eigenschaften aller Schatten Kopien im Schattenkopiesatz auf, deren ID von *shadowcopysetid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="7916a-232">Die Befehlszeilenoption **-s** listet die Eigenschaften der Schatten Kopie auf, deren ID von *shadowcopyid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="7916a-233">Diese Befehlszeilenoptionen verwenden eine Kombination aus [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) und [**IVssBackupComponents:: getionnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) , um die Eigenschaften des angegebenen Satzes von Schatten Kopien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7916a-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="7916a-234">Die Befehlszeilenoptionen **-q**, **-qx** und **-s** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="7916a-235">Löschen von Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="7916a-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="7916a-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="7916a-236">**vshadow** **-da**</span></span>

<span data-ttu-id="7916a-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="7916a-237">**vshadow** **-do**</span></span>

<span data-ttu-id="7916a-238">**vshadow** **-DX =**_Shadowcopy\* TID_</span><span class="sxs-lookup"><span data-stu-id="7916a-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="7916a-239">**vshadow** **-DS =**_shadowcopyid_</span><span class="sxs-lookup"><span data-stu-id="7916a-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="7916a-240">Der **-da-** Befehl löscht alle Schatten Kopien auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7916a-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-241">Die Befehlszeilenoption " **-da** " erfordert eine Bestätigung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7916a-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="7916a-242">Mit der Befehlszeilenoption **-DO** wird die älteste Schatten Kopie auf dem Computer gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7916a-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="7916a-243">Mit der Befehlszeilenoption **-DX** werden alle Schatten Kopien im Schattenkopiesatz gelöscht, deren ID von *shadowcopysetid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="7916a-244">Die Befehlszeilenoption **-DS** löscht die Schatten Kopie, deren ID von *shadowcopyid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="7916a-245">Diese Befehlszeilenoptionen sind nur für die Verwendung mit [*permanenten Schatten Kopien*](vssgloss-p.md) vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="7916a-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="7916a-246">Nicht persistente Schatten Kopien müssen nicht explizit gelöscht werden, da Sie automatisch gelöscht werden, wenn der vshadow-Erstellungs Befehl beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="7916a-247">Die Befehlszeilenoptionen " **-da**", "- **do**", " **-DX**" und " **-DS** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="7916a-248">Unterbrechen eines schattenkopiesatzes</span><span class="sxs-lookup"><span data-stu-id="7916a-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="7916a-249">**vshadow** **-b =**_Shadowcopy\* TID_</span><span class="sxs-lookup"><span data-stu-id="7916a-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="7916a-250">**vshadow** **-BW =**_Shadowcopy\* TID_</span><span class="sxs-lookup"><span data-stu-id="7916a-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="7916a-251">Mit der Befehlszeilenoption **-b =**_shadowcopysetid_ wird jede Schatten Kopie im Schattenkopiesatz in ein eigenständiges Schreib geschütztes Volume konvertiert.</span><span class="sxs-lookup"><span data-stu-id="7916a-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="7916a-252">Die Befehlszeilenoption **-BW =**_shadowcopysetid_ konvertiert jede Schatten Kopie im Schattenkopiesatz in ein eigenständiges beschreibbares Volume.</span><span class="sxs-lookup"><span data-stu-id="7916a-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-253">Die Befehlszeilenoptionen **-b** und **-BW** werden nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="7916a-254">Informationen zum Unterbrechen eines schattenkopiessets finden Sie unter [Breaking Shadow-Kopien](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="7916a-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="7916a-255">Nachdem der Schattenkopiesatz getrennt wurde, sind der Schattenkopiesatz und die einzelnen Schatten Kopien nicht mehr vorhanden und können nicht mithilfe von VSS-Befehlen verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="7916a-256">Ein Schattenkopiesatz ist persistent, wenn er mit dem optionalen **-p-** Flag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7916a-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="7916a-257">Wenn der über austauschen Schattenkopiesatz nicht persistent ist, wird er für kurze Zeit angezeigt, während der Befehl zum Erstellen von Schatten Kopien ausgeführt wird, und wird automatisch gelöscht, wenn der Befehl zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="7916a-258">Sie können nicht persistente Schatten Kopien nur während der Erstellung von Schatten Kopien unterbrechen, indem Sie den Schattenkopiesatz erstellen, indem Sie das optionale Flag **-exec** verwenden, um eine cmd-Datei auszuführen, die **vshadow** **-b** oder **vshadow** **-BW** aufruft.</span><span class="sxs-lookup"><span data-stu-id="7916a-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="7916a-259">Die Befehlszeilenoptionen " **-b** " und " **-BW** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="7916a-260">Unterbrechen eines schattenkopiessets mithilfe der breaksnapshotsetex-Methode</span><span class="sxs-lookup"><span data-stu-id="7916a-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="7916a-261">**vshadow** **-BEx**</span><span class="sxs-lookup"><span data-stu-id="7916a-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="7916a-262">Die Befehlszeilenoption " **-BEx** " unterbricht einen Schattenkopiesatz gemäß den Optionen, die durch die optionalen **-Mask-**,- **RW**-, **-forcerevert**-und **-norevert** -Flags angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="7916a-263">Diese Befehlszeilenoption ähnelt den Befehlszeilenoptionen **-b** und **-BW** .</span><span class="sxs-lookup"><span data-stu-id="7916a-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="7916a-264">Die Befehlszeilenoption **-BEx** verwendet die [**IVssBackupComponentsEx2:: breaksnapshotsetex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) -Methode, wohingegen die Befehlszeilenoptionen **-b** und **-BW** die [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="7916a-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="7916a-265">Informationen zum Unterbrechen eines schattenkopiessets finden Sie unter [Breaking Shadow-Kopien](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="7916a-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="7916a-266">Die Befehlszeilenoption **-BEx** wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="7916a-267">**vshadow** **-BEx** **-Mask**</span><span class="sxs-lookup"><span data-stu-id="7916a-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="7916a-268">Das Flag **-Mask** gibt an, dass die LUN der Schatten Kopie vom Host maskiert wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="7916a-269">Wenn das Flag " **-Mask** " angegeben ist, können die Flags " **-RW**", " **-forcerevert**" und " **-norevert** " nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="7916a-270">**vshadow** **-BEx** **-RW**</span><span class="sxs-lookup"><span data-stu-id="7916a-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="7916a-271">Das Flag **-RW** gibt an, dass die LUN der Schatten Kopie als Lese-/schreibvolume für den Host verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="7916a-272">**vshadow** **-BEx** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="7916a-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="7916a-273">Das Flag " **-forcerevert** " gibt an, dass die Datenträger Bezeichner aller schattenkopieluns auf die der ursprünglichen LUNs zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="7916a-274">Wenn jedoch eine der ursprünglichen LUNs auf dem System vorhanden ist, schlägt der Vorgang fehl, und keiner der Bezeichner wird wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="7916a-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="7916a-275">Dieses Flag und das **-norevert-** Flag schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="7916a-276">**vshadow** **-BEx** **-norevert**</span><span class="sxs-lookup"><span data-stu-id="7916a-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="7916a-277">Das Flag " **-norevert** " gibt an, dass keine der Datenträger-IDs der schattenkopiedatenträger wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="7916a-278">Dieses Flag und das Flag " **-forcerevert** " schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="7916a-279">Lokales verfügbar machen einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="7916a-280">**vshadow** **-El =**_shadowcopyid_*_,_*_localemptydirectory_</span><span class="sxs-lookup"><span data-stu-id="7916a-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="7916a-281">**vshadow** **-El =**_shadowcopyid_*_,_*_unuseddriveletter_</span><span class="sxs-lookup"><span data-stu-id="7916a-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="7916a-282">Mit der Befehlszeilenoption-El wird einem permanenten Schatten Kopiervorgang ein bereit **gestellter** Ordner oder ein Laufwerksbuchstabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7916a-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="7916a-283">Beachten Sie, dass die volumeinhalte schreibgeschützt bleiben, es sei denn, Sie nennen anschließend **vshadow** **-BW** , um den Schattenkopiesatz zu unterbrechen</span><span class="sxs-lookup"><span data-stu-id="7916a-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-284">Nicht persistente Schatten Kopien und [*Client barrierefreie Schatten Kopien*](vssgloss-c.md) können nicht lokal verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="7916a-285">Wenn {edbed95e-7e8d-11d8-9d01-505054503030} z. b. die GUID einer vorhandenen persistenten Schatten Kopie und X: ein nicht verwendeter Laufwerk Buchstabe ist, macht der folgende Befehl die Schatten Kopie unter X verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7916a-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="7916a-286">**vshadow** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, x:**</span><span class="sxs-lookup"><span data-stu-id="7916a-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="7916a-287">Im folgenden Beispiel wird gezeigt, wie die gleiche Schatten Kopie unter dem bereitgestellten Ordner C: \\ Shadowcopy June23 verfügbar gemacht wird \\ :</span><span class="sxs-lookup"><span data-stu-id="7916a-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="7916a-288">**mkdir c: \\ shadowkopien \\ June23**</span><span class="sxs-lookup"><span data-stu-id="7916a-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="7916a-289">**vshadow** **-El = {edbed95e-7e8d-11d8-9d01-505054503030}, c: \\ shadowkopien \\ June23**</span><span class="sxs-lookup"><span data-stu-id="7916a-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="7916a-290">Die Befehlszeilenoption **-El** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="7916a-291">Remote verfügbar machen einer Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="7916a-292">**vshadow** **-er =**_shadowcopyid_*_,_*_unusedsharename_</span><span class="sxs-lookup"><span data-stu-id="7916a-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="7916a-293">**vshadow** **-er =**_shadowcopyid_*_,_*_unusedsharename_*_,_*_pathfromrootonshadow_</span><span class="sxs-lookup"><span data-stu-id="7916a-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="7916a-294">Die Befehlszeilenoption **-er** weist der Schatten Kopie einen schreibgeschützten Freigabe Namen (oder ein Unterverzeichnis) dem Stammverzeichnis zu.</span><span class="sxs-lookup"><span data-stu-id="7916a-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="7916a-295">Beachten Sie, dass der Inhalt der Freigabe weiterhin schreibgeschützt bleibt, es sei denn, Sie werden anschließend **vshadow** **-BW** aufgerufen, um den Schattenkopiesatz</span><span class="sxs-lookup"><span data-stu-id="7916a-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-296">Die vom [*Client zugänglichen Schatten Kopien*](vssgloss-c.md) können nicht Remote verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="7916a-297">Wenn {edbed95e-7e8d-11d8-9d01-505054503030} z. b. die GUID einer vorhandenen persistenten Schatten Kopie und Share 123 ein nicht verwendeter \_ Freigabe Name ist, macht der folgende Befehl die Schatten Kopie unter Freigabe \_ 123 verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7916a-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="7916a-298">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, Freigabe \_ 123**</span><span class="sxs-lookup"><span data-stu-id="7916a-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="7916a-299">Im folgenden Beispiel wird gezeigt, wie Sie nur eine Teilstruktur (mit dem Namen "" Ordner1 " \\ Folder2") derselben Schatten Kopie in derselben Freigabe verfügbar machen:</span><span class="sxs-lookup"><span data-stu-id="7916a-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="7916a-300">**vshadow** **-er = {edbed95e-7e8d-11d8-9d01-505054503030}, Freigabe \_ 123, "Ordner1" \\ Folder2**</span><span class="sxs-lookup"><span data-stu-id="7916a-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="7916a-301">Die Befehlszeilenoption **-er** kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="7916a-302">Auflisten des Writer-Status und der Metadaten</span><span class="sxs-lookup"><span data-stu-id="7916a-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="7916a-303">**vshadow** **-WS**</span><span class="sxs-lookup"><span data-stu-id="7916a-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="7916a-304">**vshadow** **-WM**</span><span class="sxs-lookup"><span data-stu-id="7916a-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="7916a-305">**vshadow** **-wm2**</span><span class="sxs-lookup"><span data-stu-id="7916a-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="7916a-306">**vshadow** **-WM3**</span><span class="sxs-lookup"><span data-stu-id="7916a-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="7916a-307">Mit der Befehlszeilenoption **-WS** werden die VSS-Writer aufgelistet, die derzeit auf dem Computer ausgeführt werden, und Ihr Status wird beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7916a-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="7916a-308">Dieser Befehl entspricht dem Befehl [vssadmin List Writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="7916a-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="7916a-309">Es gibt sechs mögliche Zustands Werte: "stabil", "Fehler", "unbekannt", "warten auf Einfrieren", "fixiert" und "warten auf Abschluss</span><span class="sxs-lookup"><span data-stu-id="7916a-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="7916a-310">Die Befehlszeilenoption **-WM** listet eine Zusammenfassung der Writer-Metadaten auf, einschließlich der betroffenen Volumes.</span><span class="sxs-lookup"><span data-stu-id="7916a-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="7916a-311">Die Befehlszeilenoption **-wm2** listet alle Writer-Metadaten auf.</span><span class="sxs-lookup"><span data-stu-id="7916a-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="7916a-312">Die Befehlszeilenoption **-WM3** listet alle Writer-Metadaten im unformatierten XML-Format auf.</span><span class="sxs-lookup"><span data-stu-id="7916a-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="7916a-313">**Windows Vista und Windows Server 2003:** Die Befehlszeilenoption **-WM3** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="7916a-314">Sie können diese Informationen verwenden, um zu bestimmen, welche Volumes in den Volumeschattenkopie-Satz eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7916a-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-315">Wenn der Writer-Zustand stabil ist oder auf den Abschluss wartet, kann der Writer als stabiler Zustand angesehen werden, der für die nächste Sicherung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="7916a-316">Die Befehlszeilenoptionen **-WS**, **-WM**, **-wm2** und **-WM3** schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="7916a-317">Ausführen von Wiederherstellungsoperationen</span><span class="sxs-lookup"><span data-stu-id="7916a-317">Performing Restore Operations</span></span>

<span data-ttu-id="7916a-318">**vshadow** \[ Optionalflags \] **-r =**_File_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="7916a-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="7916a-319">**vshadow** \[ Optionalflags \] **-RS =**_File_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="7916a-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="7916a-320">Die Befehlszeilenoption **-r** führt einen Wiederherstellungs Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="7916a-321">Die Befehlszeilenoption **-RS** führt einen simulierten Wiederherstellungs Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="7916a-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="7916a-322">Die *File.xml* Datei muss eine Sicherungs Komponenten-Dokument Datei für einen Schattenkopiesatz sein, der mit dem optionalen **-t-** oder **-BC-** Flag erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7916a-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="7916a-323">Die Befehlszeilenoptionen " **-r** " und " **-RS** " schließen sich gegenseitig aus und können nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="7916a-324">*Optionalflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7916a-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="7916a-325">Optionaler Flagwert</span><span class="sxs-lookup"><span data-stu-id="7916a-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="7916a-326">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7916a-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7916a-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_Writer_</span><span class="sxs-lookup"><span data-stu-id="7916a-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="7916a-328">Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente in die Wiederherstellung eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="7916a-329">Der *Writer* kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="7916a-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_Writer_</span><span class="sxs-lookup"><span data-stu-id="7916a-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="7916a-331">Dieses optionale Flag überprüft, ob der angegebene Writer oder die Komponente von der Wiederherstellung ausgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7916a-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="7916a-332">Der *Writer* kann einen Komponenten Pfad, einen Writer-Namen, eine Writer-ID oder eine Writer-Instanz-ID angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="7916a-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec =**_Befehl_</span><span class="sxs-lookup"><span data-stu-id="7916a-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="7916a-334">Dieses optionale Flag führt einen Befehl oder ein Skript zwischen den Ereignissen vor und nach der Wiederherstellung aus, die an die Writer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="7916a-335">Der *Befehl* kann einen ausführbaren Shellbefehl oder eine cmd-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="7916a-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="7916a-336">Wenn Sie einen Shellbefehl angibt, können keine Befehlsparameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="7916a-337"><span id="-tracing"></span><span id="-TRACING"></span>**-Ablauf Verfolgung**</span><span class="sxs-lookup"><span data-stu-id="7916a-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="7916a-338">Dieses optionale Flag generiert eine ausführliche Ausgabe, die für die Problembehandlung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7916a-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="7916a-339">Zurücksetzen auf eine vorherige Schatten Kopie</span><span class="sxs-lookup"><span data-stu-id="7916a-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="7916a-340">**vshadow** **-Revert =**_shadowcopyid_</span><span class="sxs-lookup"><span data-stu-id="7916a-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="7916a-341">Diese Befehlszeilenoption wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="7916a-342">**Windows Server 2008 und Windows Server 2003:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="7916a-343">Mit der Befehlszeilenoption **-Revert** wird ein Volume auf die vorherige Schatten Kopie zurückgesetzt, deren ID von *shadowcopyid* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7916a-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="7916a-344">Die Befehlszeilenoption ' **-Revert** ' kann nicht mit anderen Befehlszeilenoptionen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="7916a-345">Neusynchronisierung von LUNs</span><span class="sxs-lookup"><span data-stu-id="7916a-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="7916a-346">**vshadow** **-adresssync =**_shadowcopyid_ **-Resync =**_bcdfilename_ \[ optionalresyncflags\]</span><span class="sxs-lookup"><span data-stu-id="7916a-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="7916a-347">**vshadow** **-adresssync =**_shadowcopyid_*_,_* *targetvolumedriveletter* **-Resync =**_bcdfilename_ \[ optionalresyncflags\]</span><span class="sxs-lookup"><span data-stu-id="7916a-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="7916a-348">Mit der Befehlszeilenoption **-adresssync** werden die Volumes angegeben, die in einen LUN-Neusynchronisierungs Vorgang eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7916a-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="7916a-349">Der *shadowcopyid* -Parameter gibt den Bezeichner der Schatten Kopie an.</span><span class="sxs-lookup"><span data-stu-id="7916a-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="7916a-350">Der optionale Parameter *targetvolumedriveletter* gibt das Ziel Volume an, in das der Inhalt des schattenkopiespeichervolumes kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7916a-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="7916a-351">Mit der Befehlszeilenoption **-Resync** wird ein LUN-Vorgang für die erneute Synchronisierung initiiert.</span><span class="sxs-lookup"><span data-stu-id="7916a-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="7916a-352">Nachdem der Vorgang beendet wurde, sollte die Signatur der einzelnen Ziel-LUN mit der Signatur der Ziel Volume-LUN identisch sein.</span><span class="sxs-lookup"><span data-stu-id="7916a-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="7916a-353">Der *bcdfilename* -Parameter gibt den Namen der XML-Datei an, die das Sicherungs Komponenten Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="7916a-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="7916a-354">Die Befehlszeilenoptionen **-adresssync** und **-Resync** werden nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="7916a-355">**Windows Server 2008 und Windows Server 2003:** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="7916a-356">*Optionalresyncflags* ist eine Bitmaske Optionaler Flagwerte aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7916a-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7916a-357">Optionaler Flagwert</span><span class="sxs-lookup"><span data-stu-id="7916a-357">Optional flag value</span></span></th>
<th><span data-ttu-id="7916a-358">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7916a-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7916a-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-360">Dieses optionale Flag gibt an, dass die Signatur der einzelnen Ziel-LUN nach Abschluss des Vorgangs mit der ursprünglichen LUN identisch sein sollte, mit der die Schatten Kopie erstellt wurde, nicht mit der Ziel Volume-LUN.</span><span class="sxs-lookup"><span data-stu-id="7916a-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-361">Das Flag " <strong>-revertsig</strong> " wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-362"><strong>Windows Server 2008 und Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7916a-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="7916a-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="7916a-364">Dieses optionale Flag gibt an, dass der VSS-Dienst nicht nach nicht ausgewählten Volumes suchen soll, die durch den LUN-Vorgang zum erneuten Synchronisieren überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7916a-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7916a-365">Das Flag " <strong>-novolcheck</strong> " wird nur unter Windows Server-Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="7916a-366"><strong>Windows Server 2008 und Windows Server 2003:</strong> Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7916a-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
