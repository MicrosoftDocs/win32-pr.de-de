---
title: Informationen zur Wiedergabeliste
description: Informationen zur Wiedergabeliste
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, Wiedergabelisten Synchronisierung
- Windows Media Player-Objektmodell, Wiedergabelisten Synchronisierung
- Objektmodell, Wiedergabelisten Synchronisierung
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten Synchronisierung
- ActiveX-Steuerelement, Wiedergabeliste
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten Synchronisierung
- Windows Media Player Mobile, Wiedergabelisten Synchronisierung
- Synchronisieren von Geräten, Wiedergabelisten
- Geräte Synchronisierung, Wiedergabelisten
- Wiedergabelisten, Synchronisierung
- Windows Media Metadatei-Wiedergabelisten, Synchronisierung
- Metadatei-Wiedergabelisten, Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314243"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="f0d48-115">Informationen zur Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="f0d48-115">About Playlist Synchronization</span></span>

<span data-ttu-id="f0d48-116">Windows Media Player 10 oder höher ist so konzipiert, dass digitale Medieninhalte mithilfe eines Wiedergabelisten-Synchronisierungs Modells mit Geräten synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f0d48-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="f0d48-117">Dies bedeutet, dass Inhalte, die auf ein Gerät kopiert werden sollen, Teil einer Wiedergabeliste sein müssen.</span><span class="sxs-lookup"><span data-stu-id="f0d48-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="f0d48-118">Wenn der Benutzer die Inhalte einzelner digitaler Medien von seinem Computer auf ein Gerät übertragen möchte, fügt Windows Media Player den Inhalt einer Standard Wiedergabeliste zum Kopieren hinzu.</span><span class="sxs-lookup"><span data-stu-id="f0d48-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="f0d48-119">Die APIs für die Synchronisierung von Windows Media Player-Geräten sind so konzipiert, dass Sie auch so funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f0d48-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="f0d48-120">Wie bei Windows Media Player kann das Programm dem Benutzer eine Liste der von ihm definierten Wiedergabelisten präsentieren.</span><span class="sxs-lookup"><span data-stu-id="f0d48-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="f0d48-121">Anschließend können Sie es dem Benutzer ermöglichen, auszuwählen, welche Wiedergabelisten mit einem bestimmten Gerät synchronisiert werden sollen, und die Prioritäts Reihenfolge für den Synchronisierungs Prozess festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f0d48-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="f0d48-122">Da tragbare Geräte über eine begrenzte Speicherkapazität verfügen, ist es möglich, dass der Benutzer mehr digitale Medieninhalte synchronisiert, als das Gerät speichern kann.</span><span class="sxs-lookup"><span data-stu-id="f0d48-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="f0d48-123">Windows Media Player synchronisiert Inhalte in der Prioritäts Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="f0d48-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="f0d48-124">Der Benutzer kann die Prioritäts Reihenfolge mithilfe eines Dialog Felds definieren, auf das über die **Geräte** Funktion zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0d48-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="f0d48-125">Als Reaktion auf Benutzereingaben für Ihr Programm können Sie die Prioritäts Reihenfolge Programm gesteuert ändern, indem Sie die Werte bestimmter Wiedergabelisten Attribute ändern.</span><span class="sxs-lookup"><span data-stu-id="f0d48-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="f0d48-126">Gemeinsam werden diese Attribute als *Synchronisierungs* Attribute bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f0d48-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="f0d48-127">Jede Wiedergabeliste in einer Bibliothek hat 16 Synchronisierungs Attribute: **Sync01** bis **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="f0d48-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="f0d48-128">Jedes Attribut stellt das Gerät dar, das über den entsprechenden Partnerschafts Index verfügt.</span><span class="sxs-lookup"><span data-stu-id="f0d48-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="f0d48-129">Der Wert jedes Attributs gibt Ihnen zwei Dinge:</span><span class="sxs-lookup"><span data-stu-id="f0d48-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="f0d48-130">Gibt an, ob die Wiedergabeliste mit dem Gerät synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0d48-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="f0d48-131">Der Prioritätswert für die Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="f0d48-131">The priority value for the playlist.</span></span>

<span data-ttu-id="f0d48-132">Der Wert 0 (null) gibt an, dass Windows Media Player nicht versuchen soll, die Wiedergabeliste mit dem Gerät zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f0d48-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="f0d48-133">Jeder andere Wert ist eine Prioritäts Nummer.</span><span class="sxs-lookup"><span data-stu-id="f0d48-133">Any other value is a priority number.</span></span> <span data-ttu-id="f0d48-134">Niedrigere Werte erhalten zum Zeitpunkt der Synchronisierung höhere Priorität.</span><span class="sxs-lookup"><span data-stu-id="f0d48-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="f0d48-135">Wiedergabelisten verfügen auch über ein **synkonstante** Attribut, das angibt, ob die Wiedergabeliste nur für die Synchronisierung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f0d48-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="f0d48-136">Einzelne Elemente digitaler Medieninhalte enthalten ebenfalls Metadaten über die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="f0d48-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="f0d48-137">Wenn Sie ein **Medien** Objekt aus der Bibliothek abrufen, können Sie den Wert des **SyncState** -Attributs überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f0d48-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="f0d48-138">Dieses Attribut enthält erweiterte Informationen darüber, ob der Inhalt erfolgreich auf das Gerät kopiert wurde oder ob beim Kopieren des Inhalts ein Fehler aufgetreten ist, weil er nicht geeignet wäre.</span><span class="sxs-lookup"><span data-stu-id="f0d48-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="f0d48-139">Vermeiden Sie die Bereitstellung von Benutzeroberflächen Elementen, die es dem Benutzer ermöglichen, für die Synchronisierung Wiedergabelisten aus allen Bibliotheks Inhalten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0d48-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="f0d48-140">Um die Leistung zu optimieren, erzwingt Windows Media Player einen Satz von Regeln zum Erstellen von Synchronisierungs Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="f0d48-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="f0d48-141">Ihr Programm sollte nur Synchronisierungs Wiedergabelisten für den von Ihnen bereitgestellten Inhalt erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0d48-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="f0d48-142">Erlauben Sie Windows Media Player, Synchronisierungs Wiedergabelisten für Inhalte zu erstellen, die der Bibliothek aus anderen Quellen hinzugefügt hat.</span><span class="sxs-lookup"><span data-stu-id="f0d48-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="f0d48-143">Als Alternative zum Erstellen einer eigenen Wiedergabeliste können Sie Benutzern ein Standard Dialogfeld für die Auswahl von Wiedergabelisten und die Verwaltung der Partnerschaft für ein Gerät präsentieren.</span><span class="sxs-lookup"><span data-stu-id="f0d48-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="f0d48-144">Nennen Sie hierzu [iwmpsyncdevice:: showsettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="f0d48-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="f0d48-145">Wenn Sie diese Methode aufrufen, zeigt Windows Media Player das Dialogfeld Synchronisierungs Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="f0d48-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="f0d48-146">Wenn der Benutzer das Dialogfeld schließt, kehrt Windows Media Player automatisch in seinen vorherigen Andock Zustand zurück und übergibt die Steuerung zurück an das Remote Programm.</span><span class="sxs-lookup"><span data-stu-id="f0d48-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0d48-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0d48-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0d48-148">**Informationen zur Geräte Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="f0d48-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="f0d48-149">**Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="f0d48-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="f0d48-150">**Wiedergabelisten Attribute**</span><span class="sxs-lookup"><span data-stu-id="f0d48-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




