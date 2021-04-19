---
title: Wiedergabeliste. getNextSelectedItem2
description: Die getNextSelectedItem2-Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- Wiedergabeliste. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373607"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="78625-104">Wiedergabeliste. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="78625-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="78625-105">Die **getNextSelectedItem2** -Methode ruft den Index des nächsten ausgewählten Elements in der Wiedergabeliste nach dem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="78625-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="78625-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78625-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="78625-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="78625-108">**Zahl** (**Long**), die den Index des Elements angibt, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="78625-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78625-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78625-109">Return Value</span></span>

<span data-ttu-id="78625-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="78625-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="78625-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78625-111">Remarks</span></span>

<span data-ttu-id="78625-112">Diese Methode kann mit geschachtelte-Wiedergabelisten arbeiten und ersetzt die **getnextselecteditem** -Methode, die nicht.</span><span class="sxs-lookup"><span data-stu-id="78625-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="78625-113">Übergeben Sie 1 in den *Element* Parameter, um das erste ausgewählte Element zu suchen.</span><span class="sxs-lookup"><span data-stu-id="78625-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="78625-114">Wenn keine weiteren ausgewählten Elemente vorhanden sind, wird-1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78625-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="78625-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78625-115">Requirements</span></span>



| <span data-ttu-id="78625-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78625-116">Requirement</span></span> | <span data-ttu-id="78625-117">Wert</span><span class="sxs-lookup"><span data-stu-id="78625-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="78625-118">Version</span><span class="sxs-lookup"><span data-stu-id="78625-118">Version</span></span><br/> | <span data-ttu-id="78625-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="78625-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78625-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78625-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78625-121">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="78625-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="78625-122">**Wiedergabeliste. getnextselecteditem**</span><span class="sxs-lookup"><span data-stu-id="78625-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





