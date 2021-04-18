---
title: Informationen zur Geräte Synchronisierung
description: Informationen zur Geräte Synchronisierung
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, Synchronisieren von Geräten
- Windows Media Player-Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX-Steuerelement, Synchronisieren von Geräten
- ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile, Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen zu
- Geräte Synchronisierung, Informationen zu
- Synchronisieren von Geräten, manuelle Übertragung
- Geräte Synchronisierung, manuelle Übertragung
- Synchronisieren von Geräten, automatische Synchronisierung
- Geräte Synchronisierung, automatische Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340617"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="01f92-116">Informationen zur Geräte Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="01f92-116">About Device Synchronization</span></span>

<span data-ttu-id="01f92-117">In Windows Media Player 10 wurde ein neues Modell für die Synchronisierung von Inhalten digitaler Medien mit tragbaren Geräten eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01f92-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="01f92-118">Aus Sicht des Benutzers bedeutet dies, dass Sie angeben können, welche Wiedergabelisten (einschließlich automatischer Wiedergabelisten) automatisch mit Geräten synchronisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="01f92-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="01f92-119">Sie können auch den Inhalt digitaler Medien manuell auf Geräte übertragen.</span><span class="sxs-lookup"><span data-stu-id="01f92-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="01f92-120">Aus Sicht des Entwicklers bedeutet dies, dass neue Funktionen verfügbar gemacht werden, die Sie in Ihren Anwendungen nutzen können.</span><span class="sxs-lookup"><span data-stu-id="01f92-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="01f92-121">Zu diesem Zweck müssen Sie eine Remote Instanz des Windows Media Player-Steuer Elements erstellen.</span><span class="sxs-lookup"><span data-stu-id="01f92-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="01f92-122">Es gibt zwei Möglichkeiten, wie ein Benutzer Digital Media-Inhalte auf ein Gerät kopieren kann:</span><span class="sxs-lookup"><span data-stu-id="01f92-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="01f92-123">**Manuelle Übertragung.**</span><span class="sxs-lookup"><span data-stu-id="01f92-123">**Manual transfer.**</span></span> <span data-ttu-id="01f92-124">Der Benutzer wählt den Inhalt digitaler Medien in der Bibliothek aus und initiiert dann eine Übertragung des Inhalts auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="01f92-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="01f92-125">Dies ist vergleichbar mit der Funktionalität, die in früheren Versionen von Windows Media Player bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="01f92-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="01f92-126">Das Windows Media Player SDK bietet keine Methoden zum Übertragen digitaler Medien auf ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="01f92-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="01f92-127">**Automatische Synchronisierung.**</span><span class="sxs-lookup"><span data-stu-id="01f92-127">**Automatic synchronization.**</span></span> <span data-ttu-id="01f92-128">Der Benutzer gibt Wiedergabelisten an, die automatisch mit dem Gerät synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="01f92-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="01f92-129">Dies ist ein Feature von Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="01f92-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="01f92-130">Das Windows Media Player SDK bietet Funktionen zum Verwalten der automatischen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="01f92-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="01f92-131">Mit dieser Funktion können Sie eine benutzerdefinierte Benutzeroberfläche für Ihre Anwendung erstellen, um anzugeben, wie die Geräte Synchronisierung durchgeführt wird, und um den Benutzern Statusinformationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="01f92-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="01f92-132">Damit die automatische Synchronisierung funktioniert, muss zwischen Windows Media Player und dem Gerät eine besondere Beziehung hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01f92-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="01f92-133">Diese Beziehung wird als *Partnerschaft* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="01f92-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="01f92-134">In den folgenden Abschnitten finden Sie weitere Informationen zur Geräte Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="01f92-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="01f92-135">Informationen zu Geräten</span><span class="sxs-lookup"><span data-stu-id="01f92-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="01f92-136">Informationen zu Partnerschaften</span><span class="sxs-lookup"><span data-stu-id="01f92-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="01f92-137">Informationen zur Synchronisierungs-Engine</span><span class="sxs-lookup"><span data-stu-id="01f92-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="01f92-138">Informationen zur Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="01f92-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="01f92-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01f92-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01f92-140">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="01f92-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="01f92-141">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="01f92-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="01f92-142">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="01f92-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




