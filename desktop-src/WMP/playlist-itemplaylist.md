---
title: Wiedergabeliste. itemwiedergabe Liste
description: Das itemwiedergabe-Attribut ruft die Wiedergabeliste für das Medien Element ab, das am angegebenen Index im Wiedergabelisten Element angezeigt wird.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- Wiedergabeliste. itemwiedergabe Fenster Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359783"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="4a864-104">Wiedergabeliste. itemwiedergabe Liste</span><span class="sxs-lookup"><span data-stu-id="4a864-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="4a864-105">Das **itemwiedergabe** -Attribut ruft die Wiedergabeliste für das Medien Element ab, das am angegebenen Index im **Wiedergabe** Listenelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4a864-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="4a864-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4a864-106">Possible Values</span></span>

<span data-ttu-id="4a864-107">Dieses Attribut ist ein Schreib geschütztes **Wiedergabe** Listen Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a864-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a864-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a864-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a864-109"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="4a864-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="4a864-110">**Zahl**(**Long**), die den Index eines Wiedergabelisten Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="4a864-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a864-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a864-111">Remarks</span></span>

<span data-ttu-id="4a864-112">Die **itemwiedergabe** -Eigenschaft gibt das Wiedergabelisten Objekt zurück, das im **Wiedergabe** Listenelement erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="4a864-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="4a864-113">Wenn z. b. zwei nicht im **Wiedergabe** Listenelement enthaltene, nicht erweiterte Wiedergabelisten vorhanden sind und jeweils drei Medienclips enthalten, gibt **itemwiedergabe**(1) die übergeordnete Wiedergabeliste zurück, die die beiden in der Liste enthaltenen Wiedergabelisten enthält.</span><span class="sxs-lookup"><span data-stu-id="4a864-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="4a864-114">Wenn die zweite Wiedergabeliste erweitert ist, gibt **itemwiedergabe**(1) die zweite Wiedergabeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="4a864-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="4a864-115">Wenn beide Wiedergabelisten erweitert werden, gibt **itemwiedergabe**(1) die erste Wiedergabeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="4a864-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a864-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a864-116">Requirements</span></span>



| <span data-ttu-id="4a864-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a864-117">Requirement</span></span> | <span data-ttu-id="4a864-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4a864-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="4a864-119">Version</span><span class="sxs-lookup"><span data-stu-id="4a864-119">Version</span></span><br/> | <span data-ttu-id="4a864-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4a864-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a864-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a864-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a864-122">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="4a864-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="4a864-123">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="4a864-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





