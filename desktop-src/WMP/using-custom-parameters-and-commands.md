---
title: Verwenden von benutzerdefinierten Parametern und Befehlen
description: Verwenden von benutzerdefinierten Parametern und Befehlen
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Media Metadatei-Wiedergabelisten, benutzerdefinierte Parameter
- Wiedergabelisten, benutzerdefinierte Parameter
- Metadatei-Wiedergabelisten, benutzerdefinierte Parameter
- Windows Media Metadatei-Wiedergabelisten, benutzerdefinierte Befehle
- Wiedergabelisten, benutzerdefinierte Befehle
- Metadatei-Wiedergabelisten, benutzerdefinierte Befehle
- Windows Media Metadatei-Wiedergabelisten, Parameter
- Wiedergabelisten, Parameter
- Metadatei-Wiedergabelisten, Parameter
- benutzerdefinierte Parameter
- Benutzerdefinierte Befehle
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856327"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="7eea2-114">Verwenden von benutzerdefinierten Parametern und Befehlen</span><span class="sxs-lookup"><span data-stu-id="7eea2-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="7eea2-115">Mithilfe des **param** -Elements können Sie benutzerdefinierte Parameter erstellen, um zusätzliche Metadaten in einer Metadatei-Wiedergabeliste zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="7eea2-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="7eea2-116">Verwenden Sie das **Name** -Attribut des **param** -Elements, um den Namen des benutzerdefinierten Parameters zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7eea2-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="7eea2-117">Verwenden Sie das **value** -Attribut, um den Wert für den benannten benutzerdefinierten Parameter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7eea2-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="7eea2-118">Rufen Sie **param** -Metadaten mithilfe der **getiteminfo** -Methoden der **Medien** -und **Wiedergabe** Listen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="7eea2-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="7eea2-119">Ein Beispiel für die Verwendung dieser Methoden zum Abrufen von Metadaten finden Sie unter der [AttributeCount](playlist-attributecount.md) -Methode des **Wiedergabe** Listen Objekts.</span><span class="sxs-lookup"><span data-stu-id="7eea2-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="7eea2-120">Die folgende Beispiel-Metadatei-Wiedergabeliste zeigt die Verwendung des **param** -Elements, um benutzerdefinierte Parameter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="7eea2-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="7eea2-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7eea2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eea2-122">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="7eea2-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




