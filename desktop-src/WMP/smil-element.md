---
title: smil-Element
description: Das smil-Element ist immer das Element der obersten Ebene in einer Windows Media-Wiedergabe Datei (WPL). Er gibt an, dass die Datei SMIL-Syntax und-Grammatik (synchronisiert Multimedia Integration Language) verwendet.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil-Element Windows-Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359739"
---
# <a name="smil-element"></a><span data-ttu-id="44369-105">smil-Element</span><span class="sxs-lookup"><span data-stu-id="44369-105">smil Element</span></span>

<span data-ttu-id="44369-106">Das **SMIL** -Element ist immer das Element der obersten Ebene in einer Windows Media-Wiedergabe Datei (WPL).</span><span class="sxs-lookup"><span data-stu-id="44369-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="44369-107">Er gibt an, dass die Datei SMIL-Syntax und-Grammatik (synchronisiert Multimedia Integration Language) verwendet.</span><span class="sxs-lookup"><span data-stu-id="44369-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="44369-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="44369-108">Attributes</span></span>

<span data-ttu-id="44369-109">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="44369-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="44369-110">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="44369-110">Parent/Child Elements</span></span>



| <span data-ttu-id="44369-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="44369-111">Hierarchy</span></span> | <span data-ttu-id="44369-112">Elemente</span><span class="sxs-lookup"><span data-stu-id="44369-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="44369-113">Parent</span><span class="sxs-lookup"><span data-stu-id="44369-113">Parent</span></span>    | <span data-ttu-id="44369-114">Keine</span><span class="sxs-lookup"><span data-stu-id="44369-114">None</span></span>                                               |
| <span data-ttu-id="44369-115">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="44369-115">Child</span></span>     | <span data-ttu-id="44369-116">[Kopf](head-element.md), [Text](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="44369-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="44369-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44369-117">Remarks</span></span>

<span data-ttu-id="44369-118">Jede Windows-Medienwiedergabe Liste muss über das **SMIL** -Element im Stammverzeichnis verfügen.</span><span class="sxs-lookup"><span data-stu-id="44369-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="44369-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44369-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="44369-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44369-120">Requirements</span></span>



| <span data-ttu-id="44369-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44369-121">Requirement</span></span> | <span data-ttu-id="44369-122">Wert</span><span class="sxs-lookup"><span data-stu-id="44369-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="44369-123">Version</span><span class="sxs-lookup"><span data-stu-id="44369-123">Version</span></span><br/> | <span data-ttu-id="44369-124">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="44369-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44369-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44369-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44369-126">**Body-Element**</span><span class="sxs-lookup"><span data-stu-id="44369-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="44369-127">**Head-Element**</span><span class="sxs-lookup"><span data-stu-id="44369-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="44369-128">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="44369-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





