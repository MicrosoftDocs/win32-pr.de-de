---
description: Erstellen Sie symbolische Verknüpfungen, die entweder einen absoluten oder relativen Pfad verwenden, indem Sie die CreateSymbolicLink-Funktion verwenden.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Erstellen symbolischer Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387706"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="f31be-103">Erstellen symbolischer Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f31be-103">Creating Symbolic Links</span></span>

<span data-ttu-id="f31be-104">Mit der [**Funktion CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) können Sie symbolische Verknüpfungen mit einem absoluten oder relativen Pfad erstellen.</span><span class="sxs-lookup"><span data-stu-id="f31be-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="f31be-105">Symbolische Verknüpfungen können entweder absolute oder relative Links sein.</span><span class="sxs-lookup"><span data-stu-id="f31be-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="f31be-106">Absolute Links sind Links, die jeden Teil des Pfadnamens angeben. Relative Links werden relativ dazu bestimmt, wo sich relative-link-Spezifizierer in einem angegebenen Pfad befinden.</span><span class="sxs-lookup"><span data-stu-id="f31be-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="f31be-107">Relative Links werden mit den folgenden Konventionen angegeben:</span><span class="sxs-lookup"><span data-stu-id="f31be-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="f31be-108">Punkt (.</span><span class="sxs-lookup"><span data-stu-id="f31be-108">Dot (.</span></span> <span data-ttu-id="f31be-109">und ..) -Konventionen, z. B. ".. \\ " löst den Pfad relativ zum übergeordneten Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="f31be-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="f31be-110">Namen ohne Schrägstriche ( \\ ), z.B. "tmp" löst den Pfad relativ zum aktuellen Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="f31be-110">Names with no slashes (\\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="f31be-111">Root relative, z.B. " \\ Windows \\ System32" wird in das *"aktuelle Laufwerk*: \\ Windows \\ System32" aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f31be-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="f31be-112">directory</span><span class="sxs-lookup"><span data-stu-id="f31be-112">directory</span></span>
-   <span data-ttu-id="f31be-113">Aktuelles Arbeitsverzeichnis relativ: Wenn das aktuelle Arbeitsverzeichnis z. B. "C: \\ Windows \\ System32" lautet, wird "C:File.txt" in "C: \\ Windows \\ System32 \\File.txt" aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f31be-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="f31be-114">**Hinweis**  Wenn Sie einen aktuellen Link vom Typ Arbeitsverzeichnis –relativ angeben, wird er aufgrund der Verarbeitung des aktuellen Arbeitsverzeichnisses basierend auf dem Benutzer und dem Thread als absoluter Link erstellt.</span><span class="sxs-lookup"><span data-stu-id="f31be-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="f31be-115">Eine symbolische Verknüpfung kann auch Verbindungspunkte und bereitgestellte Ordner als Teil des Pfadnamens enthalten.</span><span class="sxs-lookup"><span data-stu-id="f31be-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="f31be-116">Symbolische Verknüpfungen können mithilfe des UNC-Pfads direkt auf eine Remotedatei oder ein Remoteverzeichnis verweisen.</span><span class="sxs-lookup"><span data-stu-id="f31be-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="f31be-117">Relative symbolische Verknüpfungen sind auf ein einzelnes Volume beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f31be-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="f31be-118">Beispiel für einen absoluten symbolischen Link</span><span class="sxs-lookup"><span data-stu-id="f31be-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="f31be-119">In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", die eine absolute symbolische Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="f31be-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="f31be-120">Wenn *"x"* gefunden wird, wird das Fragment des ursprünglichen Pfads bis einschließlich *"x"* vollständig durch den Pfad ersetzt, auf den *"x"* zeigt.</span><span class="sxs-lookup"><span data-stu-id="f31be-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="f31be-121">Der Rest des Pfads nach "*x*" wird an diesen neuen Pfad angefügt.</span><span class="sxs-lookup"><span data-stu-id="f31be-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="f31be-122">Dies wird nun zum geänderten Pfad.</span><span class="sxs-lookup"><span data-stu-id="f31be-122">This now becomes the modified path.</span></span>

<span data-ttu-id="f31be-123">X: "C: \\ alpha \\ beta \\ absLink gamma \\ \\ file"</span><span class="sxs-lookup"><span data-stu-id="f31be-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="f31be-124">Link: "absLink" wird \\ \\ "machineB \\ share" zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f31be-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="f31be-125">Geänderter Pfad: \\ \\ "machineB \\ share \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="f31be-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="f31be-126">Beispiel für relative symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f31be-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="f31be-127">In diesem Beispiel enthält der ursprüngliche Pfad eine Komponente "*x*", die eine relative symbolische Verknüpfung ist.</span><span class="sxs-lookup"><span data-stu-id="f31be-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="f31be-128">Wenn '*x*' gefunden wird, wird '*x*' vollständig durch das neue Fragment ersetzt, auf das von '*x*' gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f31be-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="f31be-129">Der Rest des Pfads nach '*x*' wird an den neuen Pfad angefügt.</span><span class="sxs-lookup"><span data-stu-id="f31be-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="f31be-130">Alle Punkte (..) in diesem neuen Pfad ersetzen Komponenten, die vor den Punkten (..) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f31be-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="f31be-131">Jeder Satz von Punkten ersetzt die vorangehende Komponente.</span><span class="sxs-lookup"><span data-stu-id="f31be-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="f31be-132">Wenn die Anzahl der Punkte (..) die Anzahl der Komponenten überschreitet, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f31be-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="f31be-133">Andernfalls verbleibt der letzte geänderte Pfad, wenn der Austausch aller Komponenten abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f31be-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="f31be-134">X: C: \\ Alpha beta link gamma \\ \\ \\ \\ file</span><span class="sxs-lookup"><span data-stu-id="f31be-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="f31be-135">Link: "link" entspricht ".. \\ .. \\ theta"</span><span class="sxs-lookup"><span data-stu-id="f31be-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="f31be-136">Geänderter Pfad: "C: \\ alpha \\ beta \\ .. \\ .. \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="f31be-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="f31be-137">Endgültiger Pfad: "C: \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="f31be-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="f31be-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f31be-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f31be-139">Symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f31be-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="f31be-140">Hard Links and Junctions</span><span class="sxs-lookup"><span data-stu-id="f31be-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="f31be-141">Benennen von Dateien, Pfaden und Namespaces</span><span class="sxs-lookup"><span data-stu-id="f31be-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



