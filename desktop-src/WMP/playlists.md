---
title: Wiedergabelisten
description: Wiedergabelisten
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, Wiedergabelisten
- Windows Media Player-Objektmodell, Wiedergabelisten
- Objektmodell, Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten
- ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten
- Windows Media Player Mobile, Wiedergabelisten
- Wiedergabelisten, Migration
- Windows Media Metadatei-Wiedergabelisten, Migration
- Metadatei-Wiedergabelisten, Migration
- Migrations Handbuch, Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036695"
---
# <a name="playlists"></a><span data-ttu-id="fe51c-114">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="fe51c-114">Playlists</span></span>

<span data-ttu-id="fe51c-115">Das Windows Media Player 6,4-ActiveX-Steuerelement-Objektmodell enthält vier Methoden und eine Eigenschaft zum Arbeiten mit Windows Media Metadatei-Wiedergabelisten:</span><span class="sxs-lookup"><span data-stu-id="fe51c-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="fe51c-116">*Player6*. **Getcurrententry**</span><span class="sxs-lookup"><span data-stu-id="fe51c-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="fe51c-117">*Player6*. **Setcurrententry**</span><span class="sxs-lookup"><span data-stu-id="fe51c-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="fe51c-118">*Player6*. **Getmediaparameter**</span><span class="sxs-lookup"><span data-stu-id="fe51c-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="fe51c-119">*Player6*. **Getmediaparametername**</span><span class="sxs-lookup"><span data-stu-id="fe51c-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="fe51c-120">*Player6*. **Entrycount**.</span><span class="sxs-lookup"><span data-stu-id="fe51c-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="fe51c-121">Diese bieten eine begrenzte Funktionalität zum Navigieren in einer Wiedergabelisten-Metadatei mit der Dateinamenerweiterung. ASX und zum Abrufen von Informationen zu den Einträgen, die in der Wiedergabeliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fe51c-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="fe51c-122">In Windows Media Player 7 wurde "Medienbibliothek" eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fe51c-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="fe51c-123">Die Bibliothek ermöglicht es Benutzern, Ihre digitalen Medieninhalte zu organisieren und benutzerdefinierte Wiedergabelisten zu erstellen, die von der grafischen Benutzeroberfläche des Players verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="fe51c-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="fe51c-124">Das ActiveX-Steuerelement Objektmodell von Windows Media Player 7 oder höher bietet Unterstützung für die Arbeit mit Bibliotheks Wiedergabelisten sowie die in Windows Media-Metadateien mit der Dateinamenerweiterung ". asx" enthaltenen Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="fe51c-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="fe51c-125">Aus Sicherheitsgründen muss der Benutzer die Zugriffsrechte für die Bibliothek erteilen, bevor das Programm seinen Inhalt bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="fe51c-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="fe51c-126">Zugriffsrechte können nur über das Windows Media Player 9-oder spätere Objektmodell angefordert und erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fe51c-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="fe51c-127">Weitere Informationen zu Zugriffsrechten finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fe51c-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="fe51c-128">Das Objektmodell Windows Media Player 7 oder höher enthält drei Objekte zum Verarbeiten von Wiedergabelisten.</span><span class="sxs-lookup"><span data-stu-id="fe51c-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="fe51c-129">Das **playlistcollection** -Objekt stellt Funktionen zum Organisieren von Wiedergabelisten bereit. Er stellt die gesamte Auflistung von Wiedergabelisten in der Bibliothek des Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="fe51c-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="fe51c-130">Das **playlistarray** -Objekt bietet eine Möglichkeit zum Abrufen einer bestimmten Wiedergabeliste aus dem **playlistcollection** -Objekt mithilfe einer Indexnummer. zwei der **playlistcollection** -Objektmethoden rufen ein **playlistarray** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="fe51c-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="fe51c-131">Das **Wiedergabe** Listen Objekt stellt die Eigenschaften und Methoden bereit, die zum Bearbeiten von in einer einzelnen Wiedergabeliste enthaltenen Medien Elementen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fe51c-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="fe51c-132">Da jede Wiedergabeliste in der Bibliothek z. b. einen eindeutigen Namen hat, können Sie mithilfe von *playlistcollection* eine Wiedergabeliste aus der Bibliothek abrufen. **getByName** -Methode:</span><span class="sxs-lookup"><span data-stu-id="fe51c-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



<span data-ttu-id="fe51c-133">Am häufigsten möchten Sie mit der aktuellen Wiedergabeliste arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe51c-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="fe51c-134">Obwohl es möglich ist, mehrere Wiedergabelisten Objekte zu verwenden, kann nur eine vom *Player* abgerufen werden. **currentwiedergabe** -Eigenschaft zu einem beliebigen Zeitpunkt: der, den Windows Media Player zu diesem Zeitpunkt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fe51c-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="fe51c-135">Wenn Windows Media Player 7 oder höher eine Windows Media-Metadatei mit der Dateinamenerweiterung ". asx" wieder gibt, erstellt Sie zuerst ein **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="fe51c-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="fe51c-136">Anschließend wird das Objekt mit den Informationen aus der. ASX-Wiedergabeliste gefüllt, und dieses **Wiedergabe** Listen Objekt wird zur aktuellen Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="fe51c-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="fe51c-137">Dies bedeutet, dass Sie die dem **Wiedergabe** Listen Objekt zugeordneten Eigenschaften und Methoden verwenden können, um. ASX-Wiedergabelisten genau so zu bearbeiten, wie Sie die Wiedergabelisten in der Bibliothek verarbeiten würden.</span><span class="sxs-lookup"><span data-stu-id="fe51c-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="fe51c-138">Um beispielsweise die Anzahl der Einträge in einer. ASX-Wiedergabeliste mit dem Objektmodell der Version 6,4 abzurufen, verwenden Sie *Player6*. **Entrycount** -Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="fe51c-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="fe51c-139">Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, verwenden Sie die *Wiedergabeliste*. **count** -Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="fe51c-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="fe51c-140">Wenn Sie das-Steuerelement der Version 6,4 verwenden, können Sie *Player6* verwenden. **Getcurrententry** -Methode zum Abrufen des Index des aktuellen Eintrags in einer. ASX-Wiedergabeliste:</span><span class="sxs-lookup"><span data-stu-id="fe51c-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="fe51c-141">Sie können das gleiche Ergebnis erzielen, indem Sie das Objektmodell Windows Media Player 7 oder höher im Skript verwenden.</span><span class="sxs-lookup"><span data-stu-id="fe51c-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="fe51c-142">Im folgenden JScript-Beispiel wird das aktuelle Medienobjekt mit jedem Element in der Wiedergabeliste verglichen.</span><span class="sxs-lookup"><span data-stu-id="fe51c-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="fe51c-143">Wenn *Medien*. **isidentical** gibt true zurück, ein Meldungs Feld zeigt den Index des aktuellen Medien Elements an.</span><span class="sxs-lookup"><span data-stu-id="fe51c-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



<span data-ttu-id="fe51c-144">Um den Index des aktuellen Eintrags in einer. ASX-Wiedergabeliste anzugeben, verwenden Sie *Player6*. **Setcurrententry**.</span><span class="sxs-lookup"><span data-stu-id="fe51c-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="fe51c-145">Wiedergabe Indizes der Wiedergabeliste in Version 6,4 beginnen mit 1. Wenn Sie also den zweiten Eintrag in einer Metadatei Wiedergabeliste des aktuellen Eintrags vornehmen möchten, verwenden Sie die folgende Syntax:</span><span class="sxs-lookup"><span data-stu-id="fe51c-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="fe51c-146">Wiedergabe Indizes für Wiedergabelisten sind in Windows Media Player 7 oder höher Null basiert; Verwenden Sie die folgende Syntax, um den zweiten Eintrag in einer Metadatei-Wiedergabeliste für die aktuelle zu verwenden, wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden:</span><span class="sxs-lookup"><span data-stu-id="fe51c-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="fe51c-147">Im folgenden JScript-Beispiel wird eine Funktion veranschaulicht, die eine Indexnummer als Parameter akzeptiert, und dann den Wiedergabelisten Eintrag, der dem Index das aktuelle Medien Element entspricht, erstellt:</span><span class="sxs-lookup"><span data-stu-id="fe51c-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



<span data-ttu-id="fe51c-148">Windows Media-Metadateien können benutzerdefinierte Parameter Elemente enthalten, die Sie mit dem- **<PARAM>** Tag angeben.</span><span class="sxs-lookup"><span data-stu-id="fe51c-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="fe51c-149">Wenn Sie das Objektmodell der Version 6,4 verwenden, können Sie den Namen eines bestimmten Parameters mit *Player6* abrufen. **Getmediaparametername** -Methode.</span><span class="sxs-lookup"><span data-stu-id="fe51c-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="fe51c-150">Im folgenden JScript-Beispiel wird der Name des ersten Parameters im ersten Eintrag einer. ASX-Wiedergabeliste abgerufen:</span><span class="sxs-lookup"><span data-stu-id="fe51c-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="fe51c-151">Auf ähnliche Weise können Sie den Wert, der dem Parameter zugeordnet ist, mithilfe von *Player6* abrufen. **Getmediaparameter**:</span><span class="sxs-lookup"><span data-stu-id="fe51c-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="fe51c-152">Im folgenden JScript-Beispiel wird das Objektmodell Windows Media Player 7 oder höher verwendet, um den Parameternamen und den Wert aus dem ersten Eintrag in einer. ASX-Wiedergabeliste abzurufen:</span><span class="sxs-lookup"><span data-stu-id="fe51c-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



<span data-ttu-id="fe51c-153">Sie können den *playlistcollection*-Befehl verwenden. **importwiedergabe** -Methode, um der Bibliothek eine. ASX-Wiedergabeliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="fe51c-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="fe51c-154">Nach dem Importieren wird die Metadatei-Wiedergabeliste zu einer Bibliotheks Wiedergabeliste, sodass Sie Sie mit allen Eigenschaften und Methoden, die Sie zur Verfügung stellen, bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="fe51c-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="fe51c-155">Der Benutzer muss Vollzugriff auf die Bibliothek gewähren, damit Ihre Anwendung die **importwiedergabe** -Methode verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="fe51c-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="fe51c-156">Sie können *playlistcollection* verwenden. **getByName** , um zu testen, ob eine Wiedergabeliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="fe51c-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="fe51c-157">Diese Methode gibt immer ein gültiges **playlistarray** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="fe51c-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="fe51c-158">Wenn das abgerufene Wiedergabelisten Array genau eine Wiedergabeliste enthält, ist eine Wiedergabeliste mit diesem Namen in der Bibliothek vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe51c-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="fe51c-159">Andernfalls enthält das Wiedergabelisten Array kein Wiedergabelisten Objekt. Dies bedeutet, dass keine Wiedergabeliste in der Bibliothek vorhanden ist, in der der Name als Argument an die **getByName** -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="fe51c-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="fe51c-160">Dies wird im folgenden JScript-Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="fe51c-160">The following JScript example demonstrates this:</span></span>


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a><span data-ttu-id="fe51c-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe51c-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe51c-162">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="fe51c-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="fe51c-163">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="fe51c-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="fe51c-164">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="fe51c-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




