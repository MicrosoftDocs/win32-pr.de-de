---
title: Wiedergabelisten und Medienelemente
description: Wiedergabelisten und Medienelemente
ms.assetid: 281c744d-380e-4200-8585-a3f378bc1c36
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, Medienelemente
- Metadatei-Wiedergabelisten, Medienelemente
- Windows Media Metadatei-Wiedergabelisten, Medienelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4716a8ce07e7b0ec8348ce1a6981e23291335e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947571"
---
# <a name="playlists-and-media-items"></a><span data-ttu-id="e5867-113">Wiedergabelisten und Medienelemente</span><span class="sxs-lookup"><span data-stu-id="e5867-113">Playlists and Media Items</span></span>

<span data-ttu-id="e5867-114">Eine Wiedergabeliste ist ein Satz von Medien Elementen.</span><span class="sxs-lookup"><span data-stu-id="e5867-114">A playlist is a set of media items.</span></span> <span data-ttu-id="e5867-115">Ein **Wiedergabe** Listen Objekt kann die **Medien** Objekte, die diese Elemente darstellen, bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e5867-115">A **Playlist** object can manipulate the **Media** objects that represent those items.</span></span>

## <a name="retrieving-media-items"></a><span data-ttu-id="e5867-116">Abrufen von Medien Elementen</span><span class="sxs-lookup"><span data-stu-id="e5867-116">Retrieving Media Items</span></span>

<span data-ttu-id="e5867-117">Eine vorhandene Wiedergabeliste finden Sie in der *Wiedergabeliste*. **count** -Eigenschaft, um zu bestimmen, wie viele Medienelemente in der Wiedergabeliste angezeigt werden, und Sie können einen Verweis auf das **Medien** Objekt, das einem bestimmten Element entspricht, mithilfe der *Wiedergabeliste* erhalten. **Item** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e5867-117">For an existing playlist, you can read the *Playlist*.**count** property to determine how many media items are in the playlist, and you can get a reference to the **Media** object corresponding to a specific item using the *Playlist*.**item** property.</span></span>

<span data-ttu-id="e5867-118">Im folgenden c#-Beispiel wird ein Objekt Verweis auf ein bestimmtes Medien Element abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e5867-118">The following C# example retrieves an object reference to a specific media item.</span></span> <span data-ttu-id="e5867-119">(In diesem Thema ist die Variable *plist* ein Verweis auf ein **Wiedergabe** Listen Objekt.)</span><span class="sxs-lookup"><span data-stu-id="e5867-119">(Throughout this topic, the variable *pList* is a reference to a **Playlist** object.)</span></span>


```C++
currMedia = pList.Item(0);

```



<span data-ttu-id="e5867-120">Im folgenden c#-Beispiel werden die Namen aller Medienelemente in einer Wiedergabeliste abgerufen und in ein ListBox-Element mit dem Namen "lstoutput" eingefügt.</span><span class="sxs-lookup"><span data-stu-id="e5867-120">The following C# example retrieves the names of all the media items in a playlist and puts them in a ListBox named lstOutput.</span></span>


```C++
for (j=0; j < pList.count; j++)
{
    strItemName = pList.get_Item(j).name;
    lstOutput.Items.Add(strItemName);
}

```



## <a name="adding-items-to-a-playlist"></a><span data-ttu-id="e5867-121">Hinzufügen von Elementen zu einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="e5867-121">Adding Items to a Playlist</span></span>

<span data-ttu-id="e5867-122">Sie können ein Medien Element am Ende einer Wiedergabeliste oder an einer bestimmten Position in einer Wiedergabeliste mit der *Wiedergabeliste* hinzufügen. **appendItem** und *Wiedergabeliste*. **InsertItem** -Methoden.</span><span class="sxs-lookup"><span data-stu-id="e5867-122">You can add a media item to the end of a playlist or at a specific position in a playlist, using the *Playlist*.**appendItem** and *Playlist*.**insertItem** methods.</span></span>

<span data-ttu-id="e5867-123">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="e5867-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="e5867-124">Im folgenden c#-Beispiel werden beide Verfahren veranschaulicht, indem das aktuelle Medien Element einer Wiedergabeliste mit dem Namen "bluestest" hinzugefügt wird, zuerst am Ende und dann am Anfang der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="e5867-124">The following C# example demonstrates both techniques by adding the current media item to a playlist named "BluesTest", first at the end and then at the beginning of the playlist.</span></span>


```C++
IWMPPlaylistCollection pListColl;
IWMPPlaylistArray pListArray;
IWMPPlaylist pList;

// Initialize the Media object
IWMPMedia currMedia = Player.currentMedia;

if(currMedia != null)
{
    // Retrieve the playlist collection
    pListColl = Player.playlistCollection;

    // Retrieve a playlist array containing
    // playlists named BluesTest
    pListArray = pListColl.getByName("BluesTest");

    // Retrieve the first element with this name from the
    // array.
    pList = pListArray.Item(0);

    // Add the current item to the end, and then, the beginning
    // of the specified playlist.
    pList.appendItem(currMedia);
    pList.insertItem(0, currMedia);
}

```



<span data-ttu-id="e5867-125">Beim Erstellen einer neuen, leeren Wiedergabeliste mit *playlistcollection*. **newwiedergabe** -Methode: Sie können Medienelemente hinzufügen, indem Sie die *Wiedergabeliste* wiederholt aufrufen. **appendItem** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e5867-125">When you create a new, empty playlist by using the *PlaylistCollection*.**newPlaylist** method, you can add media items to it by repeatedly calling the *Playlist*.**appendItem** method.</span></span>

## <a name="manipulating-media-items-in-a-playlist"></a><span data-ttu-id="e5867-126">Bearbeiten von Medien Elementen in einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="e5867-126">Manipulating Media Items in a Playlist</span></span>

<span data-ttu-id="e5867-127">Mithilfe der *Wiedergabeliste* können Sie die Position eines Medien Elements in der Wiedergabeliste ändern. " **muveitem** "-Methode.</span><span class="sxs-lookup"><span data-stu-id="e5867-127">You can change the position of a media item in the playlist by using the *Playlist*.**moveItem** method.</span></span> <span data-ttu-id="e5867-128">Geben Sie das Element anhand seines aktuellen Indexes an, und geben Sie dann den neuen Index an.</span><span class="sxs-lookup"><span data-stu-id="e5867-128">You specify the item by its current index, and then you specify the new index.</span></span> <span data-ttu-id="e5867-129">Im folgenden c#-Beispiel wird ein Element in einer Wiedergabeliste von Index 5 in Index 0 verschoben.</span><span class="sxs-lookup"><span data-stu-id="e5867-129">The following C# example moves an item from index 5 to index 0 within a playlist.</span></span>


```C++
// Move the 6th item to the beginning
// of the specified playlist.
pList.moveItem(5, 0);

```



<span data-ttu-id="e5867-130">Sie können ein Medien Element mithilfe der **Wiedergabeliste** aus der Wiedergabeliste entfernen. **RemoveItem** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e5867-130">You can remove a media item from the playlist by using the **Playlist**.**removeItem** method.</span></span> <span data-ttu-id="e5867-131">Beachten Sie, dass die Indexwerte der nachfolgenden Elemente geändert werden, wenn es sich bei dem entfernten Element nicht um das letzte Element in der Wiedergabeliste handelt.</span><span class="sxs-lookup"><span data-stu-id="e5867-131">Note that if the removed item was not the final item in the playlist, the index values of the subsequent items change.</span></span> <span data-ttu-id="e5867-132">Im folgenden c#-Beispiel wird das angegebene Element entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5867-132">The following C# example removes the specified item.</span></span>


```C++
// Remove the currently playing item from the
// specified playlist.
pList.removeItem(currMedia);

```



> [!Note]  
> <span data-ttu-id="e5867-133">Benutzer können den Inhalt einer Wiedergabeliste außerhalb Ihrer Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="e5867-133">Users can change the contents of a playlist outside of your application.</span></span> <span data-ttu-id="e5867-134">Wenn Sie die Elemente in einer Wiedergabeliste bearbeiten, sollten Sie die Wiedergabelisten bezogenen Ereignisse des Windows Media Player-Steuer Elements überwachen und behandeln, um sicherzustellen, dass der Code ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e5867-134">Whenever you manipulate the items in a playlist, you should monitor and handle the playlist-related events of the Windows Media Player control to ensure that your code works correctly.</span></span> <span data-ttu-id="e5867-135">Diese Ereignisse sind *Player*. **Currentplaylistchange** und *Player*. **Playlistchange**.</span><span class="sxs-lookup"><span data-stu-id="e5867-135">These events are *Player*.**CurrentPlaylistChange** and *Player*.**PlaylistChange**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e5867-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5867-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5867-137">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="e5867-137">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="e5867-138">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="e5867-138">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e5867-139">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="e5867-139">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




