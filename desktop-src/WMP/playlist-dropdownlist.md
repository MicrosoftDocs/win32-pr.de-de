---
title: Wiedergabeliste. Dropdown List
description: Mit dem DropDownList-Attribut wird ein Wert angegeben oder abgerufen, der angibt, welche Elemente im Dropdown-Listenfeld für eine bestimmte Instanz des Wiedergabelisten Elements angezeigt werden.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- Wiedergabeliste. DropDownList Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356381"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="bbd46-104">Wiedergabeliste. Dropdown List</span><span class="sxs-lookup"><span data-stu-id="bbd46-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="bbd46-105">Mit dem **DropDownList** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, welche Elemente im Dropdown-Listenfeld für eine bestimmte Instanz des **Wiedergabe** Listen Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd46-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="bbd46-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="bbd46-106">Possible Values</span></span>

<span data-ttu-id="bbd46-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="bbd46-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="bbd46-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd46-108">Value</span></span>       | <span data-ttu-id="bbd46-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbd46-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd46-110">showalbums</span><span class="sxs-lookup"><span data-stu-id="bbd46-110">showAlbums</span></span>  | <span data-ttu-id="bbd46-111">Zeigt Alben an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="bbd46-112">ShowAll</span><span class="sxs-lookup"><span data-stu-id="bbd46-112">showAll</span></span>     | <span data-ttu-id="bbd46-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="bbd46-113">Default.</span></span> <span data-ttu-id="bbd46-114">Zeigt alle verfügbaren Elemente an, einschließlich CD-Wiedergabelisten, Benutzer Wiedergabelisten und Options Voreinstellungen.</span><span class="sxs-lookup"><span data-stu-id="bbd46-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="bbd46-115">showcd</span><span class="sxs-lookup"><span data-stu-id="bbd46-115">showCD</span></span>      | <span data-ttu-id="bbd46-116">Zeigt die CD-Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="bbd46-117">showclips</span><span class="sxs-lookup"><span data-stu-id="bbd46-117">showClips</span></span>   | <span data-ttu-id="bbd46-118">Zeigt alle Clips an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="bbd46-119">showcurrent</span><span class="sxs-lookup"><span data-stu-id="bbd46-119">showCurrent</span></span> | <span data-ttu-id="bbd46-120">Zeigt die aktuelle, nicht gespeicherte Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="bbd46-121">showlibrary</span><span class="sxs-lookup"><span data-stu-id="bbd46-121">showLibrary</span></span> | <span data-ttu-id="bbd46-122">Zeigt nur Bibliotheks Wiedergabelisten an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="bbd46-123">showradio</span><span class="sxs-lookup"><span data-stu-id="bbd46-123">showRadio</span></span>   | <span data-ttu-id="bbd46-124">Zeigt Options Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="bbd46-125">showqueries</span><span class="sxs-lookup"><span data-stu-id="bbd46-125">showQueries</span></span> | <span data-ttu-id="bbd46-126">Zeigt Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="bbd46-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="bbd46-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd46-127">Requirements</span></span>



| <span data-ttu-id="bbd46-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd46-128">Requirement</span></span> | <span data-ttu-id="bbd46-129">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd46-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bbd46-130">Version</span><span class="sxs-lookup"><span data-stu-id="bbd46-130">Version</span></span><br/> | <span data-ttu-id="bbd46-131">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bbd46-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbd46-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd46-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd46-133">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="bbd46-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





