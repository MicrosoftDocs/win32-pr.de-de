---
title: Wiedergabeliste. setcheckedstate
description: Die setcheckedstate-Methode gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- Wiedergabeliste. setcheckedstate Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369935"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="722cd-104">Wiedergabeliste. setcheckedstate</span><span class="sxs-lookup"><span data-stu-id="722cd-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="722cd-105">Die **setcheckedstate** -Methode gibt an, dass das indizierte Element in der Wiedergabeliste überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="722cd-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="722cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="722cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="722cd-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="722cd-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="722cd-108">**Number** (**Long**), der den Index des zu überprüfenden Wiedergabelisten Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="722cd-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="722cd-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="722cd-109">Return Value</span></span>

<span data-ttu-id="722cd-110">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="722cd-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="722cd-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="722cd-111">Remarks</span></span>

<span data-ttu-id="722cd-112">Sie können alle Elemente in den aktivierten Zustand setzen, indem Sie im *Item* -Parameter den Wert 1 angeben.</span><span class="sxs-lookup"><span data-stu-id="722cd-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="722cd-113">Diese Methode wurde durch **setCheckedState2** ersetzt, der als Unterstützung für die wieder-Wiedergabeliste steht.</span><span class="sxs-lookup"><span data-stu-id="722cd-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="722cd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="722cd-114">Requirements</span></span>



| <span data-ttu-id="722cd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="722cd-115">Requirement</span></span> | <span data-ttu-id="722cd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="722cd-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="722cd-117">Version</span><span class="sxs-lookup"><span data-stu-id="722cd-117">Version</span></span><br/> | <span data-ttu-id="722cd-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="722cd-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="722cd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="722cd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="722cd-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="722cd-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="722cd-121">**Wiedergabeliste. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="722cd-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





