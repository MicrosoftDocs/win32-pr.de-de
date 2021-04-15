---
title: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
description: Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player Online Stores, automatische Wiedergabelisten
- Online Stores, automatische Wiedergabelisten
- Typ 1 Online Stores, automatische Wiedergabelisten
- Typ 2 Online Stores, automatische Wiedergabelisten
- Windows Media Player Online Stores, organisieren von Bibliotheks Inhalten
- Online Stores, organisieren von Bibliotheks Inhalten
- Geben Sie 1 Online Stores ein, organisieren Sie Bibliotheksinhalte.
- Typ 2 Online Stores, organisieren von Bibliotheksinhalt
- Windows Media Player Online Stores, organisieren von Bibliotheks Inhalten
- Online Stores, organisieren von Bibliotheks Inhalten
- Typ 1 Online Stores, Bibliothek Inhalt organisieren
- Typ 2 Online Stores, Bibliothek Inhalt organisieren
- Bibliothek, organisieren von Inhalten
- Organisieren von Bibliotheksinhalt
- automatische Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa53a4b9f56a8aa6425f137ef4a8c43bd8ed1454
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515866"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a><span data-ttu-id="a4275-118">Verwenden von automatischen Wiedergabelisten zum Organisieren von Inhalten in der Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4275-118">Using Auto Playlists to Organize Content in the Library</span></span>

<span data-ttu-id="a4275-119">Sie können automatische Wiedergabelisten verwenden, um von Ihnen bereitgestellte Premium-Inhalte zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="a4275-119">You can use auto playlists to organize premium content you provide.</span></span> <span data-ttu-id="a4275-120">Beispielsweise können Sie mit Windows Media Player eine automatische Wiedergabeliste erstellen, die nur Inhalte enthält, die Sie mit einer Benutzer Bewertung von mindestens vier Sternen angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="a4275-120">For example, you could use Windows Media Player to create an auto playlist that contains only content you provided having a user rating of at least four stars.</span></span> <span data-ttu-id="a4275-121">Anschließend können Sie die automatische Wiedergabeliste der Bibliothek in Windows Media Player hinzufügen, sodass Sie im Knoten "erworbene Musik" unter Ihrem Inhalts Verteilerknoten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4275-121">You can then add the auto playlist to the library in Windows Media Player so that it displays in the Purchased Music node under your content distributor node.</span></span>

<span data-ttu-id="a4275-122">Gehen Sie hierzu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="a4275-122">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="a4275-123">Erstellen Sie die automatische Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="a4275-123">Create the auto playlist.</span></span>
2.  <span data-ttu-id="a4275-124">Navigieren Sie in Windows-Explorer zur automatischen Wiedergabeliste, und rufen Sie die WPL-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="a4275-124">Using Windows Explorer, browse to the auto playlist and retrieve the .wpl file.</span></span>
3.  <span data-ttu-id="a4275-125">Fügen Sie der Bibliothek mithilfe des Windows Media Player-Objektmodells die automatische Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4275-125">Using the Windows Media Player object model, add the auto playlist to the library.</span></span>
4.  <span data-ttu-id="a4275-126">Legen Sie das **WM/contentdistributor-** Attribut für die Wiedergabeliste auf den Schlüsselnamen ihres Inhalts Verteilers fest.</span><span class="sxs-lookup"><span data-stu-id="a4275-126">Set the **WM/ContentDistributor** attribute for the playlist to your content distributor key name.</span></span>
5.  <span data-ttu-id="a4275-127">Legen Sie das **synattribute** -Attribut für die Wiedergabeliste auf true fest.</span><span class="sxs-lookup"><span data-stu-id="a4275-127">Set the **SyncOnly** attribute for the playlist to true.</span></span>

<span data-ttu-id="a4275-128">Der folgende JScript-Beispielcode zeigt eine Funktion, die dem Proseware-Knoten in der Bibliothek eine automatische Wiedergabeliste mit dem Namen "Favoriten Treffer" hinzufügt:</span><span class="sxs-lookup"><span data-stu-id="a4275-128">The following JScript example code shows a function that adds an auto playlist named "Favorite Hits" to the Proseware node in the library:</span></span>


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a><span data-ttu-id="a4275-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4275-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4275-130">Informationen zur Bibliotheks Integration</span><span class="sxs-lookup"><span data-stu-id="a4275-130">About Library Integration</span></span>](download-manager-overview.md)
</dt> <dt>

[<span data-ttu-id="a4275-131">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="a4275-131">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a4275-132">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="a4275-132">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="a4275-133">**Wiedergabeliste. Einstellungs Element**</span><span class="sxs-lookup"><span data-stu-id="a4275-133">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a4275-134">**Statische und automatische Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="a4275-134">**Static and Auto Playlists**</span></span>](static-and-auto-playlists.md)
</dt> <dt>

[<span data-ttu-id="a4275-135">**Synkonstante-Attribut**</span><span class="sxs-lookup"><span data-stu-id="a4275-135">**SyncOnly Attribute**</span></span>](synconly-attribute.md)
</dt> <dt>

[<span data-ttu-id="a4275-136">**WM-/contentverteilungs-Attribut**</span><span class="sxs-lookup"><span data-stu-id="a4275-136">**WM/ContentDistributor Attribute**</span></span>](wm-contentdistributor-attribute.md)
</dt> <dt>

[<span data-ttu-id="a4275-137">**Arbeiten mit der Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="a4275-137">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




