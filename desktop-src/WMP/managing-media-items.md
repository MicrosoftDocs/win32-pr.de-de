---
title: Verwalten von Medienelementen
description: Verwalten von Medienelementen
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player,Bibliothek
- Windows Media Player-Objektmodell, Bibliothek
- Objektmodell,Bibliothek
- Windows Media Player Mobile,Bibliothek für Objektmodell
- Windows Media Player ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Bibliothek für Objektmodell
- ActiveX-Steuerelement, Bibliothek für Objektmodell
- Windows Media Player bibliothek,Verwalten von Medienelementen
- Bibliothek,Verwalten von Medienelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386889"
---
# <a name="managing-media-items"></a><span data-ttu-id="3401f-112">Verwalten von Medienelementen</span><span class="sxs-lookup"><span data-stu-id="3401f-112">Managing Media Items</span></span>

<span data-ttu-id="3401f-113">Ein **Medienobjekt** stellt ein Medienelement dar.</span><span class="sxs-lookup"><span data-stu-id="3401f-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="3401f-114">Sie verfügt über Eigenschaften und Methoden, mit deren Hilfe Sie Informationen abrufen und dem Benutzer anzeigen können, oder um basierend auf dem abgerufenen Wert unterschiedliche Aktionen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3401f-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="3401f-115">Ein Großteil Ihrer Arbeit mit **Medienobjekten** umfasst Metadaten zum Inhalt des Medienelements, die als Attribute bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3401f-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="3401f-116">Im Thema [Media Item Attributes (Medienelementattribute)](media-item-attributes.md) wird beschrieben, wie Attributwerte gelesen und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3401f-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="3401f-117">Weitere Informationen zu den Attributen und deren Verwendung finden Sie zusätzlich zu diesem Thema in den Richtlinien zur Verwendung von [Windows-Medienmetadaten](/previous-versions/ms867702(v=msdn.10)) auf der Microsoft-Website.</span><span class="sxs-lookup"><span data-stu-id="3401f-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="3401f-118">Das **Media-Objekt** verfügt über Eigenschaften und Methoden, die einige Attribute direkt abrufen, z. B. den Namen oder die Dauer des Elements.</span><span class="sxs-lookup"><span data-stu-id="3401f-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="3401f-119">Für Videoelemente können Sie die Höhe und Breite des Bilds und Markerinformationen basierend auf dem Namen oder Index eines Markers abrufen.</span><span class="sxs-lookup"><span data-stu-id="3401f-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="3401f-120">Sie können auch bestimmen, ob ein bestimmtes Medienelement in einer bestimmten Wiedergabeliste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3401f-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="3401f-121">Abrufen eines Medienobjekts</span><span class="sxs-lookup"><span data-stu-id="3401f-121">Retrieving a Media Object</span></span>

<span data-ttu-id="3401f-122">Mit dem *Player* können Sie schnell auf das aktuelle Medienelement zugreifen. **currentMedia-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="3401f-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="3401f-123">In diesem Thema wurde das **Player-Objekt** wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3401f-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="3401f-124">Im folgenden C#-Beispiel wird ein **Media-Objekt** abgerufen, das das aktuelle Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="3401f-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="3401f-125">Sie können ein neues Medienelement aus einer digitalen Mediendatei erstellen, indem Sie *player* verwenden. **newMedia-Methode.**</span><span class="sxs-lookup"><span data-stu-id="3401f-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="3401f-126">Sie übergeben die -Methode den URL-Pfad an eine digitale Mediendatei und geben einen Verweis auf das neue **Medienobjekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="3401f-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="3401f-127">Die -Methode fügt das neue -Objekt der Bibliothek nicht direkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="3401f-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="3401f-128">Sie können das Objekt jedoch an die *Wiedergabeliste* übergeben. **appendItem-Methode** oder *wiedergabeliste*. **insertItem-Methode.**</span><span class="sxs-lookup"><span data-stu-id="3401f-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="3401f-129">Im folgenden C#-Beispiel wird ein **Medienobjekt** basierend auf einem der digitalen Medienbeispiele erstellt, die mit dem Windows Media Player SDK installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="3401f-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="3401f-130">Sie müssen zwei umgekehrte Schrägstriche () in eine Zeichenfolge einschließen \\ (oder das @-Zeichen in C#) verwenden, um einen tatsächlichen umgekehrten Schrägstrich darzustellen.</span><span class="sxs-lookup"><span data-stu-id="3401f-130">You must include two backslash (\\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="3401f-131">Dies liegt daran, dass C# einen einzelnen umgekehrten Schrägstrich verwendet, um eine Escapesequenz zu definieren.</span><span class="sxs-lookup"><span data-stu-id="3401f-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="3401f-132">Sie können ein neues Medienelement aus einer digitalen Mediendatei erstellen und der Bibliothek in einem Schritt mithilfe der *MediaCollection* hinzufügen. **add-Methode.**</span><span class="sxs-lookup"><span data-stu-id="3401f-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="3401f-133">Wie der *Player*. **newMedia-Methode:** Die **add-Methode** nimmt einen Pfad zu einer digitalen Mediendatei an.</span><span class="sxs-lookup"><span data-stu-id="3401f-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="3401f-134">Im folgenden C#-Beispiel wird ein **Medienobjekt** basierend auf einer der SDK-Beispieldateien erstellt und der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3401f-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="3401f-135">Sie können ein **Medienobjekt** abrufen, das ein Medienelement in einer Wiedergabeliste darstellt, indem Sie die *Wiedergabeliste* verwenden. **item-Methode.**</span><span class="sxs-lookup"><span data-stu-id="3401f-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="3401f-136">Im folgenden C#-Beispiel wird das sechste Medienelement aus der aktuellen Wiedergabeliste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3401f-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="3401f-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3401f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3401f-138">**Controls.currentItem**</span><span class="sxs-lookup"><span data-stu-id="3401f-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="3401f-139">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="3401f-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="3401f-140">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="3401f-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3401f-141">**MediaCollection.add**</span><span class="sxs-lookup"><span data-stu-id="3401f-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="3401f-142">**Player.currentMedia**</span><span class="sxs-lookup"><span data-stu-id="3401f-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="3401f-143">**Player.newMedia**</span><span class="sxs-lookup"><span data-stu-id="3401f-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="3401f-144">**Playlist.item**</span><span class="sxs-lookup"><span data-stu-id="3401f-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="3401f-145">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="3401f-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




