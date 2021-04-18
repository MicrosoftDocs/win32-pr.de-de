---
description: Beschreibt feste Links und Verbindungen.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Feste Links und Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352532"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="e6e33-103">Feste Links und Verbindungen</span><span class="sxs-lookup"><span data-stu-id="e6e33-103">Hard Links and Junctions</span></span>

<span data-ttu-id="e6e33-104">Es gibt drei Typen von Datei Verknüpfungen, die im NTFS-Dateisystem unterstützt werden: feste Links, Verbindungen und symbolische Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="e6e33-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="e6e33-105">Dieses Thema stellt eine Übersicht über feste Links und Verbindungen dar.</span><span class="sxs-lookup"><span data-stu-id="e6e33-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="e6e33-106">Informationen zu symbolischen Verknüpfungen finden Sie unter [Erstellen von symbolischen Verknüpfungen](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="e6e33-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="e6e33-107">Feste Links</span><span class="sxs-lookup"><span data-stu-id="e6e33-107">Hard Links</span></span>

<span data-ttu-id="e6e33-108">Ein fester *Link* ist die Dateisystem Darstellung einer Datei, durch die mehr als ein Pfad auf eine einzelne Datei auf demselben Volume verweist.</span><span class="sxs-lookup"><span data-stu-id="e6e33-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="e6e33-109">Um einen festen Link zu erstellen, verwenden Sie die Funktion " [**kreatehardlink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) ".</span><span class="sxs-lookup"><span data-stu-id="e6e33-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="e6e33-110">Alle Änderungen an dieser Datei sind für Anwendungen, die über die darauf referendeten Hardlinks darauf zugreifen, sofort sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e6e33-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="e6e33-111">Die Verzeichniseintrags Größe und die Attributinformationen werden jedoch nur für den Link aktualisiert, über den die Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="e6e33-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="e6e33-112">Beachten Sie, dass sich die Attribute für die Datei in jedem festen Link zu dieser Datei widerspiegeln, und dass Änderungen an den Attributen dieser Datei an alle festen Links weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e6e33-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="e6e33-113">Wenn Sie z. b. das Attribut "schreibgeschützt" auf einem festen Link zurücksetzen, um diesen bestimmten festen Link zu löschen, und mehrere feste Links zur eigentlichen Datei vorhanden sind, müssen Sie das schreibgeschützte Bit in der Datei von einem der restlichen festen Links zurücksetzen, um die Datei und alle restlichen festen Links wieder in den schreibgeschützten Zustand zu bringen.</span><span class="sxs-lookup"><span data-stu-id="e6e33-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="e6e33-114">In einem System, in dem Z. b. "C:" und "D:" lokale Laufwerke sind und Z: ein Netzlaufwerk ist, \\ \\ das Fred-Freigabe zugeordnet ist \\ , sind die folgenden Verweise als hardlink zulässig:</span><span class="sxs-lookup"><span data-stu-id="e6e33-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="e6e33-115">C: \\ dira \\ethel.txt mit C: \\ dirb \\ Dirc verknüpft \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="e6e33-116">D: \\ dir1 \\tinker.txt to d: \\ dir2 \\ DirX \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="e6e33-117">C: \\ DirY \\ Bob. bak, verknüpft mit C: \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="e6e33-118">Folgendes ist nicht:</span><span class="sxs-lookup"><span data-stu-id="e6e33-118">The following are not:</span></span>

-   <span data-ttu-id="e6e33-119">C: \\ dira mit c: \\ dirb verknüpft</span><span class="sxs-lookup"><span data-stu-id="e6e33-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="e6e33-120">C: \\ dira \\ethel.txt mit D: \\ dirb verknüpft \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="e6e33-121">C: \\ dira \\ethel.txt mit Z: \\ dirb verknüpft \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="e6e33-122">Verwenden Sie die [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) -Funktion, um einen festen Link zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e6e33-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="e6e33-123">Sie können feste Verknüpfungen unabhängig von der Reihenfolge, in der Sie erstellt werden, in beliebiger Reihenfolge löschen.</span><span class="sxs-lookup"><span data-stu-id="e6e33-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="e6e33-124">Verbindungen</span><span class="sxs-lookup"><span data-stu-id="e6e33-124">Junctions</span></span>

<span data-ttu-id="e6e33-125">Eine *Verknüpfung (auch* als *Weiche Verknüpfung* bezeichnet) unterscheidet sich von einer festen Verknüpfung darin, dass es sich bei den Speicher Objekten, auf die verwiesen wird, um separate Verzeichnisse handelt, und eine Verknüpfung kann Verzeichnisse verknüpfen, die sich auf verschiedenen lokalen Volumes auf demselben Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="e6e33-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="e6e33-126">Andernfalls funktionieren die Verbindungen mit festen Links identisch.</span><span class="sxs-lookup"><span data-stu-id="e6e33-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="e6e33-127">Verbindungen werden über Analyse [Punkte](reparse-points.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="e6e33-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="e6e33-128">Wenn Sie die gleichen Bedingungen im Abschnitt feste Links annehmen, sind die folgenden Verweise als Verbindungen zulässig:</span><span class="sxs-lookup"><span data-stu-id="e6e33-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="e6e33-129">C: \\ dira mit c: \\ dirb \\ Dirc verknüpft</span><span class="sxs-lookup"><span data-stu-id="e6e33-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="e6e33-130">C: \\ DirX verknüpft mit D: \\ DirY</span><span class="sxs-lookup"><span data-stu-id="e6e33-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="e6e33-131">Folgendes ist nicht:</span><span class="sxs-lookup"><span data-stu-id="e6e33-131">The following are not:</span></span>

-   <span data-ttu-id="e6e33-132">C: \\ dira \\one.txt mit C: \\ dirb verknüpft \\two.txt</span><span class="sxs-lookup"><span data-stu-id="e6e33-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="e6e33-133">C: \\ dir1 verknüpft mit Z: \\ dir2</span><span class="sxs-lookup"><span data-stu-id="e6e33-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6e33-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6e33-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6e33-135">Erstellen von symbolischen Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="e6e33-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



