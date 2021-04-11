---
title: Verwalten von Medien Elementen
description: Verwalten von Medien Elementen
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell, Bibliothek
- Windows Media Player Mobile, Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player-Bibliothek, Verwalten von Medien Elementen
- Bibliothek, Verwalten von Medien Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100810"
---
# <a name="managing-media-items"></a><span data-ttu-id="a3c46-112">Verwalten von Medien Elementen</span><span class="sxs-lookup"><span data-stu-id="a3c46-112">Managing Media Items</span></span>

<span data-ttu-id="a3c46-113">Ein **Medien** Objekt stellt ein Medien Element dar.</span><span class="sxs-lookup"><span data-stu-id="a3c46-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="a3c46-114">Es verfügt über Eigenschaften und Methoden, die Sie verwenden können, um Informationen abzurufen und für den Benutzer anzuzeigen, oder um verschiedene Aktionen basierend auf dem von Ihnen abzurufenden Wert auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a3c46-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="a3c46-115">Ein Großteil der Arbeit mit **Medien** Objekten umfasst Metadaten zum Inhalt des Medien Elements, die als Attribute bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a3c46-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="a3c46-116">Das Thema [Medien Element Attribute](media-item-attributes.md) beschreibt das Lesen und Ändern von Attributwerten.</span><span class="sxs-lookup"><span data-stu-id="a3c46-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="a3c46-117">Weitere Informationen zu den Attributen und deren Verwendung finden Sie in den [Richtlinien zur Verwendung von Windows Media-Metadaten](/previous-versions/ms867702(v=msdn.10)) auf der Microsoft-Website.</span><span class="sxs-lookup"><span data-stu-id="a3c46-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="a3c46-118">Das **Medien** Objekt verfügt über Eigenschaften und Methoden, die einige Attribute direkt abrufen, z. b. den Namen oder die Dauer des Elements.</span><span class="sxs-lookup"><span data-stu-id="a3c46-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="a3c46-119">Bei Videoelementen können Sie die Höhe und Breite des Bilds abrufen und Markerinformationen auf Grundlage des Namens oder Indexes eines Markers abrufen.</span><span class="sxs-lookup"><span data-stu-id="a3c46-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="a3c46-120">Sie können auch bestimmen, ob ein bestimmtes Medien Element in einer bestimmten Wiedergabeliste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a3c46-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="a3c46-121">Abrufen eines Medien Objekts</span><span class="sxs-lookup"><span data-stu-id="a3c46-121">Retrieving a Media Object</span></span>

<span data-ttu-id="a3c46-122">Sie können schnell auf das aktuelle Medien Element zugreifen, indem Sie den *Player* verwenden. **currentMedia** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a3c46-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="a3c46-123">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="a3c46-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="a3c46-124">Im folgenden c#-Beispiel wird ein **Medien** Objekt abgerufen, das das aktuelle Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3c46-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="a3c46-125">Mithilfe des *Players* können Sie ein neues Medien Element aus einer digitalen Mediendatei erstellen. **newmedia** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3c46-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="a3c46-126">Sie übergeben die-Methode den URL-Pfad an eine digitale Mediendatei und geben einen Verweis auf das neue **Medien** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a3c46-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="a3c46-127">Die-Methode fügt das neue-Objekt nicht direkt der Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3c46-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="a3c46-128">Sie können das Objekt jedoch an die *Wiedergabeliste* übergeben. **appendItem** -Methode oder die *Wiedergabeliste*. **InsertItem** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3c46-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="a3c46-129">Im folgenden c#-Beispiel wird ein **Medien** Objekt erstellt, das auf einem der Digital Media-Beispiele basiert, das mit dem Windows Media Player SDK installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a3c46-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="a3c46-130">Sie müssen zwei umgekehrte Schrägstriche ( \) oder das @-Zeichen in c#) in einer Zeichenfolge einschließen, um einen tatsächlichen umgekehrten Schrägstrich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="a3c46-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="a3c46-131">Dies liegt daran, dass c# einen einzelnen umgekehrten Schrägstrich zum Definieren einer Escapesequenz verwendet.</span><span class="sxs-lookup"><span data-stu-id="a3c46-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="a3c46-132">Sie können ein neues Medien Element aus einer digitalen Mediendatei erstellen und es der Bibliothek in einem Schritt mithilfe von *mediacollection* hinzufügen. Methode **Hinzufügen** .</span><span class="sxs-lookup"><span data-stu-id="a3c46-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="a3c46-133">Wie der *Player*. **newmedia** -Methode, die **Add** -Methode nimmt einen Pfad zu einer digitalen Mediendatei an.</span><span class="sxs-lookup"><span data-stu-id="a3c46-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="a3c46-134">Im folgenden c#-Beispiel wird ein **Medien** Objekt erstellt, das auf einer der SDK-Beispieldateien basiert, und dieses Objekt wird der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a3c46-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="a3c46-135">Mithilfe der *Wiedergabeliste* können Sie ein **Medien** Objekt abrufen, das ein Medien Element in einer Wiedergabeliste darstellt. **Item** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a3c46-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="a3c46-136">Im folgenden c#-Beispiel wird das sechste Medien Element aus der aktuellen Wiedergabeliste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3c46-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="a3c46-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3c46-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3c46-138">**Controls. happtitem**</span><span class="sxs-lookup"><span data-stu-id="a3c46-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="a3c46-139">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="a3c46-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="a3c46-140">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="a3c46-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a3c46-141">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="a3c46-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="a3c46-142">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="a3c46-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="a3c46-143">**Player. newmedia**</span><span class="sxs-lookup"><span data-stu-id="a3c46-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="a3c46-144">**Wiedergabeliste. Element**</span><span class="sxs-lookup"><span data-stu-id="a3c46-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="a3c46-145">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="a3c46-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




