---
title: Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden
description: Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Device Manager, Portable Audioplayer
- Device Manager, Portable Audioplayer
- Programmier Handbuch, Portable Audioplayer
- Dienstanbieter, Portable Audioplayer
- Erstellen von Dienstanbietern, portablen Audioplayern
- Portable Audioplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340837"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="af8ea-109">Anforderungen für tragbare Audioplayer, die im Windows-Explorer angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="af8ea-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="af8ea-110">Die Portable Audioplayer-Shell-Namespace Erweiterung bietet Windows-Benutzern eine konsistente Möglichkeit, Audiogeräte zu verwalten, die von Windows Media Device Manager verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="af8ea-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="af8ea-111">Wenn Sie den Dienstanbieter und die Treiber Komponenten gemäß den folgenden Richtlinien erstellen, wird Ihr Gerät im Shell-Namespace angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af8ea-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="af8ea-112">Benutzer können in Windows-Explorer auf konsistente Weise mit den Inhalten Ihres Geräts interagieren, um grundlegende Vorgänge wie das Kopieren, löschen und Umbenennen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="af8ea-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="af8ea-113">Die folgenden shellanforderungen für Dienstanbieter und Treiber Komponenten dienen dazu, die allgemeinen Richtlinien für Windows Media-Device Manager zu ergänzen.</span><span class="sxs-lookup"><span data-stu-id="af8ea-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="af8ea-114">Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="af8ea-114">Device Capabilities</span></span>

<span data-ttu-id="af8ea-115">Windows Media Device Manager-Dienstanbieter sollten in Ihren unterstützten Funktionen explizit sein.</span><span class="sxs-lookup"><span data-stu-id="af8ea-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="af8ea-116">Wenn ein-Befehl nicht unterstützt wird, muss ein Fehlercode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="af8ea-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="af8ea-117">Die entsprechenden Felder müssen für das vorhanden sein oder Fehlen von Funktionen für die Rückgabe der folgenden Funktionen festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="af8ea-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="af8ea-118">**Imdspstorageglobals:: getfunktionen**</span><span class="sxs-lookup"><span data-stu-id="af8ea-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="af8ea-119">**Imdspstorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="af8ea-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="af8ea-120">**Imdspdevice:: getformatsupport**</span><span class="sxs-lookup"><span data-stu-id="af8ea-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="af8ea-121">Dienstanbieter müssen die folgenden Funktionen unterstützen, um mit der Shell kompatibel zu sein:</span><span class="sxs-lookup"><span data-stu-id="af8ea-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="af8ea-122">Kopieren auf das Gerät (mit Unterstützung für Abbruch-und Fortschritts Rückrufe)</span><span class="sxs-lookup"><span data-stu-id="af8ea-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="af8ea-123">Datei von Gerät löschen (mit Unterstützung für Abbruch-und Fortschritts Rückrufe)</span><span class="sxs-lookup"><span data-stu-id="af8ea-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="af8ea-124">Datei auf Gerät umbenennen</span><span class="sxs-lookup"><span data-stu-id="af8ea-124">Rename file on device</span></span>
-   <span data-ttu-id="af8ea-125">Speicherplatz Berichterstattung (Gesamter Speicherplatz, freier Speicherplatz, nicht verwendbar)</span><span class="sxs-lookup"><span data-stu-id="af8ea-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="af8ea-126">Plug & Play (siehe [Aktivieren von PNP für Geräte](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="af8ea-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="af8ea-127">Format (vorzugsweise mit Unterstützung für Abbruch-und Fortschritts Rückrufe)</span><span class="sxs-lookup"><span data-stu-id="af8ea-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="af8ea-128">Wenn Metadaten unterstützt werden, müssen die folgenden Felder für einzelne Dateien unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="af8ea-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="af8ea-129">Wenn keine Daten verfügbar sind, sollte das Feld als leere Zeichenfolge initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="af8ea-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="af8ea-130">Feld</span><span class="sxs-lookup"><span data-stu-id="af8ea-130">Field</span></span>        | <span data-ttu-id="af8ea-131">Konstante (in WMDM. idl definiert)</span><span class="sxs-lookup"><span data-stu-id="af8ea-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="af8ea-132">Metadatentag</span><span class="sxs-lookup"><span data-stu-id="af8ea-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="af8ea-133">Titeltitel</span><span class="sxs-lookup"><span data-stu-id="af8ea-133">Song Title</span></span>   | <span data-ttu-id="af8ea-134">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="af8ea-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="af8ea-135">WMDM/Titel</span><span class="sxs-lookup"><span data-stu-id="af8ea-135">WMDM/Title</span></span>      |
| <span data-ttu-id="af8ea-136">Nachverfolgen der Nummer</span><span class="sxs-lookup"><span data-stu-id="af8ea-136">Track Number</span></span> | <span data-ttu-id="af8ea-137">g \_ wszwmdmtrack</span><span class="sxs-lookup"><span data-stu-id="af8ea-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="af8ea-138">WMDM/Track</span><span class="sxs-lookup"><span data-stu-id="af8ea-138">WMDM/Track</span></span>      |
| <span data-ttu-id="af8ea-139">Interpret</span><span class="sxs-lookup"><span data-stu-id="af8ea-139">Artist</span></span>       | <span data-ttu-id="af8ea-140">g \_ wszwmdmauthor</span><span class="sxs-lookup"><span data-stu-id="af8ea-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="af8ea-141">WMDM/Autor</span><span class="sxs-lookup"><span data-stu-id="af8ea-141">WMDM/Author</span></span>     |
| <span data-ttu-id="af8ea-142">Aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="af8ea-142">Album</span></span>        | <span data-ttu-id="af8ea-143">g \_ wszwmdmalbumtitle</span><span class="sxs-lookup"><span data-stu-id="af8ea-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="af8ea-144">WMDM/albumtitle</span><span class="sxs-lookup"><span data-stu-id="af8ea-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="af8ea-145">Year</span><span class="sxs-lookup"><span data-stu-id="af8ea-145">Year</span></span>         | <span data-ttu-id="af8ea-146">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="af8ea-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="af8ea-147">WMDM/Jahr</span><span class="sxs-lookup"><span data-stu-id="af8ea-147">WMDM/Year</span></span>       |
| <span data-ttu-id="af8ea-148">Genre</span><span class="sxs-lookup"><span data-stu-id="af8ea-148">Genre</span></span>        | <span data-ttu-id="af8ea-149">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="af8ea-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="af8ea-150">WMDM/Genre</span><span class="sxs-lookup"><span data-stu-id="af8ea-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="af8ea-151">Parallelität</span><span class="sxs-lookup"><span data-stu-id="af8ea-151">Concurrency</span></span>

<span data-ttu-id="af8ea-152">Kernelmodustreiber für Windows Media Device Manager müssen bei der Behandlung des gleichzeitigen Zugriffs robust sein.</span><span class="sxs-lookup"><span data-stu-id="af8ea-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="af8ea-153">Beispielsweise kann ein Benutzer gleichzeitig sowohl über die Shell als auch über den Media Player oder einfach über mehrere Fenster in der Shell auf das Gerät zugreifen.</span><span class="sxs-lookup"><span data-stu-id="af8ea-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="af8ea-154">Im Rahmen der Handhabung von Parallelität sollten Treiber nicht davon ausgehen, dass der Dienstanbieter geladen ist, dass das Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af8ea-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="af8ea-155">Stattdessen sollten Sie einen Sperrmechanismus implementieren, um den Zugriff auf das Gerät nach Bedarf für einzelne Vorgänge zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="af8ea-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="af8ea-156">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="af8ea-156">UI</span></span>

<span data-ttu-id="af8ea-157">Dienstanbieter für Windows Media Device Manager sollten keine Benutzeroberfläche anzeigen.</span><span class="sxs-lookup"><span data-stu-id="af8ea-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="af8ea-158">Alle Fehler sollten von Methoden aufrufen als bestimmte Windows Media-Device Manager Fehlercodes zurückgegeben werden, wann immer dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="af8ea-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="af8ea-159">Aktivieren in der Shell</span><span class="sxs-lookup"><span data-stu-id="af8ea-159">Enabling in the Shell</span></span>

<span data-ttu-id="af8ea-160">Wenn Ihr Paket alle shellanforderungen erfüllt, können Sie das Gerät in der Shell anzeigen lassen, indem Sie den *showinshell* -Wert unter den Geräteparametern auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="af8ea-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="af8ea-161">Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="af8ea-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af8ea-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af8ea-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af8ea-163">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="af8ea-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




