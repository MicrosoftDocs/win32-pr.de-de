---
title: 'Download-Manager: Übersicht'
description: 'Download-Manager: Übersicht'
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Echt Zeit Downloads
- Online Stores, Echt Zeit Downloads
- Typ 2 Online Stores, Echt Zeit Download
- Windows Media Player Online Stores, herunterladen im Hintergrund
- Online Stores, herunterladen im Hintergrund
- Typ 2 Online Stores, herunterladen im Hintergrund
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Herunterladen in Echtzeit
- Herunterladen im Hintergrund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037507"
---
# <a name="download-manager-overview"></a><span data-ttu-id="d6f7c-117">Download-Manager: Übersicht</span><span class="sxs-lookup"><span data-stu-id="d6f7c-117">Download Manager Overview</span></span>

<span data-ttu-id="d6f7c-118">Microsoft Windows Media Player bietet Aufgabenbereiche im Online Store, die ein gehostetes Browserfenster enthalten.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-118">Microsoft Windows Media Player provides online store task panes that contain a hosted browser window.</span></span> <span data-ttu-id="d6f7c-119">Über die Online Stores können Benutzer über das Internet mit Webseiten im Online Store interagieren.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-119">Through the online stores, users can interact with online store webpages across the Internet.</span></span>

<span data-ttu-id="d6f7c-120">Der Windows Media Player Download-Manager stellt ein Objektmodell bereit, das Sie verwenden können, um die Aufgaben für das Herunterladen von Inhalten auf dem Computer des Benutzers von Microsoft Internetinformationsdienste (IIS) mithilfe von Hypertext Transfer Protocol (http) zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-120">The Windows Media Player Download Manager provides an object model that you can use to handle the tasks associated with downloading content to the user's computer from Microsoft Internet Information Services (IIS) using Hypertext Transfer Protocol (HTTP).</span></span> <span data-ttu-id="d6f7c-121">Mit dem Download-Manager können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="d6f7c-121">With the Download Manager, you can:</span></span>

-   <span data-ttu-id="d6f7c-122">Gleichzeitiges Verwalten mehrerer Downloads als Sammlung</span><span class="sxs-lookup"><span data-stu-id="d6f7c-122">Manage multiple downloads simultaneously as a collection.</span></span>
-   <span data-ttu-id="d6f7c-123">Geben Sie eine URL für eine Datei an, und starten Sie Sie mit http.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-123">Specify a URL for a file and start it downloading using HTTP.</span></span>
-   <span data-ttu-id="d6f7c-124">Fragen Sie den Download Status und den Fortschritt ab.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-124">Query for the download state and progress.</span></span>
-   <span data-ttu-id="d6f7c-125">Anhalten, fortsetzen oder Abbrechen eines Downloads.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-125">Pause, resume, or cancel a download.</span></span>
-   <span data-ttu-id="d6f7c-126">Geben Sie an, ob ein Download im Hintergrund oder in Echtzeit stattfinden soll.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-126">Specify whether a download occurs in the background or in real time.</span></span> <span data-ttu-id="d6f7c-127">(Das Herunterladen im Hintergrund ist nur unter dem Betriebssystem Microsoft Windows XP verfügbar.) Weitere Informationen finden Sie unter [Informationen zu Hintergrund und Echt Zeit Downloads](#about-background-and-real-time-downloading).</span><span class="sxs-lookup"><span data-stu-id="d6f7c-127">(Background downloading is only available on the Microsoft Windows XP operating system.) See [About Background and Real-time Downloading](#about-background-and-real-time-downloading).</span></span>
-   <span data-ttu-id="d6f7c-128">Geben Sie an, wie Inhalt in der Bibliothek angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-128">Specify how content is displayed in the library.</span></span> <span data-ttu-id="d6f7c-129">[Informationen zur Bibliotheks Integration](#about-library-integration)finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-129">See [About Library Integration](#about-library-integration).</span></span>

<span data-ttu-id="d6f7c-130">Der Download-Manager ist die Lösung für das Herunterladen von Inhalten aus Skriptcode in gehosteten Webseiten.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-130">The Download Manager is the solution for downloading content from script code in hosted webpages.</span></span> <span data-ttu-id="d6f7c-131">Zum Herunterladen von Inhalten mithilfe von C++-Code verwenden Sie Windows XP Background Intelligent Transfer Service (Bits).</span><span class="sxs-lookup"><span data-stu-id="d6f7c-131">To download content using C++ code, use the Windows XP Background Intelligent Transfer Service (BITS).</span></span> <span data-ttu-id="d6f7c-132">Weitere Informationen finden Sie unter [Bits](bits.md).</span><span class="sxs-lookup"><span data-stu-id="d6f7c-132">For more information, see [BITS](bits.md).</span></span>

## <a name="about-background-and-real-time-downloading"></a><span data-ttu-id="d6f7c-133">Informationen zu Hintergrund-und Echt Zeit Downloads</span><span class="sxs-lookup"><span data-stu-id="d6f7c-133">About Background and Real-time Downloading</span></span>

<span data-ttu-id="d6f7c-134">Der Download-Manager bietet zwei Arten von Downloads: Hintergrund und Echt Zeit.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-134">The Download Manager offers two types of downloading: background and real-time.</span></span> <span data-ttu-id="d6f7c-135">Welchen Typ Sie verwenden, ist Ihnen überlassen, und es ist möglich, dem Benutzer auch das Auswählen des Download Typs zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-135">Which type you use is up to you, and it is possible to allow the user to select the download type as well.</span></span> <span data-ttu-id="d6f7c-136">Wenn Sie dem Benutzer die Auswahl des Download Typs gestatten, sollten Sie die Unterschiede zwischen den beiden verfügbaren Typen erläutern.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-136">If you choose to allow the user to select the download type, be sure to explain the differences between the two available types.</span></span>

<span data-ttu-id="d6f7c-137">Der Echt Zeit Download erfolgt gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-137">Real-time downloading occurs all at once.</span></span> <span data-ttu-id="d6f7c-138">Wenn der Benutzer einen Datei Download startet, wird die gesamte Datei in einem einzigen kontinuierlichen Stream auf den Computer des Benutzers übertragen.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-138">When the user starts a file download, the entire file is transferred to the user's computer in a single, continuous stream.</span></span> <span data-ttu-id="d6f7c-139">Der Benutzer kann den Download nicht anhalten oder anderweitig unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-139">The user cannot pause or otherwise interrupt the download.</span></span> <span data-ttu-id="d6f7c-140">Wenn der Benutzer Windows Media Player schließen möchte, bevor der Download abgeschlossen ist, verliert er alle unvollständigen Dateien und muss Sie von Anfang an herunterladen, um den Inhalt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-140">If the user chooses to close Windows Media Player before the download is finished, he or she loses any incomplete files and must download them from the beginning to acquire the content.</span></span>

<span data-ttu-id="d6f7c-141">Der Hauptvorteil von Echt Zeit Downloads besteht darin, dass der Benutzer den Inhalt schneller als das Herunterladen im Hintergrund abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-141">The main advantage of real-time downloading is that it allows the user to acquire the content faster than background downloading.</span></span> <span data-ttu-id="d6f7c-142">Das Herunterladen in Echtzeit ist für Benutzer von Windows XP verfügbar, aber es ist die einzige Art von Download, die unter Versionen des Windows-Betriebssystems vor Windows XP verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-142">Real-time downloading is available to users of Windows XP, but it is the only type of downloading available on versions of the Windows operating system prior to Windows XP.</span></span>

<span data-ttu-id="d6f7c-143">Das Herunterladen im Hintergrund erfolgt schrittweise.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-143">Background downloading happens in a piecemeal fashion.</span></span> <span data-ttu-id="d6f7c-144">Wenn der Benutzer einen Download im Hintergrund startet, werden Teile der Datei auf den Computer des Benutzers übertragen, wenn die Prozessorzeit verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-144">When the user starts a background download, parts of the file are transferred to the user's computer when processor time is available.</span></span> <span data-ttu-id="d6f7c-145">Es ist möglich, einen Hintergrund Download anzuhalten und fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-145">It is possible to pause and resume a background download.</span></span> <span data-ttu-id="d6f7c-146">Wenn sich der Benutzer für das Schließen von Windows-Media Player entscheidet, bevor das Herunterladen des Hintergrunds abgeschlossen ist, wird die Bedingung aller unvollständigen Dateien gespeichert, und der Download kann im Hintergrund fortgesetzt werden, auch nachdem der Computer neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-146">If the user chooses to close Windows Media Player before background downloading is finished, the condition of any incomplete files is saved and the downloading can continue in the background, even after restarting the computer.</span></span>

<span data-ttu-id="d6f7c-147">Das Herunterladen im Hintergrund kann länger dauern als das Herunterladen in Echtzeit, da der Downloadvorgang nur erfolgt, wenn der Prozessor keine anderen Tasks ausführt.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-147">Background downloading can take longer than real-time downloading because the download process only happens when the processor is not performing other tasks.</span></span>

<span data-ttu-id="d6f7c-148">Das Herunterladen im Hintergrund ist nur bei Verwendung von Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-148">Background downloading is only available when using Windows XP.</span></span>

## <a name="about-library-integration"></a><span data-ttu-id="d6f7c-149">Informationen zur Bibliotheks Integration</span><span class="sxs-lookup"><span data-stu-id="d6f7c-149">About Library Integration</span></span>

<span data-ttu-id="d6f7c-150">Windows Media Player kann Online Store-Inhalte in der Bibliothek automatisch organisieren.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-150">Windows Media Player can automatically organize online store content in the library.</span></span> <span data-ttu-id="d6f7c-151">Um dies zu ermöglichen, müssen Sie für jede digitale Mediendatei einen Wert für das Attribut " **WM/contentdistributor** " angeben.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-151">To enable this, you must specify a value for the **WM/ContentDistributor** attribute for each digital media file.</span></span> <span data-ttu-id="d6f7c-152">Wenn der Bibliothek eine digitale Mediendatei hinzugefügt wird, die automatisch bei Verwendung des Download-Managers erfolgt, wird die Datei automatisch im Knoten **erworbene Musik** oder **erworbene Videos** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6f7c-152">When a digital media file is added to the library, which happens automatically when using the Download Manager, the file is listed in the **Purchased Music** or **Purchased Videos** node automatically.</span></span> <span data-ttu-id="d6f7c-153">Wenn der Wert für **WM/contentdistributor** beispielsweise "Proseware" lautet und die digitale Mediendatei Musik enthält, wird der Inhalt in der Bibliothek am folgenden Speicherort angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d6f7c-153">For example, if the value for **WM/ContentDistributor** is "Proseware" and the digital media file contains music, the content would appear in the library in the following location:</span></span>

<span data-ttu-id="d6f7c-154">Alle Musik/erworbenen Musik/Proseware</span><span class="sxs-lookup"><span data-stu-id="d6f7c-154">All Music/Purchased Music/Proseware</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6f7c-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6f7c-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f7c-156">**Download-Manager**</span><span class="sxs-lookup"><span data-stu-id="d6f7c-156">**Download Manager**</span></span>](download-manager.md)
</dt> <dt>

[<span data-ttu-id="d6f7c-157">**Download Collection. startDownload**</span><span class="sxs-lookup"><span data-stu-id="d6f7c-157">**DownloadCollection.startDownload**</span></span>](downloadcollection-startdownload.md)
</dt> </dl>

 

 




