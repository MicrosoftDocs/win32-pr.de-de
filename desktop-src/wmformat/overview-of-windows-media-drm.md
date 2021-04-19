---
title: Übersicht über Windows Media DRM
description: Übersicht über Windows Media DRM
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Lizenzen für DRM
- Digital Rights Management (DRM), Informationen zu
- DRM (Digital Rights Management), Informationen zu
- Digital Rights Management (DRM), Verpacken von Windows Media-Dateien
- DRM (Digital Rights Management), Verpacken von Windows Media-Dateien
- Digital Rights Management (DRM), geschützte Datei Lizenzierung
- DRM (Digital Rights Management), geschützte Datei Lizenzierung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), lesen geschützter Dateien
- DRM (Digital Rights Management), lesen geschützter Dateien
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- Lizenzen, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341839"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="c311f-119">Übersicht über Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="c311f-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="c311f-120">Bei Windows Media Digital Rights Management (DRM) handelt es sich um ein System zum Schutz der Inhalte in Windows Media-Dateien, sodass nicht autorisierte Benutzer nicht darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="c311f-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="c311f-121">Der grundlegende DRM-Cycle umfasst drei Phasen: Verpacken, Lizenzierung und lesen.</span><span class="sxs-lookup"><span data-stu-id="c311f-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="c311f-122">Verpacken von Windows Media-Dateien</span><span class="sxs-lookup"><span data-stu-id="c311f-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="c311f-123">Windows Media DRM ist für die Arbeit mit Windows Media-Dateien konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c311f-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="c311f-124">Eine Windows Media-Datei ist eine Datei, die der "Advanced Systems Format (ASF)"-Spezifikation entspricht und nur Audiodateien und Videos enthält, die mithilfe der Windows Media Audio-und Video Codecs komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c311f-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="c311f-125">Wenn eine ASF-Datei gepackt wird, wird ein DRM-spezifischer Abschnitt zum-Header hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c311f-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="c311f-126">Der DRM-Header enthält eine Schlüssel-ID, die den Inhalt für die Lizenzierung identifiziert, und eine Lizenz Erwerbs-URL. Hierbei handelt es sich um die Adresse einer Webseite, die Lizenzen zum Lesen geschützter Inhalte ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="c311f-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="c311f-127">Es gibt noch viel mehr Informationen, die in den DRM-Header eingefügt werden können. Dies ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="c311f-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="c311f-128">Der DRM-Header ist signiert, sodass der Packager überprüft werden kann.</span><span class="sxs-lookup"><span data-stu-id="c311f-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="c311f-129">Der Inhalt in der ASF-Datei wird während des Verpackungsvorgangs verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c311f-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="c311f-130">Die folgenden Informationen in der Paketdatei sind jedoch auch für Clients verfügbar, die nicht über eine Lizenz verfügen:</span><span class="sxs-lookup"><span data-stu-id="c311f-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="c311f-131">Metadaten, die im ASF-Header gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c311f-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="c311f-132">Einige Metadaten, die im DRM-Header gespeichert sind (z. b. können Sie immer die Lizenz Erwerbs-URL abrufen).</span><span class="sxs-lookup"><span data-stu-id="c311f-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="c311f-133">Lizenzieren geschützter Dateien</span><span class="sxs-lookup"><span data-stu-id="c311f-133">Licensing Protected Files</span></span>

<span data-ttu-id="c311f-134">Damit eine Paketdatei gelesen wird, muss eine Lizenz an den Client Computer ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c311f-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="c311f-135">Eine Lizenz besteht aus einem Satz von Daten, die die Bedingungen beschreiben, unter denen Daten in geschützten Dateien gelesen werden können.</span><span class="sxs-lookup"><span data-stu-id="c311f-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="c311f-136">In den meisten Fällen wird eine Lizenz für eine geschützte Datei ausgegeben, als Antwort darauf, dass der Benutzer versucht, einen Vorgang für die Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c311f-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="c311f-137">Es ist jedoch auch möglich, dass ein Lizenz Aussteller Lizenzen an einen Client übermitteln muss, bevor er explizit angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c311f-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="c311f-138">Weitere Informationen zu Lizenzen finden Sie unter [Lizenzen](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="c311f-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="c311f-139">Lesen von Daten aus geschützten Dateien</span><span class="sxs-lookup"><span data-stu-id="c311f-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="c311f-140">Wenn ein Benutzer versucht, einen Vorgang für eine geschützte Datei auszuführen (Wiedergabe, Brennen auf CD, kopieren auf ein Gerät usw.), muss die Anwendung auf dem Client Computer nach Lizenzen suchen.</span><span class="sxs-lookup"><span data-stu-id="c311f-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="c311f-141">Wenn auf dem Client Computer eine gültige Lizenz vorhanden ist, kann der Vorgang fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c311f-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="c311f-142">Wenn keine Lizenz für den Inhalt vorhanden ist oder wenn keine Lizenz für den Inhalt, der auf dem Client Computer vorhanden ist, die angeforderte Aktion zulässt, muss eine Lizenz erworben werden.</span><span class="sxs-lookup"><span data-stu-id="c311f-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c311f-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c311f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c311f-144">**Informationen zu den erweiterten APIs für den Windows Media DRM-Client**</span><span class="sxs-lookup"><span data-stu-id="c311f-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




