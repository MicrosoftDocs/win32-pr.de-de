---
title: Verwenden des Objektmodells Windows Media Player 7 oder höher
description: Verwenden des Objektmodells Windows Media Player 7 oder höher
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, Objektmodell
- Windows Media Player-Objektmodell, Version 7 oder höher
- Objektmodell, Version 7 oder höher
- Windows Media Player ActiveX-Steuerelement, Version 7 oder höher
- ActiveX-Steuerelement, Version 7 oder höher
- Windows Media Player Mobile ActiveX-Steuerelement, Version 7 oder höher
- Windows Media Player Mobile, Objektmodell
- Migrations Handbuch, Version 7 oder höher
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310395"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="33ff7-112">Verwenden des Objektmodells Windows Media Player 7 oder höher</span><span class="sxs-lookup"><span data-stu-id="33ff7-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="33ff7-113">Die meisten Aufgaben, die Sie möglicherweise mit dem Windows Media Player 6,4-ActiveX-Steuerelement Objektmodell durchgeführt haben, erfordern einen neuen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="33ff7-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="33ff7-114">In vielen Fällen haben sich die Namen der Eigenschaften, Methoden und Ereignisse im Objektmodell Windows Media Player 7 oder höher geändert.</span><span class="sxs-lookup"><span data-stu-id="33ff7-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="33ff7-115">Um beispielsweise den Dateipfad im Objektmodell der Version 6,4 anzugeben, legen Sie die **Player6. filename** -Eigenschaft fest:</span><span class="sxs-lookup"><span data-stu-id="33ff7-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="33ff7-116">Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, müssen Sie die Eigenschaft **Player. URL** festlegen:</span><span class="sxs-lookup"><span data-stu-id="33ff7-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="33ff7-117">Alternativ können Sie das 10-Objektmodell verwenden, indem Sie ein **Medien** Objekt aus der Bibliothek abrufen und dann die Eigenschaft **Player. currentMedia** festlegen:</span><span class="sxs-lookup"><span data-stu-id="33ff7-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="33ff7-118">Der Zugriff auf einen Großteil der Funktionen des Objektmodells Windows Media Player 7 oder höher erfolgt über die Objekthierarchie.</span><span class="sxs-lookup"><span data-stu-id="33ff7-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="33ff7-119">Wie im vorherigen Beispiel gezeigt, können Sie ein **Wiedergabe** Listen Objekt mithilfe der **GetAll** -Methode des **mediacollection** -Objekts abrufen, auf das über das root **Player** -Objekt zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="33ff7-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="33ff7-120">Sie können dann mithilfe der **Item** -Methode des **Wiedergabe** Listen Objekts ein bestimmtes **Medien** Objekt aus dem **Wiedergabe** Listen Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="33ff7-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="33ff7-121">Es gibt fünf zusätzliche Methoden, auf die über das **mediacollection** -Objekt zugegriffen werden kann, die ein **Wiedergabe** Listen Objekt zurückgeben mit jeder Methode können Sie das Objekt auf der Grundlage spezifischer Kriterien abrufen, z. b. Genre oder Album.</span><span class="sxs-lookup"><span data-stu-id="33ff7-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="33ff7-122">Die hierarchische Struktur des ActiveX-Steuerelement Objektmodells Windows Media Player 7 oder höher bietet einen logischeren Ansatz zum Organisieren der Eigenschaften, Methoden und Ereignisse, die für ihre Verwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="33ff7-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="33ff7-123">Alle Funktionen für die Player-Steuerelemente sind im Steuer **Element Objekt enthalten** , die gesamte Funktionalität für die Player-Netzwerkverbindung ist im **Netzwerk** Objekt enthalten usw.</span><span class="sxs-lookup"><span data-stu-id="33ff7-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="33ff7-124">Um beispielsweise die Wiedergabe von Inhalten mit dem Objektmodell der Version 6,4 zu starten, verwenden Sie die **Player6. Play** -Methode:</span><span class="sxs-lookup"><span data-stu-id="33ff7-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="33ff7-125">Wenn Sie das Objektmodell Windows Media Player 7 oder höher verwenden, müssen Sie über das Steuerelement **-Objekt auf** die **Play** -Methode zugreifen:</span><span class="sxs-lookup"><span data-stu-id="33ff7-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="33ff7-126">Die Tiefe des Objektmodells kann jedoch zu sehr langen Skript Anweisungen führen:</span><span class="sxs-lookup"><span data-stu-id="33ff7-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="33ff7-127">Anweisungen wie die vorherige können viel einfacher und lesbarer werden, indem Sie mit einzelnen benannten Objekten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="33ff7-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="33ff7-128">Im folgenden Beispiel wird die vorherige Code Anweisung durch Syntax unter Verwendung separater Objektvariablen ersetzt:</span><span class="sxs-lookup"><span data-stu-id="33ff7-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



<span data-ttu-id="33ff7-129">Dieser Codierungsstil erfordert mehr Skript Zeilen, ist jedoch viel leichter zu befolgen, insbesondere mit den hinzugefügten Kommentaren.</span><span class="sxs-lookup"><span data-stu-id="33ff7-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="33ff7-130">Es gibt einen weiteren Vorteil: das **currentwiedergabe** -Objekt ist leicht wiederzuverwenden, da es in der Variablen "pl" gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="33ff7-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="33ff7-131">Viele der Eigenschaften, Methoden und Ereignisse im Objektmodell Windows Media Player 7 oder höher legen unterschiedliche Werte fest oder rufen Werte eines anderen Typs oder einer anderen Zahl ab, und zwar im Vergleich zu den entsprechenden Funktionen im Objektmodell der Version 6,4.</span><span class="sxs-lookup"><span data-stu-id="33ff7-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="33ff7-132">Wenn **Player6. openstate** beispielsweise 2 abruft, entspricht dieser Wert der Visual Basic Konstante **nsloadingnsc**. Dies bedeutet, dass der Spieler eine Stations Datei mit der Dateinamenerweiterung ". NSC" lädt.</span><span class="sxs-lookup"><span data-stu-id="33ff7-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="33ff7-133">Wenn jedoch die Eigenschaften **Player. openstate** von Windows Media Player 7 oder höher den objektmodelltyp 2 abruft, entspricht dieser Wert dem Status playlistlocate, d. h., Windows Media Player versucht, eine Wiedergabeliste zu finden.</span><span class="sxs-lookup"><span data-stu-id="33ff7-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="33ff7-134">Darüber hinaus können mit der **Player6. openstate** -Eigenschaft sieben verschiedene Werte abgerufen werden, während die Windows Media Player 7-oder spätere **Player. openstate** -Eigenschaft 22 verschiedene Werte abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="33ff7-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="33ff7-135">Achten Sie darauf, dass Sie im Abschnitt "Objektmodell Referenz für Skripterstellung" des Windows Media Player SDK nach dem Überarbeiten von Code für die Verwendung einer anderen Objektmodell Version darauf verweisen.</span><span class="sxs-lookup"><span data-stu-id="33ff7-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33ff7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33ff7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33ff7-137">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="33ff7-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="33ff7-138">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="33ff7-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="33ff7-139">**Handbuch für die Migration des Objektmodells**</span><span class="sxs-lookup"><span data-stu-id="33ff7-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




