---
title: Wiedergabeliste. getnextselecteditem
description: Die getnextselecteditem-Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- Wiedergabeliste. getnextselecteditem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368284"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="933e1-104">Wiedergabeliste. getnextselecteditem</span><span class="sxs-lookup"><span data-stu-id="933e1-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="933e1-105">Die **getnextselecteditem** -Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="933e1-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="933e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="933e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933e1-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="933e1-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="933e1-108">**Zahl** (**Long**), die den Index des Elements angibt, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="933e1-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933e1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="933e1-109">Return Value</span></span>

<span data-ttu-id="933e1-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="933e1-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="933e1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="933e1-111">Remarks</span></span>

<span data-ttu-id="933e1-112">Wenn keine weiteren ausgewählten Elemente vorhanden sind, gibt diese Methode 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="933e1-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="933e1-113">Diese Methode wurde durch **getNextSelectedItem2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.</span><span class="sxs-lookup"><span data-stu-id="933e1-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="933e1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="933e1-114">Requirements</span></span>



| <span data-ttu-id="933e1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="933e1-115">Requirement</span></span> | <span data-ttu-id="933e1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="933e1-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="933e1-117">Version</span><span class="sxs-lookup"><span data-stu-id="933e1-117">Version</span></span><br/> | <span data-ttu-id="933e1-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="933e1-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="933e1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="933e1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933e1-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="933e1-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="933e1-121">**Wiedergabeliste. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="933e1-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





