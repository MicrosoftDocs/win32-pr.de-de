---
description: Diese Tabelle enthält die Symbol Dateien. Jedes Symbol aus der Tabelle wird als Teil der Produktankündigung in eine Datei kopiert, die für angekündigte Verknüpfungen und OLE-Server verwendet werden soll. Siehe OLE-Einschränkungen für Datenströme.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Symboltabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215701"
---
# <a name="icon-table"></a><span data-ttu-id="e45d6-105">Symboltabelle</span><span class="sxs-lookup"><span data-stu-id="e45d6-105">Icon Table</span></span>

<span data-ttu-id="e45d6-106">Diese Tabelle enthält die Symbol Dateien.</span><span class="sxs-lookup"><span data-stu-id="e45d6-106">This table contains the icon files.</span></span> <span data-ttu-id="e45d6-107">Jedes Symbol aus der Tabelle wird als Teil der Produktankündigung in eine Datei kopiert, die für angekündigte Verknüpfungen und OLE-Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e45d6-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="e45d6-108">Siehe [OLE-Einschränkungen für Datenströme](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e45d6-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="e45d6-109">Die Symboltabelle enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="e45d6-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="e45d6-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="e45d6-110">Column</span></span> | <span data-ttu-id="e45d6-111">Typ</span><span class="sxs-lookup"><span data-stu-id="e45d6-111">Type</span></span>                         | <span data-ttu-id="e45d6-112">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e45d6-112">Key</span></span> | <span data-ttu-id="e45d6-113">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="e45d6-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="e45d6-114">Name</span><span class="sxs-lookup"><span data-stu-id="e45d6-114">Name</span></span>   | [<span data-ttu-id="e45d6-115">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e45d6-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="e45d6-116">J</span><span class="sxs-lookup"><span data-stu-id="e45d6-116">Y</span></span>   | <span data-ttu-id="e45d6-117">N</span><span class="sxs-lookup"><span data-stu-id="e45d6-117">N</span></span>        |
| <span data-ttu-id="e45d6-118">Daten</span><span class="sxs-lookup"><span data-stu-id="e45d6-118">Data</span></span>   | [<span data-ttu-id="e45d6-119">Binär (Binary)</span><span class="sxs-lookup"><span data-stu-id="e45d6-119">Binary</span></span>](binary.md)         | <span data-ttu-id="e45d6-120">N</span><span class="sxs-lookup"><span data-stu-id="e45d6-120">N</span></span>   | <span data-ttu-id="e45d6-121">N</span><span class="sxs-lookup"><span data-stu-id="e45d6-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e45d6-122">Spalten</span><span class="sxs-lookup"><span data-stu-id="e45d6-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e45d6-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen</span><span class="sxs-lookup"><span data-stu-id="e45d6-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="e45d6-124">Der Name der Symbol Datei.</span><span class="sxs-lookup"><span data-stu-id="e45d6-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="e45d6-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Vorrats</span><span class="sxs-lookup"><span data-stu-id="e45d6-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="e45d6-126">Die Binär Symbol Daten im PE-Format (dll-oder exe-Datei) oder im Symbol Format (. ico).</span><span class="sxs-lookup"><span data-stu-id="e45d6-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e45d6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e45d6-127">Remarks</span></span>

<span data-ttu-id="e45d6-128">Diese Tabelle wird beim Ausführen der [publishproduct-Aktion](publishproduct-action.md) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e45d6-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="e45d6-129">Die Symbole für Verknüpfungen, Dateinamen Erweiterungen und CLSIDs müssen in Dateien gespeichert werden, die von der Zieldatei selbst getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e45d6-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="e45d6-130">Dies ist erforderlich, da das Installationsprogramm nur die kleinen Symbol Dateien auf den Computer des Benutzers kopieren soll, wenn die Ressource angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="e45d6-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="e45d6-131">Ein Entwickler eines Installationspakets muss daher separate Dateien erstellen, die nur die Symbole enthalten.</span><span class="sxs-lookup"><span data-stu-id="e45d6-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="e45d6-132">Diese Symbol Dateien werden dann als Binärdaten in der Symboltabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e45d6-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="e45d6-133">Symbol Dateien, die ausschließlich Dateinamen Erweiterungen oder CLSIDs zugeordnet sind, können eine beliebige Erweiterung haben, z. b. ico.</span><span class="sxs-lookup"><span data-stu-id="e45d6-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="e45d6-134">Symbol Dateien, die Verknüpfungen zugeordnet sind, müssen sich jedoch im Binärformat der exe-Datei befinden und müssen so benannt werden, dass Ihre Erweiterung mit der Erweiterung des Ziels übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e45d6-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="e45d6-135">Die Verknüpfung funktioniert nicht, wenn diese Regel nicht befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="e45d6-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="e45d6-136">Wenn eine Verknüpfung z. b. auf eine Ressource mit der Schlüsseldatei Red.Bar zeigen soll, muss die Symbol Datei auch die Erweiterung. Bar aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e45d6-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="e45d6-137">Mehrere Symbole können in dieselbe Symbol Datei gefüllt werden, solange alle Zieldateien dieselbe Erweiterung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e45d6-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="e45d6-138">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="e45d6-138">Validation</span></span>

<dl>

[<span data-ttu-id="e45d6-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="e45d6-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e45d6-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="e45d6-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="e45d6-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="e45d6-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="e45d6-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="e45d6-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="e45d6-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="e45d6-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="e45d6-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="e45d6-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



