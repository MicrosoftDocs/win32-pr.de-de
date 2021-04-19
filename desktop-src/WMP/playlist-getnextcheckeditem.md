---
title: Wiedergabeliste. getnextcheckeditem
description: Die getnextcheckeditem-Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Wiedergabeliste. getnextcheckeditem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373608"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="cacd4-104">Wiedergabeliste. getnextcheckeditem</span><span class="sxs-lookup"><span data-stu-id="cacd4-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="cacd4-105">Die **getnextcheckeditem** -Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="cacd4-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="cacd4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cacd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cacd4-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="cacd4-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="cacd4-108">**Zahl** (**Long**), die den Index des Elements angibt, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cacd4-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cacd4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cacd4-109">Return Value</span></span>

<span data-ttu-id="cacd4-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="cacd4-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="cacd4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cacd4-111">Remarks</span></span>

<span data-ttu-id="cacd4-112">Wenn keine weiteren aktivierten Elemente vorhanden sind, gibt diese Methode 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="cacd4-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="cacd4-113">Diese Methode wurde durch **getNextCheckedItem2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.</span><span class="sxs-lookup"><span data-stu-id="cacd4-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacd4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacd4-114">Requirements</span></span>



| <span data-ttu-id="cacd4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cacd4-115">Requirement</span></span> | <span data-ttu-id="cacd4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cacd4-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cacd4-117">Version</span><span class="sxs-lookup"><span data-stu-id="cacd4-117">Version</span></span><br/> | <span data-ttu-id="cacd4-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="cacd4-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cacd4-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cacd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacd4-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="cacd4-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="cacd4-121">**Wiedergabeliste. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="cacd4-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





