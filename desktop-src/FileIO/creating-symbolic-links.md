---
description: Erstellen Sie symbolische Verknüpfungen, die einen absoluten oder relativen Pfad verwenden, indem Sie die Funktion "kreatesymboliclink" verwenden.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Erstellen von symbolischen Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347829"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="6a229-103">Erstellen von symbolischen Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="6a229-103">Creating Symbolic Links</span></span>

<span data-ttu-id="6a229-104">Die Funktion " [**kreatesymboliclink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) " ermöglicht es Ihnen, symbolische Verknüpfungen mit einem absoluten oder relativen Pfad zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a229-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="6a229-105">Symbolische Verknüpfungen können entweder absolute oder relative Links sein.</span><span class="sxs-lookup"><span data-stu-id="6a229-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="6a229-106">Absolute Links sind Links, die jeden Teil des Pfadnamens angeben. relative Verknüpfungen werden relativ zu bestimmt, wo sich relative –-linkspezifier in einem angegebenen Pfad befinden.</span><span class="sxs-lookup"><span data-stu-id="6a229-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="6a229-107">Relative Links werden mithilfe der folgenden Konventionen angegeben:</span><span class="sxs-lookup"><span data-stu-id="6a229-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="6a229-108">Punkt (.</span><span class="sxs-lookup"><span data-stu-id="6a229-108">Dot (.</span></span> <span data-ttu-id="6a229-109">und..) Konventionen – z. b. ".. \\ " löst den Pfad relativ zum übergeordneten Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="6a229-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="6a229-110">Namen ohne Schrägstriche ( \) – z. b. "tmp" löst den Pfad relativ zum aktuellen Verzeichnis auf.</span><span class="sxs-lookup"><span data-stu-id="6a229-110">Names with no slashes (\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="6a229-111">Root relative – beispielsweise wird " \\ Windows \\ system32" in das *aktuelle Laufwerk*: \\ Windows System32 aufgelöst \\ .</span><span class="sxs-lookup"><span data-stu-id="6a229-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="6a229-112">directory</span><span class="sxs-lookup"><span data-stu-id="6a229-112">directory</span></span>
-   <span data-ttu-id="6a229-113">Aktuelles Arbeitsverzeichnis-relativ – wenn das aktuelle Arbeitsverzeichnis z. b. "c: \\ Windows \\ system32" ist, wird "C:File.txt" in "c: \\ Windows \\ system32 \\File.txt" aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="6a229-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="6a229-114">**Hinweis**  Wenn Sie ein Aktuelles Arbeitsverzeichnis angeben – relative Verknüpfung, wird es als absoluter Link erstellt, weil das aktuelle Arbeitsverzeichnis basierend auf dem Benutzer und dem Thread verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6a229-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="6a229-115">Eine symbolische Verknüpfung kann auch sowohl Verknüpfungs Punkte als auch eingebundene Ordner als Teil des Pfadnamens enthalten.</span><span class="sxs-lookup"><span data-stu-id="6a229-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="6a229-116">Symbolische Verknüpfungen können mithilfe des UNC-Pfads direkt auf eine Remote Datei oder ein Remote Verzeichnis verweisen.</span><span class="sxs-lookup"><span data-stu-id="6a229-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="6a229-117">Relative symbolische Verknüpfungen sind auf ein einzelnes Volume beschränkt.</span><span class="sxs-lookup"><span data-stu-id="6a229-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="6a229-118">Beispiel für einen absoluten symbolischen Link</span><span class="sxs-lookup"><span data-stu-id="6a229-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="6a229-119">In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", bei der es sich um einen absoluten symbolischen Link handelt.</span><span class="sxs-lookup"><span data-stu-id="6a229-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="6a229-120">Wenn '*x*' gefunden wird, wird das Fragment des ursprünglichen Pfads bis zu und einschließlich '*x*' vollständig durch den Pfad ersetzt, auf den von '*x*' verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6a229-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="6a229-121">Der restliche Pfad nach "*x*" wird an diesen neuen Pfad angehängt.</span><span class="sxs-lookup"><span data-stu-id="6a229-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="6a229-122">Dies wird jetzt zum geänderten Pfad.</span><span class="sxs-lookup"><span data-stu-id="6a229-122">This now becomes the modified path.</span></span>

<span data-ttu-id="6a229-123">X: "C: \\ alpha \\ Beta \\ abslink \\ Gamma \\ Datei"</span><span class="sxs-lookup"><span data-stu-id="6a229-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="6a229-124">Link: "abslink" ist " \\ \\ machineB \\ share" zugeordnet</span><span class="sxs-lookup"><span data-stu-id="6a229-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="6a229-125">Geänderter Pfad: " \\ \\ machineB \\ share \\ Gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="6a229-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="6a229-126">Beispiel für relative symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="6a229-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="6a229-127">In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", bei der es sich um einen relativen symbolischen Link handelt.</span><span class="sxs-lookup"><span data-stu-id="6a229-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="6a229-128">Wenn "*x*" gefunden wird, wird "*x*" vollständig durch das neue Fragment ersetzt, auf das von "*x*" gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a229-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="6a229-129">Der restliche Pfad nach "*x*" wird an den neuen Pfad angehängt.</span><span class="sxs-lookup"><span data-stu-id="6a229-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="6a229-130">Beliebige Punkte (..) in diesem neuen Pfad ersetzen Komponenten, die vor den Punkten (..) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6a229-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="6a229-131">Jede Gruppe von Punkten ersetzt die vorangehende Komponente.</span><span class="sxs-lookup"><span data-stu-id="6a229-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="6a229-132">Wenn die Anzahl der Punkte (..) die Anzahl der Komponenten überschreitet, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a229-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="6a229-133">Wenn alle Komponenten Ersetzung abgeschlossen ist, bleibt der abschließende, geänderte Pfad.</span><span class="sxs-lookup"><span data-stu-id="6a229-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="6a229-134">X: C: \\ alpha- \\ Beta \\ Link- \\ Gamma \\ Datei</span><span class="sxs-lookup"><span data-stu-id="6a229-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="6a229-135">Link: "Link" ist zugeordnet zu "... \\ . \\ Theta</span><span class="sxs-lookup"><span data-stu-id="6a229-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="6a229-136">Modifizierter Pfad: "C: \\ alpha \\ Beta \\ .. \\ . \\ Datei- \\ Gamma \\ Datei "</span><span class="sxs-lookup"><span data-stu-id="6a229-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="6a229-137">Abschließender Pfad: "C: die \\ \\ \\ Datei Gamma Datei"</span><span class="sxs-lookup"><span data-stu-id="6a229-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a229-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a229-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a229-139">Symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="6a229-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="6a229-140">Feste Links und Verbindungen</span><span class="sxs-lookup"><span data-stu-id="6a229-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="6a229-141">Benennen von Dateien, Pfaden und Namespaces</span><span class="sxs-lookup"><span data-stu-id="6a229-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



