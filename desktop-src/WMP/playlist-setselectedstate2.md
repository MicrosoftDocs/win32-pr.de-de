---
title: Wiedergabeliste. setSelectedState2
description: Die setSelectedState2-Methode legt den ausgewählten Zustand des Elements mit dem angegebenen Index im Wiedergabelisten Element fest.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- Wiedergabeliste. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374037"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="18ac6-104">Wiedergabeliste. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="18ac6-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="18ac6-105">Die **setSelectedState2** -Methode legt den ausgewählten Zustand des Elements mit dem angegebenen Index im **Wiedergabe** Listenelement fest.</span><span class="sxs-lookup"><span data-stu-id="18ac6-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="18ac6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18ac6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ac6-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="18ac6-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="18ac6-108">**Zahl** (**Long**), die den Index eines Elements in der Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="18ac6-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="18ac6-109"><span id="selected"></span><span id="SELECTED"></span>*gewählte*</span><span class="sxs-lookup"><span data-stu-id="18ac6-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="18ac6-110">Ein **boolescher** Wert, der angibt, ob das angegebene Element ausgewählt (true) oder nicht ausgewählt (false) ist.</span><span class="sxs-lookup"><span data-stu-id="18ac6-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ac6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18ac6-111">Return Value</span></span>

<span data-ttu-id="18ac6-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="18ac6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ac6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18ac6-113">Remarks</span></span>

<span data-ttu-id="18ac6-114">Diese Methode kann mit zusammengefügten Wiedergabelisten arbeiten und ersetzt die **setselectedstate** -Methode, die nicht.</span><span class="sxs-lookup"><span data-stu-id="18ac6-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="18ac6-115">Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.</span><span class="sxs-lookup"><span data-stu-id="18ac6-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ac6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18ac6-116">Requirements</span></span>



| <span data-ttu-id="18ac6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18ac6-117">Requirement</span></span> | <span data-ttu-id="18ac6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="18ac6-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="18ac6-119">Version</span><span class="sxs-lookup"><span data-stu-id="18ac6-119">Version</span></span><br/> | <span data-ttu-id="18ac6-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="18ac6-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18ac6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18ac6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ac6-122">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="18ac6-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="18ac6-123">**Wiedergabeliste. setselectedstate**</span><span class="sxs-lookup"><span data-stu-id="18ac6-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





