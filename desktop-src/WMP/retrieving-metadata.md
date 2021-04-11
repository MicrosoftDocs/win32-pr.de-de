---
title: Abrufen von Metadaten
description: Abrufen von Metadaten
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Media Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Wiedergabelisten, Abrufen von Metadaten
- Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Windows Media Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Wiedergabelisten, Abrufen von Metadaten
- Metadatei-Wiedergabelisten, Abrufen von Metadaten
- Metadaten, Abrufen
- Abrufen von Metadaten
- Windows Media Player, Abrufen von Metadaten
- Windows Media Player, Abrufen von Metadaten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947856"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="7cc03-113">Abrufen von Metadaten</span><span class="sxs-lookup"><span data-stu-id="7cc03-113">Retrieving Metadata</span></span>

<span data-ttu-id="7cc03-114">Während ein Show-oder Clip-Vorgang abgespielt wird, kann das Skript Metadaten wie Titel und Autor mithilfe der **getiteminfo** -Methoden der Windows-Media Player **Medien** -und **Wiedergabe** Listen Objekte abrufen.</span><span class="sxs-lookup"><span data-stu-id="7cc03-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="7cc03-115">Sie können Metadaten aus dem Bereich "ASX" mithilfe von **Wiedergabe** Listen-Objektmethoden und aus dem Eintrags Bereich mithilfe von **Medien** Objektmethoden abrufen.</span><span class="sxs-lookup"><span data-stu-id="7cc03-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="7cc03-116">Wenn Sie z. b. die Werte für "Author", "abstract" und "param" in der folgenden Datei abrufen möchten, verwenden Sie die **getiteminfo** -Methode des **Wiedergabe** Listen Objekts.</span><span class="sxs-lookup"><span data-stu-id="7cc03-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="7cc03-117">Der Attribut Name ist für diese Methode erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7cc03-117">The attribute name is required for this method.</span></span> <span data-ttu-id="7cc03-118">Attributnamen können abgerufen werden, indem die Indexnummer der **attributeName** -Eigenschaft bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7cc03-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="7cc03-119">Die verfügbaren Indizes für ein **Wiedergabe** Listen Objekt können mithilfe der **AttributeCount** -Eigenschaft abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7cc03-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="7cc03-120">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="7cc03-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="7cc03-121">Um die Werte des aktuellen **Medien** Objekts im Einstiegsbereich für Ref, Title, Copyright und param ("Three") abzurufen, verwenden Sie die **currentMedia** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="7cc03-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="7cc03-122">Verwenden Sie die **AttributeCount** -Eigenschaft des **Media** -Objekts, um die Anzahl der für das angegebene **Medien** Objekt verfügbaren Attribute zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7cc03-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="7cc03-123">Verwenden Sie Indexnummern mit der **getiteminfobyatom** -Methode, um Attributwerte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7cc03-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="7cc03-124">Verwenden Sie Indexnummern mit der **GetAttributeName** -Methode des **Media** -Objekts, um die Namen der verfügbaren Attribute zu bestimmen, und verwenden Sie dann die Ergebnisse mit der **getiteminfo** -Methode.</span><span class="sxs-lookup"><span data-stu-id="7cc03-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="7cc03-125">Ein Beispiel für die Verwendung von Windows Media Player-Objektmethoden zum Abrufen von Metadaten finden Sie unter [Wiedergabeliste. AttributeCount](playlist-attributecount.md).</span><span class="sxs-lookup"><span data-stu-id="7cc03-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cc03-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cc03-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cc03-127">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="7cc03-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7cc03-128">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="7cc03-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="7cc03-129">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="7cc03-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




