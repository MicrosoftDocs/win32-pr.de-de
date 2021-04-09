---
title: Medien Element Attribute
description: Medien Element Attribute
ms.assetid: d43addec-e06c-4ef3-9012-3ecf589b105c
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player, Attribute für Medienelemente
- Windows Media Player-Objektmodell, Attribute für Medienelemente
- Objektmodell, Attribute für Medienelemente
- Windows Media Player Mobile, Attribute für Medienelemente
- Windows Media Player ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player Mobile ActiveX-Steuerelement, Attribute für Medienelemente
- ActiveX-Steuerelement, Attribute für Medienelemente
- Windows Media Player-Bibliothek, Attribute für Medienelemente
- Bibliothek, Attribute für Medienelemente
- Attribute, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac8595cc07504c9cd3e195431513a1f8565e87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036928"
---
# <a name="media-item-attributes"></a><span data-ttu-id="80222-120">Medien Element Attribute</span><span class="sxs-lookup"><span data-stu-id="80222-120">Media Item Attributes</span></span>

<span data-ttu-id="80222-121">Wenn Sie sich die Bibliothek in Windows Media Player ansehen, sehen Sie in der Regel eine große Menge an Informationen zu einem Medien Element.</span><span class="sxs-lookup"><span data-stu-id="80222-121">When you look at the library in Windows Media Player, you typically see a great deal of information about a media item.</span></span> <span data-ttu-id="80222-122">Neben dem Namen eines Audiotitels sehen Sie z. b. wahrscheinlich den Namen des Albums, auf dem sich der Titel befindet, die Namen des Künstlers und Composer, das Genre der Musik usw.</span><span class="sxs-lookup"><span data-stu-id="80222-122">In addition to the name of an audio track, for example, you will likely see the name of the album the track is on, the names of the artist and composer, the genre of the music, and so on.</span></span>

<span data-ttu-id="80222-123">Im Windows Media Player-Objektmodell werden diese Metadatenelemente als Attribute bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="80222-123">In the Windows Media Player object model, these metadata items are called attributes.</span></span> <span data-ttu-id="80222-124">Das Objektmodell enthält Eigenschaften und Methoden, die Sie verwenden können, um Medienelemente und Wiedergabelisten für Attribute abzufragen.</span><span class="sxs-lookup"><span data-stu-id="80222-124">The object model includes properties and methods you can use to query media items and playlists for attributes.</span></span> <span data-ttu-id="80222-125">Anschließend können Sie Attributwerte in der Benutzeroberfläche anzeigen, oder der Code kann basierend auf dem Wert eines Attributs Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="80222-125">You can then display attribute values in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="80222-126">In den folgenden Themen wird das Arbeiten mit Medien Element Attributen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="80222-126">The following topics describe working with media item attributes.</span></span>



| <span data-ttu-id="80222-127">Thema</span><span class="sxs-lookup"><span data-stu-id="80222-127">Topic</span></span>                                                                                      | <span data-ttu-id="80222-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80222-128">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80222-129">Grundlegendes zu Attribut Quellen</span><span class="sxs-lookup"><span data-stu-id="80222-129">Understanding Attribute Sources</span></span>](understanding-attribute-sources.md)                     | <span data-ttu-id="80222-130">Beschreibt, wie sich die Quelle eines Medien Elements auf die Attribute auswirkt, die ihm zugeordnet sein können.</span><span class="sxs-lookup"><span data-stu-id="80222-130">Describes how the source of a media item affects the attributes that may be associated with it.</span></span> |
| [<span data-ttu-id="80222-131">Lesen von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="80222-131">Reading Attribute Values</span></span>](reading-attribute-values.md)                                   | <span data-ttu-id="80222-132">Zeigt die Methoden zum Abrufen des Werts eines Attributs an.</span><span class="sxs-lookup"><span data-stu-id="80222-132">Shows the methods for retrieving the value of an attribute.</span></span>                                     |
| [<span data-ttu-id="80222-133">Attribute mit mehreren Werten</span><span class="sxs-lookup"><span data-stu-id="80222-133">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md)                     | <span data-ttu-id="80222-134">Zeigt die Methoden zum Abrufen des Werts eines mehrwertigen Attributs an.</span><span class="sxs-lookup"><span data-stu-id="80222-134">Shows the methods for retrieving the value of a multi-valued attribute.</span></span>                         |
| [<span data-ttu-id="80222-135">Lesen von Attributwerten von einer CD oder DVD</span><span class="sxs-lookup"><span data-stu-id="80222-135">Reading Attribute Values from a CD or DVD</span></span>](reading-attribute-values-from-a-cd-or-dvd.md) | <span data-ttu-id="80222-136">Stellt eine Beispielanwendung bereit, die alle Attribute eines Medien Elements liest.</span><span class="sxs-lookup"><span data-stu-id="80222-136">Provides a sample application that reads all of the attributes of a media item.</span></span>                 |
| [<span data-ttu-id="80222-137">Ändern von Attributwerten</span><span class="sxs-lookup"><span data-stu-id="80222-137">Changing Attribute Values</span></span>](changing-attribute-values.md)                                 | <span data-ttu-id="80222-138">Zeigt die Methode zum Ändern des Werts eines Attributs.</span><span class="sxs-lookup"><span data-stu-id="80222-138">Shows the method for changing the value of an attribute.</span></span>                                        |
| [<span data-ttu-id="80222-139">Attributwerte für TV-Inhalt</span><span class="sxs-lookup"><span data-stu-id="80222-139">Attribute Values for TV Content</span></span>](attribute-values-for-tv-content.md)                     | <span data-ttu-id="80222-140">Zeigt, wie Attribute für digitale Videoinhalte angegeben werden, die Fernsehsendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="80222-140">Shows how to specify attributes for digital video content that contains TV shows.</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="80222-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="80222-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80222-142">**Wiedergabelisten Attribute**</span><span class="sxs-lookup"><span data-stu-id="80222-142">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> <dt>

[<span data-ttu-id="80222-143">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="80222-143">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




