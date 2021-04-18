---
title: Wiedergabeliste. getNextCheckedItem2
description: Die getNextCheckedItem2-Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Wiedergabeliste. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368285"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="cf371-104">Wiedergabeliste. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="cf371-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="cf371-105">Die **getNextCheckedItem2** -Methode ruft den Index des nächsten aktivierten Elements in der Wiedergabeliste nach dem angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="cf371-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="cf371-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf371-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf371-107"><span id="item"></span><span id="ITEM"></span>*Position*</span><span class="sxs-lookup"><span data-stu-id="cf371-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="cf371-108">**Zahl** (**Long**), die den Index des Elements angibt, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf371-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf371-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf371-109">Return Value</span></span>

<span data-ttu-id="cf371-110">Diese Methode gibt eine **Zahl** (**Long**) zurück.</span><span class="sxs-lookup"><span data-stu-id="cf371-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf371-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf371-111">Remarks</span></span>

<span data-ttu-id="cf371-112">Diese Methode kann mit schsted-Wiedergabelisten arbeiten und ersetzt die **getnextcheckeditem** -Methode, die nicht.</span><span class="sxs-lookup"><span data-stu-id="cf371-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="cf371-113">Übergeben Sie 1 in den *Element* Parameter, um das erste aktivierte Element zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cf371-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="cf371-114">Wenn keine weiteren aktivierten Elemente vorhanden sind, gibt diese Methode 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="cf371-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf371-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf371-115">Requirements</span></span>



| <span data-ttu-id="cf371-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf371-116">Requirement</span></span> | <span data-ttu-id="cf371-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cf371-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="cf371-118">Version</span><span class="sxs-lookup"><span data-stu-id="cf371-118">Version</span></span><br/> | <span data-ttu-id="cf371-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="cf371-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf371-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf371-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf371-121">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="cf371-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="cf371-122">**Wiedergabeliste. getnextcheckeditem**</span><span class="sxs-lookup"><span data-stu-id="cf371-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





