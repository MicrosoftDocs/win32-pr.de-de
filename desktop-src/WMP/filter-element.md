---
title: Filter-Element
description: Das Filter-Element enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medien Elementen in einer Wiedergabeliste einschränken.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Filter Element Fenster Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366970"
---
# <a name="filter-element"></a><span data-ttu-id="35eac-104">Filter-Element</span><span class="sxs-lookup"><span data-stu-id="35eac-104">filter Element</span></span>

<span data-ttu-id="35eac-105">Das **Filter** -Element enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medien Elementen in einer Wiedergabeliste einschränken.</span><span class="sxs-lookup"><span data-stu-id="35eac-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="35eac-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="35eac-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="35eac-107"><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="35eac-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="35eac-108">Der Typ des Filter Objekts.</span><span class="sxs-lookup"><span data-stu-id="35eac-108">The type of filter object.</span></span> <span data-ttu-id="35eac-109">Es sind keine vordefinierten Werte für dieses Attribut vorhanden.</span><span class="sxs-lookup"><span data-stu-id="35eac-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="35eac-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="35eac-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="35eac-111">Die GUID, die ein Filter Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="35eac-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="35eac-112">Die Methoden des Filter Objekts werden aufgerufen, um die im **Filter** Element enthaltenen **fragmentelemente** zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="35eac-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="35eac-113">Wert</span><span class="sxs-lookup"><span data-stu-id="35eac-113">Value</span></span>                                  | <span data-ttu-id="35eac-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35eac-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35eac-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="35eac-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="35eac-116">Die ID für den Filter "Microsoft Auto-Wiedergabeliste--schränkt die automatische Wiedergabeliste nach Anzahl, Größe oder Dauer" ein.</span><span class="sxs-lookup"><span data-stu-id="35eac-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="35eac-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**Name** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="35eac-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="35eac-118">Der Name des Filter Objekts.</span><span class="sxs-lookup"><span data-stu-id="35eac-118">The name of the filter object.</span></span>



| <span data-ttu-id="35eac-119">Wert</span><span class="sxs-lookup"><span data-stu-id="35eac-119">Value</span></span>                                                                              | <span data-ttu-id="35eac-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35eac-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="35eac-121">Microsoft Auto-Wiedergabe Filter: schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein.</span><span class="sxs-lookup"><span data-stu-id="35eac-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="35eac-122">Schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein.</span><span class="sxs-lookup"><span data-stu-id="35eac-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="35eac-123">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="35eac-123">Parent/Child Elements</span></span>



| <span data-ttu-id="35eac-124">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="35eac-124">Hierarchy</span></span> | <span data-ttu-id="35eac-125">Elemente</span><span class="sxs-lookup"><span data-stu-id="35eac-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="35eac-126">Parent</span><span class="sxs-lookup"><span data-stu-id="35eac-126">Parent</span></span>    | [<span data-ttu-id="35eac-127">smartwiedergabe</span><span class="sxs-lookup"><span data-stu-id="35eac-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="35eac-128">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="35eac-128">Child</span></span>     | [<span data-ttu-id="35eac-129">Bruch</span><span class="sxs-lookup"><span data-stu-id="35eac-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="35eac-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35eac-130">Remarks</span></span>

<span data-ttu-id="35eac-131">Das **Filter** -Element fügt einer Wiedergabeliste keine Medienelemente hinzu. der Inhalt, der vom **SourceFilter** -Element ausgewählt wurde, wird einfach entfernt oder herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="35eac-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="35eac-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35eac-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="35eac-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35eac-133">Requirements</span></span>



| <span data-ttu-id="35eac-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35eac-134">Requirement</span></span> | <span data-ttu-id="35eac-135">Wert</span><span class="sxs-lookup"><span data-stu-id="35eac-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="35eac-136">Version</span><span class="sxs-lookup"><span data-stu-id="35eac-136">Version</span></span><br/> | <span data-ttu-id="35eac-137">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="35eac-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35eac-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35eac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eac-139">**Argument-Element**</span><span class="sxs-lookup"><span data-stu-id="35eac-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="35eac-140">**Fragment-Element**</span><span class="sxs-lookup"><span data-stu-id="35eac-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="35eac-141">**smartwiedergabe-Element**</span><span class="sxs-lookup"><span data-stu-id="35eac-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="35eac-142">**SourceFilter-Element**</span><span class="sxs-lookup"><span data-stu-id="35eac-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="35eac-143">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="35eac-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





