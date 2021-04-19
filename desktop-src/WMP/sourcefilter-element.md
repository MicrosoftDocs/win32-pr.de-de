---
title: SourceFilter-Element
description: Das SourceFilter-Element enthält Elemente, die Elemente aus einer Bibliothek auswählen.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Windows Media Player SourceFilter-Element
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367760"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="de6b9-104">SourceFilter-Element</span><span class="sxs-lookup"><span data-stu-id="de6b9-104">sourceFilter Element</span></span>

<span data-ttu-id="de6b9-105">Das **SourceFilter** -Element enthält Elemente, die Elemente aus einer Bibliothek auswählen.</span><span class="sxs-lookup"><span data-stu-id="de6b9-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="de6b9-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="de6b9-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="de6b9-107"><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="de6b9-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="de6b9-108">Der Typ des Filter Objekts.</span><span class="sxs-lookup"><span data-stu-id="de6b9-108">The type of filter object.</span></span> <span data-ttu-id="de6b9-109">Es sind keine vordefinierten Werte für dieses Attribut vorhanden.</span><span class="sxs-lookup"><span data-stu-id="de6b9-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="de6b9-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="de6b9-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="de6b9-111">Der GUID, der das Quell Filter Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="de6b9-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="de6b9-112">Die Methoden des Quell Filter Objekts werden aufgerufen, um die im **SourceFilter** -Element enthaltenen **fragmentelemente** zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="de6b9-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="de6b9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="de6b9-113">Value</span></span>                                  | <span data-ttu-id="de6b9-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de6b9-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="de6b9-115">{4202947a-a563-4b05-A754-a1b4b5989849}</span><span class="sxs-lookup"><span data-stu-id="de6b9-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="de6b9-116">Der GUID für den Quell Filter "Musik in meiner Bibliothek".</span><span class="sxs-lookup"><span data-stu-id="de6b9-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="de6b9-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="de6b9-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="de6b9-118">Der GUID für den Quell Filter "Video in der Bibliothek".</span><span class="sxs-lookup"><span data-stu-id="de6b9-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="de6b9-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="de6b9-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="de6b9-120">Der GUID für den Quell Filter "Bilder in der Bibliothek".</span><span class="sxs-lookup"><span data-stu-id="de6b9-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="de6b9-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="de6b9-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="de6b9-122">Der GUID für den Quell Filter "Fernsehsendungen in meiner Bibliothek".</span><span class="sxs-lookup"><span data-stu-id="de6b9-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="de6b9-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**Name** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="de6b9-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="de6b9-124">Der Name des Filter Objekts.</span><span class="sxs-lookup"><span data-stu-id="de6b9-124">The name of the filter object.</span></span>



| <span data-ttu-id="de6b9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="de6b9-125">Value</span></span>                  | <span data-ttu-id="de6b9-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de6b9-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6b9-127">Musik in meiner Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de6b9-127">Music in my library</span></span>    | <span data-ttu-id="de6b9-128">Ein Filter Objekt, das angegebene Elemente aus dem Satz von Musikelementen in der Bibliothek des Benutzers auswählt.</span><span class="sxs-lookup"><span data-stu-id="de6b9-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="de6b9-129">Video in meiner Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de6b9-129">Video in my library</span></span>    | <span data-ttu-id="de6b9-130">Ein Filter Objekt, das angegebene Elemente aus dem Satz von Videoelementen in der Bibliothek des Benutzers auswählt.</span><span class="sxs-lookup"><span data-stu-id="de6b9-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="de6b9-131">Bilder in meiner Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de6b9-131">Pictures in my library</span></span> | <span data-ttu-id="de6b9-132">Ein Filter Objekt, das die angegebenen Elemente aus dem Satz von Fotoelementen in der Bibliothek des Benutzers auswählt.</span><span class="sxs-lookup"><span data-stu-id="de6b9-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="de6b9-133">Fernsehsendungen in meiner Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de6b9-133">TV shows in my library</span></span> | <span data-ttu-id="de6b9-134">Ein Filter Objekt, das die angegebenen Elemente aus der Gruppe der TV-Elemente in der Bibliothek des Benutzers auswählt.</span><span class="sxs-lookup"><span data-stu-id="de6b9-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="de6b9-135">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="de6b9-135">Parent/Child Elements</span></span>



| <span data-ttu-id="de6b9-136">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="de6b9-136">Hierarchy</span></span> | <span data-ttu-id="de6b9-137">Elemente</span><span class="sxs-lookup"><span data-stu-id="de6b9-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="de6b9-138">Parent</span><span class="sxs-lookup"><span data-stu-id="de6b9-138">Parent</span></span>    | [<span data-ttu-id="de6b9-139">Queryset</span><span class="sxs-lookup"><span data-stu-id="de6b9-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="de6b9-140">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="de6b9-140">Child</span></span>     | [<span data-ttu-id="de6b9-141">Bruch</span><span class="sxs-lookup"><span data-stu-id="de6b9-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="de6b9-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de6b9-142">Remarks</span></span>

<span data-ttu-id="de6b9-143">Das **SourceFilter** -Element wählt Elemente aus der Bibliothek ohne Berücksichtigung der Größe des Resultsets aus.</span><span class="sxs-lookup"><span data-stu-id="de6b9-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="de6b9-144">Das **Filter** -Element hingegen schränkt die Größe des Resultsets ein.</span><span class="sxs-lookup"><span data-stu-id="de6b9-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="de6b9-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de6b9-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a><span data-ttu-id="de6b9-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de6b9-146">Requirements</span></span>



| <span data-ttu-id="de6b9-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de6b9-147">Requirement</span></span> | <span data-ttu-id="de6b9-148">Wert</span><span class="sxs-lookup"><span data-stu-id="de6b9-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="de6b9-149">Version</span><span class="sxs-lookup"><span data-stu-id="de6b9-149">Version</span></span><br/> | <span data-ttu-id="de6b9-150">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="de6b9-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de6b9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de6b9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6b9-152">**Filter-Element**</span><span class="sxs-lookup"><span data-stu-id="de6b9-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="de6b9-153">**Fragment-Element**</span><span class="sxs-lookup"><span data-stu-id="de6b9-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="de6b9-154">**Queryset-Element**</span><span class="sxs-lookup"><span data-stu-id="de6b9-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="de6b9-155">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="de6b9-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





