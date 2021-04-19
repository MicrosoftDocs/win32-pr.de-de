---
title: Wiedergabeliste. setCheckedState2
description: Die setCheckedState2-Methode legt den aktivierten Zustand des Elements mit dem angegebenen Index im Wiedergabelisten Element fest.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- Wiedergabeliste. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360279"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="9cc65-104">Wiedergabeliste. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="9cc65-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="9cc65-105">Die **setCheckedState2** -Methode legt den aktivierten Zustand des Elements mit dem angegebenen Index im **Wiedergabe** Listenelement fest.</span><span class="sxs-lookup"><span data-stu-id="9cc65-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="9cc65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cc65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc65-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="9cc65-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="9cc65-108">**Zahl** (**Long**), die den Index des Wiedergabelisten Elements angibt, das überprüft oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9cc65-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="9cc65-109"><span id="checked"></span><span id="CHECKED"></span>*über*</span><span class="sxs-lookup"><span data-stu-id="9cc65-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="9cc65-110">**Boolescher** Wert, der angibt, ob das angegebene Element überprüft (true) oder deaktiviert (false) ist.</span><span class="sxs-lookup"><span data-stu-id="9cc65-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc65-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cc65-111">Return Value</span></span>

<span data-ttu-id="9cc65-112">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9cc65-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc65-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cc65-113">Remarks</span></span>

<span data-ttu-id="9cc65-114">Diese Methode kann mit schsted-Wiedergabelisten arbeiten und ersetzt die **setcheckedstate** -Methode, die nicht.</span><span class="sxs-lookup"><span data-stu-id="9cc65-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="9cc65-115">Sie können alle Elemente auf den angeforderten Zustand festlegen, indem Sie im *Item* -Parameter den Wert 1 angeben.</span><span class="sxs-lookup"><span data-stu-id="9cc65-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc65-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cc65-116">Requirements</span></span>



| <span data-ttu-id="9cc65-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cc65-117">Requirement</span></span> | <span data-ttu-id="9cc65-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9cc65-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9cc65-119">Version</span><span class="sxs-lookup"><span data-stu-id="9cc65-119">Version</span></span><br/> | <span data-ttu-id="9cc65-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="9cc65-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cc65-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cc65-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc65-122">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="9cc65-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="9cc65-123">**Wiedergabeliste. setcheckedstate**</span><span class="sxs-lookup"><span data-stu-id="9cc65-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





