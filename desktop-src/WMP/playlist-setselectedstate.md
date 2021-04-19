---
title: Wiedergabeliste. setselectedstate
description: Die setselectedstate-Methode gibt an, dass das indizierte Element in der Wiedergabeliste ausgewählt ist.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- Wiedergabeliste. setselectedstate Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360448"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="b171b-104">Wiedergabeliste. setselectedstate</span><span class="sxs-lookup"><span data-stu-id="b171b-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="b171b-105">Die **setselectedstate** -Methode gibt an, dass das indizierte Element in der Wiedergabeliste ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b171b-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="b171b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b171b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b171b-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="b171b-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="b171b-108">**Zahl** (**Long**), die den Index eines Elements in der Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="b171b-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b171b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b171b-109">Return Value</span></span>

<span data-ttu-id="b171b-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b171b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b171b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b171b-111">Remarks</span></span>

<span data-ttu-id="b171b-112">Sie können alle Elemente auf den ausgewählten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.</span><span class="sxs-lookup"><span data-stu-id="b171b-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="b171b-113">Diese Methode wurde durch **setSelectedState2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.</span><span class="sxs-lookup"><span data-stu-id="b171b-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="b171b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b171b-114">Requirements</span></span>



| <span data-ttu-id="b171b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b171b-115">Requirement</span></span> | <span data-ttu-id="b171b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b171b-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b171b-117">Version</span><span class="sxs-lookup"><span data-stu-id="b171b-117">Version</span></span><br/> | <span data-ttu-id="b171b-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b171b-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b171b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b171b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b171b-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="b171b-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="b171b-121">**Wiedergabeliste. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="b171b-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





