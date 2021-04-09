---
title: Wiedergabelisten Attribute
description: Wiedergabelisten Attribute
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Wiedergabelisten, Attribute
- Metadatei-Wiedergabelisten, Attribute
- Windows Media Metadatei-Wiedergabelisten, Attribute
- Attribute, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947586"
---
# <a name="playlist-attributes"></a><span data-ttu-id="fe305-114">Wiedergabelisten Attribute</span><span class="sxs-lookup"><span data-stu-id="fe305-114">Playlist Attributes</span></span>

<span data-ttu-id="fe305-115">Wiedergabelisten verfügen über Metadateninformationen, die so genannten Attribute sind, wie Medienelemente Attribute aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fe305-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="fe305-116">Sie können die Namen und Werte von Wiedergabelisten Attributen abrufen und in der Benutzeroberfläche anzeigen, oder der Code kann basierend auf dem Wert eines Attributs Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe305-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="fe305-117">Wiedergabelisten werden in Dateien definiert, die in einem XML-Format organisiert sind, und bestimmte Elemente in der Datei definieren Wiedergabelisten Attribute.</span><span class="sxs-lookup"><span data-stu-id="fe305-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="fe305-118">Einige Attribut Elemente sind gut bekannt. der Autor der Metadatei kann auch beliebige Attribute definieren.</span><span class="sxs-lookup"><span data-stu-id="fe305-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="fe305-119">Weitere Informationen zu Attribut Elementen in Wiedergabelisten Dateien finden Sie unter [Abrufen von Metadaten](retrieving-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="fe305-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="fe305-120">Die Bibliothek kann zusätzliche Wiedergabelisten Attribute wie **SourceUrl** oder **userlastplayedtime** bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fe305-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="fe305-121">Weitere Informationen zu den Wiedergabelisten Attributen der Bibliothek finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="fe305-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="fe305-122">Die *Wiedergabeliste*. **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fe305-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="fe305-123">Die *Wiedergabeliste*. **attributeName** -Eigenschaft ruft den Namen eines Attributs basierend auf seinem Index und der *Wiedergabeliste* ab. die **getiteminfo** -Methode ruft den Wert eines Attributs anhand des Namens ab.</span><span class="sxs-lookup"><span data-stu-id="fe305-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="fe305-124">Sie können den Wert eines Attributs der aktuellen Wiedergabeliste mit der *Wiedergabeliste* ändern. die Methode " **stiteminfo** ".</span><span class="sxs-lookup"><span data-stu-id="fe305-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="fe305-125">Eine besondere Verwendung **der Methode "** Methode" ist das Sortieren der Elemente in der Wiedergabeliste mithilfe des **SortAttribute** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="fe305-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="fe305-126">Im folgenden c#-Beispiel wird eine Wiedergabeliste nach den Werten des **userlastplayedtime** -Attributs sortiert.</span><span class="sxs-lookup"><span data-stu-id="fe305-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="fe305-127">Die Variablen *Wiedergabeliste* ist ein Verweis auf ein **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe305-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="fe305-128">In diesem Thema wurde das **Player** -Objekt wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="fe305-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="fe305-129">Der folgende c#-Beispielcode veranschaulicht das Abrufen von Wiedergabelisten Attributen.</span><span class="sxs-lookup"><span data-stu-id="fe305-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="fe305-130">Die erste Funktion, showplaylists, füllt ein ListBox-Steuerelement mit den Namen der verfügbaren Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="fe305-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="fe305-131">Der zweite Teil ist der Listenfeld-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="fe305-131">The second part is the list box event handler.</span></span> <span data-ttu-id="fe305-132">Wenn der Benutzer auf einen Wiedergabelisten Namen klickt, ruft dieser Code die Attribute für die Wiedergabeliste ab und zeigt diese Attribute in einem zweiten Listenfeld an.</span><span class="sxs-lookup"><span data-stu-id="fe305-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



<span data-ttu-id="fe305-133">Das SelectedIndexChanged-Ereignis für das ListBox-Steuerelement wird jedes Mal aufgerufen, wenn der Benutzer einen Wiedergabelisten Namen auswählt.</span><span class="sxs-lookup"><span data-stu-id="fe305-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="fe305-134">Der folgende Ereignishandler füllt ein zweites Listenfeld mit den Attributnamen und den Werten aus, die der Auswahl des Benutzers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fe305-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="fe305-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe305-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe305-136">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="fe305-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="fe305-137">**Medien Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="fe305-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe305-138">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="fe305-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




