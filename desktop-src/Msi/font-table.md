---
description: Die Schriftart Tabelle enthält die Informationen zum Registrieren von Schriftart Dateien beim System.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Schriftart Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960055"
---
# <a name="font-table"></a><span data-ttu-id="20932-103">Schriftart Tabelle</span><span class="sxs-lookup"><span data-stu-id="20932-103">Font Table</span></span>

<span data-ttu-id="20932-104">Die Schriftart Tabelle enthält die Informationen zum Registrieren von Schriftart Dateien beim System.</span><span class="sxs-lookup"><span data-stu-id="20932-104">The Font table contains the information for registering font files with the system.</span></span>

<span data-ttu-id="20932-105">Die Schriftart Tabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="20932-105">The Font table has the following columns.</span></span>



| <span data-ttu-id="20932-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="20932-106">Column</span></span>    | <span data-ttu-id="20932-107">Typ</span><span class="sxs-lookup"><span data-stu-id="20932-107">Type</span></span>                         | <span data-ttu-id="20932-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="20932-108">Key</span></span> | <span data-ttu-id="20932-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="20932-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="20932-110">Datei\_</span><span class="sxs-lookup"><span data-stu-id="20932-110">File\_</span></span>    | [<span data-ttu-id="20932-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="20932-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="20932-112">J</span><span class="sxs-lookup"><span data-stu-id="20932-112">Y</span></span>   | <span data-ttu-id="20932-113">N</span><span class="sxs-lookup"><span data-stu-id="20932-113">N</span></span>        |
| <span data-ttu-id="20932-114">FontTitle</span><span class="sxs-lookup"><span data-stu-id="20932-114">FontTitle</span></span> | [<span data-ttu-id="20932-115">Text</span><span class="sxs-lookup"><span data-stu-id="20932-115">Text</span></span>](text.md)             | <span data-ttu-id="20932-116">N</span><span class="sxs-lookup"><span data-stu-id="20932-116">N</span></span>   | <span data-ttu-id="20932-117">J</span><span class="sxs-lookup"><span data-stu-id="20932-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="20932-118">Spalten</span><span class="sxs-lookup"><span data-stu-id="20932-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="20932-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_</span><span class="sxs-lookup"><span data-stu-id="20932-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="20932-120">Externer Schlüssel in den [Datei Tabellen](file-table.md) Eintrag für die Schriftart Datei.</span><span class="sxs-lookup"><span data-stu-id="20932-120">External key into the [File table](file-table.md) entry for the font file.</span></span> <span data-ttu-id="20932-121">Es wird empfohlen, dass für die Komponente mit der Schriftart Datei der Ordner "fontsfolder" in der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="20932-121">It is recommended that the component containing the font file have the FontsFolder specified in the Directory\_ column of the [Component table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="20932-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span><span class="sxs-lookup"><span data-stu-id="20932-122"><span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle</span></span>
</dt> <dd>

<span data-ttu-id="20932-123">Der Schriftart Name.</span><span class="sxs-lookup"><span data-stu-id="20932-123">Font name.</span></span> <span data-ttu-id="20932-124">Es wird empfohlen, dass Sie diese Spalte für TrueType-Schriftarten und TrueType-Auflistungen Null belassen, da das Installationsprogramm die Schriftart nach dem Lesen des richtigen Schriftart Titels aus der Schriftart Datei registrieren kann.</span><span class="sxs-lookup"><span data-stu-id="20932-124">It is recommended that you leave this column null for TrueType Fonts and TrueType Collections because the installer can register the font after reading the correct font title from the font file.</span></span> <span data-ttu-id="20932-125">Wenn der Schriftart Name eingegeben wird, muss er mit dem Schriftart Titel aus der Schriftart Datei identisch sein.</span><span class="sxs-lookup"><span data-stu-id="20932-125">If the font name is entered, it must be identical to font title from the font file.</span></span> <span data-ttu-id="20932-126">Sie müssen einen Titel für Schriftarten angeben, die keine eingebetteten Namen haben, z. b.. FON-Dateien.</span><span class="sxs-lookup"><span data-stu-id="20932-126">You must specify a title for fonts that do not have embedded names, such as .fon files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20932-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20932-127">Remarks</span></span>

<span data-ttu-id="20932-128">Diese Tabelle wird beim Ausführen der [RegisterFonts-Aktion](registerfonts-action.md) oder der [unregisterfonts-Aktion](unregisterfonts-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="20932-128">This table is referred to when the [RegisterFonts action](registerfonts-action.md) or the [UnregisterFonts action](unregisterfonts-action.md) is executed.</span></span>

<span data-ttu-id="20932-129">Wenn das FontTitle-Feld den Wert NULL hat, wird der Schriftart Name direkt aus der angegebenen Schriftart Datei gelesen.</span><span class="sxs-lookup"><span data-stu-id="20932-129">If the FontTitle field is left Null, the Font name is read directly from the font file specified.</span></span> <span data-ttu-id="20932-130">Wenn sich der in das FontTitle-Feld aufgezeichnete Schriftart Name von dem internen Schriftart Namen unterscheidet, der in der Schriftart Datei aufgezeichnet wurde, wird die Schriftart zweimal von der [RegisterFonts-Aktion](registerfonts-action.md)registriert.</span><span class="sxs-lookup"><span data-stu-id="20932-130">If the font name recorded into the FontTitle field differs from the internal font name recorded in the font file, the font is registered twice by the [RegisterFonts action](registerfonts-action.md).</span></span>

<span data-ttu-id="20932-131">Schriftart Dateien sollten nicht mit einer Sprach-ID erstellt werden, da die Schriftarten nicht über eine eingebettete Sprachen-ID-Ressource verfügen. Daher sollte die sprach Spalte der [Dateitabelle](file-table.md) für Schriftart Dateien Null belassen.</span><span class="sxs-lookup"><span data-stu-id="20932-131">Font files should not be authored with a language ID, as fonts do not have an embedded language ID resource.Thus the Language column of the [File table](file-table.md) should be left null for font files.</span></span>

<span data-ttu-id="20932-132">Da das Installationsprogramm Schriftart Dateien nicht standardmäßig neu anzählt, können bereits vorhandene Schriftart Dateien beim Deinstallieren einer Anwendung mit Ihrer Komponente entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="20932-132">Because the installer does not refcount font files by default, preexisting font files may be removed with their component when uninstalling an application.</span></span> <span data-ttu-id="20932-133">Um sicherzustellen, dass eine Schriftart Datei nicht entfernt wird, können Autoren die **msidbcomponentattributesshareddllrefcount** -oder **msidbcomponentattributestribute** -Bitflags \_ \_ \_ für die Komponente, die die Schriftart Datei enthält, in der Spalte Attribute der MSI-Komponenten Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="20932-133">To ensure that a font file is not removed, authors may set the **msidbComponentAttributesSharedDllRefCount** or **msidbComponentAttributesPermanent** bit flags in the Attributes column of the Component Table\_msi\_Component\_Table for the component containing the font file.</span></span>

## <a name="validation"></a><span data-ttu-id="20932-134">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="20932-134">Validation</span></span>

<dl>

[<span data-ttu-id="20932-135">ICE03</span><span class="sxs-lookup"><span data-stu-id="20932-135">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="20932-136">ICE06</span><span class="sxs-lookup"><span data-stu-id="20932-136">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="20932-137">ICE07</span><span class="sxs-lookup"><span data-stu-id="20932-137">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="20932-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="20932-138">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="20932-139">ICE51</span><span class="sxs-lookup"><span data-stu-id="20932-139">ICE51</span></span>](ice51.md)  
[<span data-ttu-id="20932-140">ICE60</span><span class="sxs-lookup"><span data-stu-id="20932-140">ICE60</span></span>](ice60.md)  
</dl>

 

 



