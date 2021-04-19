---
title: Wiedergabeliste. ItemCount
description: Das ItemCount-Attribut ruft die Anzahl der Elemente ab, die momentan im Wiedergabelisten Element angezeigt werden.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Wiedergabeliste. ItemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359785"
---
# <a name="playlistitemcount"></a><span data-ttu-id="93b28-104">Wiedergabeliste. ItemCount</span><span class="sxs-lookup"><span data-stu-id="93b28-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="93b28-105">Das **ItemCount** -Attribut ruft die Anzahl der Elemente ab, die momentan im **Wiedergabe** Listenelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="93b28-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="93b28-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="93b28-106">Possible Values</span></span>

<span data-ttu-id="93b28-107">Bei diesem Attribut handelt es sich um eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="93b28-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="93b28-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93b28-108">Remarks</span></span>

<span data-ttu-id="93b28-109">Die **ItemCount** -Eigenschaft zählt die Gesamtzahl der erweiterten Elemente.</span><span class="sxs-lookup"><span data-stu-id="93b28-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="93b28-110">Wenn beispielsweise zwei Wiedergabelisten vorhanden sind, die jeweils drei Medienelemente enthalten, gibt **ItemCount** 2 zurück, wenn die Wiedergabelisten nicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="93b28-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="93b28-111">Wenn nur die erste Wiedergabeliste erweitert ist, wird von **ItemCount** der Wert 4 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93b28-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="93b28-112">Wenn beide Wiedergabelisten erweitert werden, wird von **ItemCount** der Wert 6 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93b28-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="93b28-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93b28-113">Requirements</span></span>



| <span data-ttu-id="93b28-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93b28-114">Requirement</span></span> | <span data-ttu-id="93b28-115">Wert</span><span class="sxs-lookup"><span data-stu-id="93b28-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="93b28-116">Version</span><span class="sxs-lookup"><span data-stu-id="93b28-116">Version</span></span><br/> | <span data-ttu-id="93b28-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="93b28-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93b28-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93b28-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b28-119">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="93b28-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





