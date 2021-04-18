---
title: smartwiedergabe-Element
description: Das smartwiedergabe-Element enthält den dynamisch definierten Teil einer Wiedergabeliste.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- smartwiedergabe-Element, Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371489"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="9163e-104">smartwiedergabe-Element</span><span class="sxs-lookup"><span data-stu-id="9163e-104">smartPlaylist Element</span></span>

<span data-ttu-id="9163e-105">Das **smartwiedergabe** -Element enthält den dynamisch definierten Teil einer Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="9163e-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="9163e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="9163e-106">Attributes</span></span>



| <span data-ttu-id="9163e-107">Begriff</span><span class="sxs-lookup"><span data-stu-id="9163e-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="9163e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9163e-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9163e-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**Version** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="9163e-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="9163e-110">Die Dezimalzahl, die die Versionsnummer des intelligenten Wiedergabelisten Schemas darstellt.</span><span class="sxs-lookup"><span data-stu-id="9163e-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="9163e-111">Legen Sie auf 1.0.0.0 fest.</span><span class="sxs-lookup"><span data-stu-id="9163e-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="9163e-112">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="9163e-112">Parent/Child Elements</span></span>



| <span data-ttu-id="9163e-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="9163e-113">Hierarchy</span></span> | <span data-ttu-id="9163e-114">Elemente</span><span class="sxs-lookup"><span data-stu-id="9163e-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="9163e-115">Parent</span><span class="sxs-lookup"><span data-stu-id="9163e-115">Parent</span></span>    | [<span data-ttu-id="9163e-116">Seq</span><span class="sxs-lookup"><span data-stu-id="9163e-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="9163e-117">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="9163e-117">Child</span></span>     | <span data-ttu-id="9163e-118">[Queryset](queryset-element.md), [Filter](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="9163e-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9163e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9163e-119">Remarks</span></span>

<span data-ttu-id="9163e-120">Ein **smartwiedergabe** -Element enthält in der Regel ein **Queryset** -Element und kann auch ein **Filter** Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="9163e-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="9163e-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9163e-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="9163e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9163e-122">Requirements</span></span>



| <span data-ttu-id="9163e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9163e-123">Requirement</span></span> | <span data-ttu-id="9163e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9163e-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="9163e-125">Version</span><span class="sxs-lookup"><span data-stu-id="9163e-125">Version</span></span><br/> | <span data-ttu-id="9163e-126">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9163e-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9163e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9163e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9163e-128">**Argument-Element**</span><span class="sxs-lookup"><span data-stu-id="9163e-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="9163e-129">**Filter-Element**</span><span class="sxs-lookup"><span data-stu-id="9163e-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="9163e-130">**Fragment-Element**</span><span class="sxs-lookup"><span data-stu-id="9163e-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="9163e-131">**Queryset-Element**</span><span class="sxs-lookup"><span data-stu-id="9163e-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="9163e-132">**ENQ-Element**</span><span class="sxs-lookup"><span data-stu-id="9163e-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="9163e-133">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="9163e-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





