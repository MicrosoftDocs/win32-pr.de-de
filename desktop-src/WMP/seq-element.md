---
title: ENQ-Element
description: Das Element "-q" enthält Elemente, die eine statische Wiedergabeliste oder Elemente definieren, die eine intelligente Wiedergabeliste definieren.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Media Player für das Fenster "
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354068"
---
# <a name="seq-element"></a><span data-ttu-id="ebb90-104">ENQ-Element</span><span class="sxs-lookup"><span data-stu-id="ebb90-104">seq Element</span></span>

<span data-ttu-id="ebb90-105">Das Element "- **q** " enthält Elemente, die eine statische Wiedergabeliste oder Elemente definieren, die eine intelligente Wiedergabeliste definieren.</span><span class="sxs-lookup"><span data-stu-id="ebb90-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="ebb90-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="ebb90-106">Attributes</span></span>

<span data-ttu-id="ebb90-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="ebb90-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ebb90-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="ebb90-108">Parent/Child Elements</span></span>



| <span data-ttu-id="ebb90-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="ebb90-109">Hierarchy</span></span> | <span data-ttu-id="ebb90-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="ebb90-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="ebb90-111">Parent</span><span class="sxs-lookup"><span data-stu-id="ebb90-111">Parent</span></span>    | [<span data-ttu-id="ebb90-112">body</span><span class="sxs-lookup"><span data-stu-id="ebb90-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="ebb90-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="ebb90-113">Child</span></span>     | <span data-ttu-id="ebb90-114">[Medien](media-element.md), [smartwiedergabe Liste](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="ebb90-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ebb90-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ebb90-115">Remarks</span></span>

<span data-ttu-id="ebb90-116">Wenn ein Element vom Typ "- **q** " nur **Medien** Elemente enthält, die auf bestimmte Medienelemente verweisen, wird die Wiedergabeliste als statisch betrachtet.</span><span class="sxs-lookup"><span data-stu-id="ebb90-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="ebb90-117">Wenn ein Element vom Typ "- **q** " ein **smartwiedergabe** -Element enthält, wird es als dynamische "intelligente" Wiedergabeliste betrachtet.</span><span class="sxs-lookup"><span data-stu-id="ebb90-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="ebb90-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebb90-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="ebb90-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebb90-119">Requirements</span></span>



| <span data-ttu-id="ebb90-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebb90-120">Requirement</span></span> | <span data-ttu-id="ebb90-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ebb90-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="ebb90-122">Version</span><span class="sxs-lookup"><span data-stu-id="ebb90-122">Version</span></span><br/> | <span data-ttu-id="ebb90-123">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ebb90-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebb90-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebb90-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb90-125">**Body-Element**</span><span class="sxs-lookup"><span data-stu-id="ebb90-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="ebb90-126">**Media-Element**</span><span class="sxs-lookup"><span data-stu-id="ebb90-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="ebb90-127">**smartwiedergabe-Element**</span><span class="sxs-lookup"><span data-stu-id="ebb90-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="ebb90-128">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="ebb90-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





