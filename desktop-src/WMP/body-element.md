---
title: Body-Element
description: Das Body-Element enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Body-Element Fenster Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369182"
---
# <a name="body-element"></a><span data-ttu-id="78577-104">Body-Element</span><span class="sxs-lookup"><span data-stu-id="78577-104">body Element</span></span>

<span data-ttu-id="78577-105">Das **Body** -Element enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.</span><span class="sxs-lookup"><span data-stu-id="78577-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="78577-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="78577-106">Attributes</span></span>

<span data-ttu-id="78577-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="78577-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="78577-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="78577-108">Parent/Child Elements</span></span>



| <span data-ttu-id="78577-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="78577-109">Hierarchy</span></span> | <span data-ttu-id="78577-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="78577-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="78577-111">Parent</span><span class="sxs-lookup"><span data-stu-id="78577-111">Parent</span></span>    | [<span data-ttu-id="78577-112">smil</span><span class="sxs-lookup"><span data-stu-id="78577-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="78577-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="78577-113">Child</span></span>     | [<span data-ttu-id="78577-114">Seq</span><span class="sxs-lookup"><span data-stu-id="78577-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="78577-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78577-115">Remarks</span></span>

<span data-ttu-id="78577-116">Der Inhalt einer Wiedergabeliste ist innerhalb eines "Element"-Elements organisiert, das im **Body** **-Element enthalten** ist.</span><span class="sxs-lookup"><span data-stu-id="78577-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="78577-117">In der Regel gibt es entweder ein **SEQ** -Element, das einen statischen Satz von Medien Elementen definiert und **Medien** Elemente enthält, oder es gibt ein Element, das einen dynamischen Satz von Medien Elementen definiert und ein **smartwiedergabe** -Element enthält.</span><span class="sxs-lookup"><span data-stu-id="78577-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="78577-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78577-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="78577-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78577-119">Requirements</span></span>



| <span data-ttu-id="78577-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78577-120">Requirement</span></span> | <span data-ttu-id="78577-121">Wert</span><span class="sxs-lookup"><span data-stu-id="78577-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="78577-122">Version</span><span class="sxs-lookup"><span data-stu-id="78577-122">Version</span></span><br/> | <span data-ttu-id="78577-123">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="78577-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78577-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78577-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78577-125">**Media-Element**</span><span class="sxs-lookup"><span data-stu-id="78577-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="78577-126">**ENQ-Element**</span><span class="sxs-lookup"><span data-stu-id="78577-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="78577-127">**smartwiedergabe-Element**</span><span class="sxs-lookup"><span data-stu-id="78577-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="78577-128">**smil-Element**</span><span class="sxs-lookup"><span data-stu-id="78577-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="78577-129">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="78577-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





