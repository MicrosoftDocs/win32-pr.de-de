---
description: Mit der Aktion "InstallFiles" werden die in der Dateitabelle angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis kopiert.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: InstallFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348839"
---
# <a name="installfiles-action"></a><span data-ttu-id="e5852-103">InstallFiles-Aktion</span><span class="sxs-lookup"><span data-stu-id="e5852-103">InstallFiles Action</span></span>

<span data-ttu-id="e5852-104">Mit der Aktion "InstallFiles" werden die in der Dateitabelle angegebenen Dateien aus dem Quellverzeichnis in das Zielverzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="e5852-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e5852-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e5852-105">Sequence Restrictions</span></span>

<span data-ttu-id="e5852-106">Die InstallFiles-Aktion muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor allen Datei abhängigen Aktionen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e5852-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e5852-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="e5852-107">ActionData Messages</span></span>



| <span data-ttu-id="e5852-108">Feld</span><span class="sxs-lookup"><span data-stu-id="e5852-108">Field</span></span> | <span data-ttu-id="e5852-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="e5852-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="e5852-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e5852-110">\[1\]</span></span> | <span data-ttu-id="e5852-111">Der Bezeichner der installierten Datei.</span><span class="sxs-lookup"><span data-stu-id="e5852-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="e5852-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="e5852-112">\[6\]</span></span> | <span data-ttu-id="e5852-113">Größe der installierten Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e5852-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="e5852-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="e5852-114">\[9\]</span></span> | <span data-ttu-id="e5852-115">Der Bezeichner des Verzeichnisses, das die installierte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="e5852-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e5852-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5852-116">Remarks</span></span>

<span data-ttu-id="e5852-117">Die InstallFiles-Aktion wird für Dateien ausgeführt, die in der [Dateitabelle](file-table.md)angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e5852-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="e5852-118">Jede Datei wird auf Grundlage des Installationsstatus der zugeordneten Komponente der Datei in der [Komponenten Tabelle](component-table.md)installiert.</span><span class="sxs-lookup"><span data-stu-id="e5852-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="e5852-119">Nur die Dateien, deren Komponenten in den Zustand **msiinstallstatelocal** aufgelöst werden, sind zum Kopieren berechtigt.</span><span class="sxs-lookup"><span data-stu-id="e5852-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="e5852-120">Die Aktion "InstallFiles" implementiert die folgenden Spalten der Dateitabelle.</span><span class="sxs-lookup"><span data-stu-id="e5852-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="e5852-121">Die FileName-Spalte gibt den Ziel Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="e5852-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="e5852-122">In der Spalte Version ist die Dateiversion angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5852-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="e5852-123">In der Spalte Attribute werden die Bits des Datei-und Installations Attributs angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5852-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="e5852-124">Die Datei Spalte gibt das eindeutige Datei Token an.</span><span class="sxs-lookup"><span data-stu-id="e5852-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="e5852-125">In der Filesize-Spalte wird die nicht komprimierte Dateigröße in Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5852-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="e5852-126">In der Spalte Sprache wird der Bezeichner der Datei Sprache angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5852-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="e5852-127">Die Sequenz Spalte gibt die Sequenznummer auf dem Medium an.</span><span class="sxs-lookup"><span data-stu-id="e5852-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="e5852-128">Die Aktion InstallFiles implementiert die folgenden Spalten der Component-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e5852-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="e5852-129">Die \_ Spalte Verzeichnis gibt einen Verweis auf ein [Verzeichnis Tabellen](directory-table.md) Element an.</span><span class="sxs-lookup"><span data-stu-id="e5852-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="e5852-130">Die Spalte Komponente gibt einen eindeutigen Namen für das Komponenten Element an.</span><span class="sxs-lookup"><span data-stu-id="e5852-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="e5852-131">Die angegebene Datei wird nur kopiert, wenn einer der folgenden Punkte zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e5852-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="e5852-132">Die Datei ist zurzeit nicht auf dem lokalen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="e5852-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="e5852-133">Die Datei befindet sich auf dem lokalen Computer, hat jedoch eine niedrigere Versionsnummer als die Datei in der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5852-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="e5852-134">Die Datei befindet sich auf dem lokalen Computer, aber es ist keine zugehörige Versionsnummer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e5852-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="e5852-135">Das Quellverzeichnis für jede zu kopierende Datei wird vom sourcemode bestimmt, das wiederum von dem Wert in der CAB-Spalte der Medien Tabelle abhängt.</span><span class="sxs-lookup"><span data-stu-id="e5852-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="e5852-136">Eine vollständige Erläuterung des Quell Modus finden Sie in der [Media-Tabelle](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5852-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="e5852-137">Wenn sich das Quellverzeichnis für eine zu kopierende Datei auf einem Wechsel Datenträger (z. b. eine Diskette oder CD-ROM) befindet, wird durch die InstallFiles-Aktion überprüft, ob die richtigen Quell Medien eingefügt werden, bevor versucht wird, die Datei zu kopieren</span><span class="sxs-lookup"><span data-stu-id="e5852-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="e5852-138">InstallFiles sucht nach Medien desselben Wechsel Datentyps mit einer [*Volumebezeichnung*](v-gly.md) , die mit dem in der Spalte VolumeLabel der Medien Tabelle angegebenen Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e5852-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="e5852-139">Wenn ein entsprechendes bereitgestelltes Volume gefunden wird, wird der Datei Kopiervorgang fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e5852-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="e5852-140">Wenn keine Entsprechung gefunden wird, fordert ein Dialogfeld an, dass der Benutzer die richtigen Medien einfügt.</span><span class="sxs-lookup"><span data-stu-id="e5852-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="e5852-141">In diesem Fall wird im Dialogfeld der Medien Name verwendet, der in der Spalte diskprompt der Medien Tabelle als Teil der Eingabeaufforderung gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="e5852-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="e5852-142">Vorsicht muss ausgeführt werden, da die InstallFiles-Aktion eine ursprüngliche Datei löschen und nicht ersetzen kann.</span><span class="sxs-lookup"><span data-stu-id="e5852-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="e5852-143">Dies tritt auf, wenn bei der InstallFiles-Aktion ein Fehler auftritt, während eine ältere Datei ersetzt wird und der Benutzer die Fehlermeldung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e5852-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="e5852-144">Das Standardverhalten des Installers besteht darin, eine alte Datei zu löschen, bevor sichergestellt wird, dass die neue Datei ordnungsgemäß kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5852-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="e5852-145">Informationen zu den vom Installer verwendeten Regeln für die Datei Versionsverwaltung finden Sie unter Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="e5852-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



