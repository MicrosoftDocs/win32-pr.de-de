---
title: Queryset-Element
description: Das Queryset-Element enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Queryset-Element, Windows-Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356023"
---
# <a name="queryset-element"></a><span data-ttu-id="382cf-104">Queryset-Element</span><span class="sxs-lookup"><span data-stu-id="382cf-104">querySet Element</span></span>

<span data-ttu-id="382cf-105">Das **Queryset** -Element enthält Elemente, die definieren, welche Medienelemente aus der Bibliothek ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="382cf-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="382cf-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="382cf-106">Attributes</span></span>

<span data-ttu-id="382cf-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="382cf-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="382cf-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="382cf-108">Parent/Child Elements</span></span>



| <span data-ttu-id="382cf-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="382cf-109">Hierarchy</span></span> | <span data-ttu-id="382cf-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="382cf-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="382cf-111">Parent</span><span class="sxs-lookup"><span data-stu-id="382cf-111">Parent</span></span>    | [<span data-ttu-id="382cf-112">smartwiedergabe</span><span class="sxs-lookup"><span data-stu-id="382cf-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="382cf-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="382cf-113">Child</span></span>     | [<span data-ttu-id="382cf-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="382cf-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="382cf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="382cf-115">Remarks</span></span>

<span data-ttu-id="382cf-116">Das **Queryset** -Element gibt an, welche Medienelemente aus der Bibliothek ausgewählt werden sollen, ohne Berücksichtigung der Größe des Resultsets.</span><span class="sxs-lookup"><span data-stu-id="382cf-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="382cf-117">Das **Filter** -Element hingegen schränkt die Größe des Resultsets ein.</span><span class="sxs-lookup"><span data-stu-id="382cf-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="382cf-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="382cf-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="382cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="382cf-119">Requirements</span></span>



| <span data-ttu-id="382cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="382cf-120">Requirement</span></span> | <span data-ttu-id="382cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="382cf-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="382cf-122">Version</span><span class="sxs-lookup"><span data-stu-id="382cf-122">Version</span></span><br/> | <span data-ttu-id="382cf-123">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="382cf-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="382cf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="382cf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="382cf-125">**Argument-Element**</span><span class="sxs-lookup"><span data-stu-id="382cf-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="382cf-126">**Filter-Element**</span><span class="sxs-lookup"><span data-stu-id="382cf-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="382cf-127">**Fragment-Element**</span><span class="sxs-lookup"><span data-stu-id="382cf-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="382cf-128">**smartwiedergabe-Element**</span><span class="sxs-lookup"><span data-stu-id="382cf-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="382cf-129">**SourceFilter-Element**</span><span class="sxs-lookup"><span data-stu-id="382cf-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="382cf-130">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="382cf-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





