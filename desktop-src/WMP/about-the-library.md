---
title: Informationen zur Bibliothek
description: Informationen zur Bibliothek
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player Bibliothek, Informationen zu
- Bibliothek, Informationen zu
- Metadaten, Windows-Media Player Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1781329a78bcb2e9cb25c45135e03465b9d63df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340813"
---
# <a name="about-the-library"></a><span data-ttu-id="c5e70-113">Informationen zur Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5e70-113">About the Library</span></span>

<span data-ttu-id="c5e70-114">Bei der Bibliothek handelt es sich um eine Datenbank mit Informationen oder *Metadaten* zu den digitalen Medieninhalten, die für Windows-Media Player verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5e70-114">The library is a database of information, or *metadata*, about the digital media content that is available to Windows Media Player.</span></span> <span data-ttu-id="c5e70-115">Einige der Informationen werden im Bereich **Bibliothek** im Player angezeigt. Weitere Informationen finden Sie im Code.</span><span class="sxs-lookup"><span data-stu-id="c5e70-115">Some of the information is displayed in the **Library** pane in the Player; more of it is available through code.</span></span>

<span data-ttu-id="c5e70-116">(In der Windows Media Player 9-Serie und früher wird diese Funktion als **Medienbibliothek** bezeichnet.)</span><span class="sxs-lookup"><span data-stu-id="c5e70-116">(In Windows Media Player 9 Series and earlier, this feature is called **Media Library**.)</span></span>

<span data-ttu-id="c5e70-117">Die-Bibliothek bietet Benutzern eine einfache Möglichkeit zum organisieren und Zugreifen auf digitale Medieninhalte.</span><span class="sxs-lookup"><span data-stu-id="c5e70-117">The library gives users an easy way to organize and access digital media content.</span></span> <span data-ttu-id="c5e70-118">Beispielsweise können Benutzer Musik, geordnet nach Album, nach Genre oder einfach als Liste aller Musik anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c5e70-118">For example, users can view music organized by album, by artist, by genre, or simply as a list of all music.</span></span> <span data-ttu-id="c5e70-119">Mit dem Windows Media Player SDK-Objektmodell können Sie auf die Bibliothek zugreifen, um Inhalte wiederzugeben, Wiedergabelisten abzurufen, Inhalte hinzuzufügen, Inhalte zu entfernen und die zugehörigen Metadaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c5e70-119">You can use the Windows Media Player SDK object model to access the library to play content, retrieve playlists, add content, remove content, and change the associated metadata.</span></span> <span data-ttu-id="c5e70-120">Windows Media Player schützt den Datenschutz der Benutzer, indem die Möglichkeit eingeschränkt wird, über Code unter bestimmten Bedingungen auf die Bibliothek zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c5e70-120">Windows Media Player protects users' privacy by restricting your ability to access the library from code under certain conditions.</span></span> <span data-ttu-id="c5e70-121">Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c5e70-121">For more information about access rights, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c5e70-122">Die Bibliothek speichert Metadaten zu zwei grundlegenden Arten von digitalen Medieninhalten.</span><span class="sxs-lookup"><span data-stu-id="c5e70-122">The library stores metadata about two basic types of digital media content.</span></span> <span data-ttu-id="c5e70-123">Der erste Typ, digitale Medienelemente, sind einzelne Inhalts Dateien, z. b. ein Musiktitel oder ein Foto.</span><span class="sxs-lookup"><span data-stu-id="c5e70-123">The first type, digital media items, are individual content files, such as a music track or a photo.</span></span> <span data-ttu-id="c5e70-124">Der zweite Typ, Wiedergabelisten, sind Dateien, die eine Gruppe digitaler Medienelemente darstellen, die in der Regel in einer angegebenen Reihenfolge wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c5e70-124">The second type, playlists, are files that represent a group of digital media items, typically intended to be played in a specified order.</span></span> <span data-ttu-id="c5e70-125">Die Metadaten, die digitalen Medieninhalten zugeordnet sind, werden als Name-Wert-Paare gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c5e70-125">The metadata associated with digital media content is stored as name-value pairs.</span></span> <span data-ttu-id="c5e70-126">Beispielsweise werden die Metadaten, die die Person beschreiben, die einen Song ausgeführt hat, "Artist" genannt, und der zugeordnete Wert ist in der Regel eine Text Zeichenfolge, die den Namen des Performers enthält.</span><span class="sxs-lookup"><span data-stu-id="c5e70-126">For example, the metadata that describes the person who performed a song is named "Artist" and the value associated with it typically is a text string containing the performer's name.</span></span> <span data-ttu-id="c5e70-127">Jeder eindeutige Metadatenname wird als *Attribut* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5e70-127">Each unique metadata name is called an *attribute*.</span></span> <span data-ttu-id="c5e70-128">Eine Auflistung der unterstützten Attribute finden Sie unter [Attribut Verweis](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="c5e70-128">For a listing of supported attributes, see the [Attribute Reference](attribute-reference.md).</span></span> <span data-ttu-id="c5e70-129">Weitere Informationen zur Verwendung von Attributen im Code finden Sie unter [Medien Element Attribute](media-item-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="c5e70-129">For information about using attributes in code, see [Media Item Attributes](media-item-attributes.md).</span></span>

<span data-ttu-id="c5e70-130">In den folgenden Abschnitten finden Sie weitere Informationen zum Arbeiten mit der-Bibliothek:</span><span class="sxs-lookup"><span data-stu-id="c5e70-130">The following sections provide more information about working with the library:</span></span>

-   [<span data-ttu-id="c5e70-131">Programm gesteuerter Zugriff auf die Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5e70-131">Accessing the Library Programmatically</span></span>](accessing-the-library-programmatically.md)
-   [<span data-ttu-id="c5e70-132">Informationen zu Bibliothek Diensten</span><span class="sxs-lookup"><span data-stu-id="c5e70-132">About Library Services</span></span>](about-library-services.md)

## <a name="related-topics"></a><span data-ttu-id="c5e70-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5e70-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5e70-134">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="c5e70-134">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




