---
title: Head-Element
description: Das Head-Element enthält Metadaten, die auf die gesamte Wiedergabeliste angewendet werden.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Windows-Media Player des Head-Elements
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361956"
---
# <a name="head-element"></a><span data-ttu-id="d4f2b-104">Head-Element</span><span class="sxs-lookup"><span data-stu-id="d4f2b-104">head Element</span></span>

<span data-ttu-id="d4f2b-105">Das **Head** -Element enthält Metadaten, die auf die gesamte Wiedergabeliste angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4f2b-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="d4f2b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4f2b-106">Attributes</span></span>

<span data-ttu-id="d4f2b-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="d4f2b-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d4f2b-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="d4f2b-108">Parent/Child Elements</span></span>



| <span data-ttu-id="d4f2b-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d4f2b-109">Hierarchy</span></span> | <span data-ttu-id="d4f2b-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="d4f2b-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="d4f2b-111">Parent</span><span class="sxs-lookup"><span data-stu-id="d4f2b-111">Parent</span></span>    | [<span data-ttu-id="d4f2b-112">smil</span><span class="sxs-lookup"><span data-stu-id="d4f2b-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="d4f2b-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="d4f2b-113">Child</span></span>     | <span data-ttu-id="d4f2b-114">[Title](title-element--wpl.md), [Meta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="d4f2b-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d4f2b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4f2b-115">Remarks</span></span>

<span data-ttu-id="d4f2b-116">In der Regel enthält das **Head** -Element ein **Title** -Element und ein oder mehrere **Meta** -Elemente, die globale Merkmale der Wiedergabeliste definieren.</span><span class="sxs-lookup"><span data-stu-id="d4f2b-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="d4f2b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4f2b-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="d4f2b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4f2b-118">Requirements</span></span>



| <span data-ttu-id="d4f2b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4f2b-119">Requirement</span></span> | <span data-ttu-id="d4f2b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d4f2b-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="d4f2b-121">Version</span><span class="sxs-lookup"><span data-stu-id="d4f2b-121">Version</span></span><br/> | <span data-ttu-id="d4f2b-122">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d4f2b-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4f2b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4f2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f2b-124">**Meta-Element**</span><span class="sxs-lookup"><span data-stu-id="d4f2b-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="d4f2b-125">**Title-Element (WPL)**</span><span class="sxs-lookup"><span data-stu-id="d4f2b-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="d4f2b-126">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="d4f2b-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





