---
title: Informationen zu mediacollection und Media Objects
description: Informationen zu mediacollection und Media Objects
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player, mediacollection-Objekt
- Windows Media Player-Objektmodell, mediacollection-Objekt
- Objektmodell, mediacollection-Objekt
- Windows Media Player ActiveX-Steuerelement, mediacollection-Objekt
- ActiveX-Steuerelement, mediacollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, mediacollection-Objekt
- Windows Media Player Mobile, mediacollection-Objekt
- Mediacollection-Objekt
- Windows Media Player, Medienobjekt
- Windows Media Player-Objektmodell, Medienobjekt
- Objektmodell, Medienobjekt
- Windows Media Player ActiveX-Steuerelement, Medienobjekt
- ActiveX-Steuerelement, Medienobjekt
- Windows Media Player Mobile ActiveX-Steuerelement, Medienobjekt
- Windows Media Player Mobile, Medienobjekt
- Medienobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340438"
---
# <a name="about-the-mediacollection-and-media-objects"></a><span data-ttu-id="7366d-119">Informationen zu mediacollection und Media Objects</span><span class="sxs-lookup"><span data-stu-id="7366d-119">About the MediaCollection and Media Objects</span></span>

<span data-ttu-id="7366d-120">**Mediacollection** und **Media** Objects steuern die Mediensammlung, in der die Speicherorte digitaler Mediendateien definiert sind, auf die Windows Media Player zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7366d-120">The **MediaCollection** and **Media** objects govern the media collection, which defines the locations of digital media files that Windows Media Player can access.</span></span> <span data-ttu-id="7366d-121">Sie erhalten das **mediacollection** -Objekt aus der **mediacollection** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7366d-121">You get the **MediaCollection** object from the **mediaCollection** property of the **Player** object.</span></span> <span data-ttu-id="7366d-122">Die **mediacollection** -Eigenschaft gibt das **mediacollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7366d-122">The **mediaCollection** property returns the **MediaCollection** object.</span></span> <span data-ttu-id="7366d-123">Sie können nur auf die Eigenschaften des **mediacollection** -Objekts zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="7366d-123">You can only access the properties of the **MediaCollection** object after you have created it.</span></span> <span data-ttu-id="7366d-124">Wenn Sie z. b. ein **Medien** Objekt (einen Song) hinzufügen möchten, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="7366d-124">For example, to add a **Media** object (a song), use the following code:</span></span>


```C++
player.mediacollection.add('laure.wma');

```



<span data-ttu-id="7366d-125">Sie haben der Mediensammlung die Datei "Laure. wma" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7366d-125">You have added the file laure.wma to the media collection.</span></span>

<span data-ttu-id="7366d-126">Sie können das aktuelle **Medien** Objekt mit der **currentMedia** -Eigenschaft des **Players** erhalten.</span><span class="sxs-lookup"><span data-stu-id="7366d-126">You can get the current **Media** object by using the **currentMedia** property of the **Player**.</span></span> <span data-ttu-id="7366d-127">Mit diesem Code wird beispielsweise die **Duration** -Eigenschaft des aktuellen **Medien** Objekts abgerufen:</span><span class="sxs-lookup"><span data-stu-id="7366d-127">For example, this code gets the **duration** property of the current **Media** object:</span></span>


```C++
myduration = player.currentmedia.duration;

```



<span data-ttu-id="7366d-128">Es gibt viele Möglichkeiten, ein **Medien** Objekt zu erhalten, sodass Sie auf seine Eigenschaften zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7366d-128">There are many ways to get a **Media** object so that you can access its properties.</span></span> <span data-ttu-id="7366d-129">Wenn Sie z. b. auf die **Duration** -Eigenschaft des aktuellen Mediums zugreifen möchten, können Sie jede der folgenden Codezeilen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7366d-129">For example, if you want to access the **duration** property of the current media, each of the following lines of code could be used.</span></span>

<span data-ttu-id="7366d-130">So erhalten Sie die Dauer der derzeit Wiedergabe Medien:</span><span class="sxs-lookup"><span data-stu-id="7366d-130">To get the duration of the currently playing media:</span></span>


```C++
player.currentMedia.duration;

```



<span data-ttu-id="7366d-131">So erhalten Sie die Dauer des aktuellen Mediums in einer Wiedergabeliste:</span><span class="sxs-lookup"><span data-stu-id="7366d-131">To get the duration of the current media in a playlist:</span></span>


```C++
player.controls.currentItem.duration;

```



<span data-ttu-id="7366d-132">So erhalten Sie die Dauer des dritten Medien Elements in einer Wiedergabeliste:</span><span class="sxs-lookup"><span data-stu-id="7366d-132">To get the duration of the third media item in a playlist:</span></span>


```C++
player.currentPlaylist.item(2).duration;

```



<span data-ttu-id="7366d-133">So erhalten Sie die Dauer des dritten Medien Elements in einem "Jazz"-Genre:</span><span class="sxs-lookup"><span data-stu-id="7366d-133">To get the duration of the third media item in a "Jazz" genre:</span></span>


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



<span data-ttu-id="7366d-134">So erhalten Sie die Dauer des dritten Medien Elements in der zweiten Wiedergabeliste:</span><span class="sxs-lookup"><span data-stu-id="7366d-134">To get the duration of the third media item in the second playlist:</span></span>


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a><span data-ttu-id="7366d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7366d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7366d-136">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="7366d-136">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7366d-137">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7366d-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7366d-138">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="7366d-138">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




