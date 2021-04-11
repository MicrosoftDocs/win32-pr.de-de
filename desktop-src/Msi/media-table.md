---
description: In der Medien Tabelle wird der Satz von Datenträgern beschrieben, aus denen die-Quell Medien für die-Installation gemacht werden.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Medien Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351258"
---
# <a name="media-table"></a><span data-ttu-id="be283-103">Medien Tabelle</span><span class="sxs-lookup"><span data-stu-id="be283-103">Media Table</span></span>

<span data-ttu-id="be283-104">In der Medien Tabelle wird der Satz von Datenträgern beschrieben, aus denen die-Quell Medien für die-Installation gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="be283-104">The Media table describes the set of disks that make up the source media for the installation.</span></span>

<span data-ttu-id="be283-105">Die Medien Tabelle enthält die Spalten, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="be283-105">The Media table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="be283-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="be283-106">Column</span></span>       | <span data-ttu-id="be283-107">Typ</span><span class="sxs-lookup"><span data-stu-id="be283-107">Type</span></span>                     | <span data-ttu-id="be283-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="be283-108">Key</span></span> | <span data-ttu-id="be283-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="be283-109">Nullable</span></span> |
|--------------|--------------------------|-----|----------|
| <span data-ttu-id="be283-110">DiskId</span><span class="sxs-lookup"><span data-stu-id="be283-110">DiskId</span></span>       | [<span data-ttu-id="be283-111">Integer</span><span class="sxs-lookup"><span data-stu-id="be283-111">Integer</span></span>](integer.md)   | <span data-ttu-id="be283-112">J</span><span class="sxs-lookup"><span data-stu-id="be283-112">Y</span></span>   | <span data-ttu-id="be283-113">N</span><span class="sxs-lookup"><span data-stu-id="be283-113">N</span></span>        |
| <span data-ttu-id="be283-114">LastSequence</span><span class="sxs-lookup"><span data-stu-id="be283-114">LastSequence</span></span> | [<span data-ttu-id="be283-115">Integer</span><span class="sxs-lookup"><span data-stu-id="be283-115">Integer</span></span>](integer.md)   | <span data-ttu-id="be283-116">N</span><span class="sxs-lookup"><span data-stu-id="be283-116">N</span></span>   | <span data-ttu-id="be283-117">N</span><span class="sxs-lookup"><span data-stu-id="be283-117">N</span></span>        |
| <span data-ttu-id="be283-118">Diskprompt</span><span class="sxs-lookup"><span data-stu-id="be283-118">DiskPrompt</span></span>   | [<span data-ttu-id="be283-119">Text</span><span class="sxs-lookup"><span data-stu-id="be283-119">Text</span></span>](text.md)         | <span data-ttu-id="be283-120">N</span><span class="sxs-lookup"><span data-stu-id="be283-120">N</span></span>   | <span data-ttu-id="be283-121">J</span><span class="sxs-lookup"><span data-stu-id="be283-121">Y</span></span>        |
| <span data-ttu-id="be283-122">KEs</span><span class="sxs-lookup"><span data-stu-id="be283-122">Cabinet</span></span>      | [<span data-ttu-id="be283-123">KEs</span><span class="sxs-lookup"><span data-stu-id="be283-123">Cabinet</span></span>](cabinet.md)   | <span data-ttu-id="be283-124">N</span><span class="sxs-lookup"><span data-stu-id="be283-124">N</span></span>   | <span data-ttu-id="be283-125">J</span><span class="sxs-lookup"><span data-stu-id="be283-125">Y</span></span>        |
| <span data-ttu-id="be283-126">VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="be283-126">VolumeLabel</span></span>  | [<span data-ttu-id="be283-127">Text</span><span class="sxs-lookup"><span data-stu-id="be283-127">Text</span></span>](text.md)         | <span data-ttu-id="be283-128">N</span><span class="sxs-lookup"><span data-stu-id="be283-128">N</span></span>   | <span data-ttu-id="be283-129">J</span><span class="sxs-lookup"><span data-stu-id="be283-129">Y</span></span>        |
| <span data-ttu-id="be283-130">`Source`</span><span class="sxs-lookup"><span data-stu-id="be283-130">Source</span></span>       | [<span data-ttu-id="be283-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="be283-131">Property</span></span>](property.md) | <span data-ttu-id="be283-132">N</span><span class="sxs-lookup"><span data-stu-id="be283-132">N</span></span>   | <span data-ttu-id="be283-133">J</span><span class="sxs-lookup"><span data-stu-id="be283-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="be283-134">Spalten</span><span class="sxs-lookup"><span data-stu-id="be283-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="be283-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span><span class="sxs-lookup"><span data-stu-id="be283-135"><span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId</span></span>
</dt> <dd>

<span data-ttu-id="be283-136">Bestimmt die Sortierreihenfolge für die Tabelle.</span><span class="sxs-lookup"><span data-stu-id="be283-136">Determines the sort order for the table.</span></span> <span data-ttu-id="be283-137">Diese Zahl muss größer oder gleich 1 sein.</span><span class="sxs-lookup"><span data-stu-id="be283-137">This number must be equal to or greater than 1.</span></span>

</dd> <dt>

<span data-ttu-id="be283-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span><span class="sxs-lookup"><span data-stu-id="be283-138"><span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence</span></span>
</dt> <dd>

<span data-ttu-id="be283-139">Datei Sequenznummer für die letzte Datei für dieses Medium.</span><span class="sxs-lookup"><span data-stu-id="be283-139">File sequence number for the last file for this media.</span></span> <span data-ttu-id="be283-140">Die Zahlen in der Spalte LastSequence geben an, welche Dateien in der [Datei](file-table.md) Tabelle auf einem bestimmten Quell Datenträger gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="be283-140">The numbers in the LastSequence column specify which of the files in the [File](file-table.md) table are found on a particular source disk.</span></span> <span data-ttu-id="be283-141">Jeder Quell Datenträger enthält alle Dateien mit Sequenznummern (wie in der Sequence-Spalte der File-Tabelle angezeigt), die kleiner oder gleich dem Wert in der LastSequence-Spalte sind, und größer als der LastSequence-Wert des vorherigen Datenträgers (oder größer als 0 für den ersten Eintrag in der Medien Tabelle).</span><span class="sxs-lookup"><span data-stu-id="be283-141">Each source disk contains all files with sequence numbers (as shown in the Sequence column of the File table) less than or equal to the value in the LastSequence column, and greater than the LastSequence value of the previous disk (or greater than 0, for the first entry in the Media table).</span></span> <span data-ttu-id="be283-142">Diese Zahl darf nicht negativ sein. der maximale Grenzwert beträgt 32767 Dateien.</span><span class="sxs-lookup"><span data-stu-id="be283-142">This number must be non-negative; the maximum limit is 32767 files.</span></span> <span data-ttu-id="be283-143">Weitere Informationen zum Erstellen eines Windows Installer Pakets mit weiteren Dateien finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md).</span><span class="sxs-lookup"><span data-stu-id="be283-143">For more information about creating a Windows Installer package with more files, see [Authoring a Large Package](authoring-a-large-package.md).</span></span>

</dd> <dt>

<span data-ttu-id="be283-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>Diskprompt</span><span class="sxs-lookup"><span data-stu-id="be283-144"><span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt</span></span>
</dt> <dd>

<span data-ttu-id="be283-145">Der Datenträger Name, der in der Regel der auf dem Datenträger gedruckte sichtbare Text ist.</span><span class="sxs-lookup"><span data-stu-id="be283-145">The disk name, which is usually the visible text printed on the disk.</span></span> <span data-ttu-id="be283-146">Dieser lokalisierbare Text wird verwendet, um den Benutzer zur Eingabe aufzufordern, wenn dieser Datenträger eingefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="be283-146">This localizable text is used to prompt the user when this disk needs to be inserted.</span></span>

</dd> <dt>

<span data-ttu-id="be283-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>KEs</span><span class="sxs-lookup"><span data-stu-id="be283-147"><span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Cabinet</span></span>
</dt> <dd>

<span data-ttu-id="be283-148">Der Name der CAB-Datei, wenn einige oder alle Dateien, die auf dem Medium gespeichert sind, in eine CAB-Datei komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="be283-148">The name of the cabinet if some or all of the files stored on the media are compressed into a cabinet file.</span></span> <span data-ttu-id="be283-149">Wenn keine Schränke verwendet werden, muss diese Spalte leer sein.</span><span class="sxs-lookup"><span data-stu-id="be283-149">If no cabinets are used, this column must be blank.</span></span> <span data-ttu-id="be283-150">Der Name der CAB [-Datei muss](cabinet.md) die Syntax des CAB-Datentyps verwenden.</span><span class="sxs-lookup"><span data-stu-id="be283-150">The name of the cabinet must use the syntax of the [Cabinet](cabinet.md) data type.</span></span> <span data-ttu-id="be283-151">Windows Installer benötigt immer eine gültige Quelle zum Reparieren von Dateien, die in eingebetteten CAB-Dateien enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="be283-151">Windows Installer always requires a valid source to repair files included in embedded cabinet files.</span></span> <span data-ttu-id="be283-152">Wenn Windows Installer ein Paket installiert, das eine eingebettete CAB-Datei enthält, kann eine Kopie der CAB-Datei vom System gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="be283-152">When Windows Installer installs a package containing an embedded cabinet file, a copy of the cabinet file can be saved by the system.</span></span> <span data-ttu-id="be283-153">Diese Kopie kann nicht verwendet werden, um die CAB-Datei zu reparieren.</span><span class="sxs-lookup"><span data-stu-id="be283-153">This copy cannot be used to repair the cabinet file.</span></span> <span data-ttu-id="be283-154">Um Speicherplatz zu sparen, verwenden Sie externe CAB-Dateien anstelle von eingebetteten CAB-Dateien.</span><span class="sxs-lookup"><span data-stu-id="be283-154">To conserve disk space, use external cabinet files instead of embedded cabinet files.</span></span>

</dd> <dt>

<span data-ttu-id="be283-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="be283-155"><span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel</span></span>
</dt> <dd>

<span data-ttu-id="be283-156">Die Bezeichnung, die dem Volume zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="be283-156">The label attributed to the volume.</span></span> <span data-ttu-id="be283-157">Dies ist die Lautstärke Bezeichnung, die von der [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="be283-157">This is the volume label returned by the [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) function.</span></span> <span data-ttu-id="be283-158">Wenn die [**SourceDir**](sourcedir.md) -Eigenschaft auf ein Wechsel Datenträger (Disketten oder CD-ROM) verweist, wird diese Volumebezeichnung verwendet, um zu überprüfen, ob sich der richtige Datenträger im Laufwerk befindet, bevor versucht wird, Dateien zu installieren.</span><span class="sxs-lookup"><span data-stu-id="be283-158">If the [**SourceDir**](sourcedir.md) property refers to a removable (floppy or CD-ROM) volume, then this volume label is used to verify that the proper disk is in the drive before attempting to install files.</span></span> <span data-ttu-id="be283-159">Der Eintrag in dieser Spalte muss mit der Volumebezeichnung des physischen Mediums identisch sein.</span><span class="sxs-lookup"><span data-stu-id="be283-159">The entry in this column must match the volume label of the physical media.</span></span>

</dd> <dt>

<span data-ttu-id="be283-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs</span><span class="sxs-lookup"><span data-stu-id="be283-160"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="be283-161">Dieses Feld wird nur durch Patchen verwendet und andernfalls leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="be283-161">This field is only used by patching and is otherwise left blank.</span></span> <span data-ttu-id="be283-162">Eine patchtransformation kann hier eine Eigenschaft eingeben, bei der es sich um den Speicherort der CAB-Datei mit den Patchdateien oder um neue Dateien handelt, die vom Patch hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="be283-162">A patch transform can enter a property here that is the location of the cabinet file containing the patch files or any new files added by the patch.</span></span> <span data-ttu-id="be283-163">Für diese Dateien muss eine andere Quelle angegeben werden, da die Quelle des Patchpakets getrennt von der Produkt Quelle gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="be283-163">A different source needs to be specified for these files because the source of the patch package can be stored separately from the product's source.</span></span> <span data-ttu-id="be283-164">Wenn das CAB-Feld leer ist, ignoriert das Installationsprogramm den Wert in dieser Spalte.</span><span class="sxs-lookup"><span data-stu-id="be283-164">If the Cabinet field is empty, the installer ignores the value in this column.</span></span> <span data-ttu-id="be283-165">Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert der [**SourceDir**](sourcedir.md) -Eigenschaft als Quelle der CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="be283-165">If this field is empty, the installer uses the value of the [**SourceDir**](sourcedir.md) property as the source of the cabinet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be283-166">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be283-166">Remarks</span></span>

<span data-ttu-id="be283-167">Wenn dem CAB-Namen ein Nummern Zeichen () vorangestellt ist \# , werden die Dateien, die auf diesen Medien Tabellendaten Satz verweisen, in einer CAB-Datei verpackt, die in der Datenbank als separater Stream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="be283-167">If the cabinet name is preceded by a number sign (\#), then the files referencing this Media table record are packed in a cabinet file that is stored within the database as a separate stream.</span></span>

<span data-ttu-id="be283-168">Weitere Informationen zum Hinzufügen von schränken zu den Datei Tabellen und Medien Tabellen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="be283-168">For more information about how to add cabinets to the File tables and Media tables, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="be283-169">Windows Installer erfordert, dass sich die MSI-Datei auf dem ersten Datenträger des Wechsel Datenträgers (CD, DVD oder Diskette) befindet, der für die Installation des Produkts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be283-169">Windows Installer requires that the .msi file be on the first disk of removable media (CD, DVD or floppy) used for the product's installation.</span></span>

<span data-ttu-id="be283-170">**Bestimmen von sourcemode**</span><span class="sxs-lookup"><span data-stu-id="be283-170">**Determining the SourceMode**</span></span>

<span data-ttu-id="be283-171">Die " [**Word Count Summary**](word-count-summary.md) "-Eigenschaft bestimmt den Quell Modus für die aktuelle Installation.</span><span class="sxs-lookup"><span data-stu-id="be283-171">The [**Word Count Summary**](word-count-summary.md) property determines the source mode for the current install.</span></span> <span data-ttu-id="be283-172">Wenn diese Eigenschaft auf 2 oder 3 festgelegt ist, wird eine CAB-Installation angenommen.</span><span class="sxs-lookup"><span data-stu-id="be283-172">If this property is set to 2 or 3, a cabinet install is assumed.</span></span> <span data-ttu-id="be283-173">In diesem Modus wird davon ausgegangen, dass die CAB-Dateien im Verzeichnis vorhanden sind, das von der [**SourceDir**](sourcedir.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="be283-173">In this mode, the cabinet files are assumed to exist in the directory indicated by the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="be283-174">Wenn der Quelltyp "0" oder "1" ist, wird davon ausgegangen, dass alle Quelldateien in der Struktur vorhanden sind, deren Stamm durch die **SourceDir** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="be283-174">If the Source Type value is 0 or 1, all source files are assumed to exist in the tree whose root is indicated by the **SourceDir** property.</span></span>

<span data-ttu-id="be283-175">Beachten Sie, dass dies nur für Dateien in der Dateitabelle gilt, für die in der Spalte Attribute weder das komprimierte als auch das unkomprimierte Bit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="be283-175">Note that this only applies to files in the File table that do not have either the Compressed or Uncompressed bits set in the attributes column.</span></span> <span data-ttu-id="be283-176">Diese Bits überschreiben den Wert der [**Zusammenfassungs Eigenschaft der Wort Zählung**](word-count-summary.md) , wenn bestimmt wird, ob eine bestimmte Datei komprimiert oder unkomprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="be283-176">These bits override the value of the [**Word Count Summary**](word-count-summary.md) property when determining if a particular file is compressed or uncompressed.</span></span>

## <a name="validation"></a><span data-ttu-id="be283-177">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="be283-177">Validation</span></span>

<dl>

[<span data-ttu-id="be283-178">ICE03</span><span class="sxs-lookup"><span data-stu-id="be283-178">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="be283-179">ICE04</span><span class="sxs-lookup"><span data-stu-id="be283-179">ICE04</span></span>](ice04.md)  
[<span data-ttu-id="be283-180">ICE06</span><span class="sxs-lookup"><span data-stu-id="be283-180">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="be283-181">ICE35</span><span class="sxs-lookup"><span data-stu-id="be283-181">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="be283-182">ICE58</span><span class="sxs-lookup"><span data-stu-id="be283-182">ICE58</span></span>](ice58.md)  
[<span data-ttu-id="be283-183">ICE71</span><span class="sxs-lookup"><span data-stu-id="be283-183">ICE71</span></span>](ice71.md)  
[<span data-ttu-id="be283-184">ICE81</span><span class="sxs-lookup"><span data-stu-id="be283-184">ICE81</span></span>](ice81.md)  
</dl>

 

 
