---
title: Meta-Element
description: Das Meta-Element gibt Metadaten an, die auf die gesamte Wiedergabeliste angewendet werden.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Media Player des Meta-Element-Windows
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359329"
---
# <a name="meta-element"></a><span data-ttu-id="bb99b-104">Meta-Element</span><span class="sxs-lookup"><span data-stu-id="bb99b-104">meta Element</span></span>

<span data-ttu-id="bb99b-105">Das **Meta** -Element gibt Metadaten an, die auf die gesamte Wiedergabeliste angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb99b-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="bb99b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="bb99b-106">Attributes</span></span>



| <span data-ttu-id="bb99b-107">Begriff</span><span class="sxs-lookup"><span data-stu-id="bb99b-107">Term</span></span>                                                                       | <span data-ttu-id="bb99b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb99b-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb99b-109"><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="bb99b-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="bb99b-110">Der Name eines Elements von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="bb99b-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="bb99b-111"><span id="content"></span><span id="CONTENT"></span>**inhaltliche**</span><span class="sxs-lookup"><span data-stu-id="bb99b-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="bb99b-112">Der Wert eines Elements von Metadaten.</span><span class="sxs-lookup"><span data-stu-id="bb99b-112">The value of an item of metadata.</span></span> <span data-ttu-id="bb99b-113">Wenn das Namensattribut z. b. "Genre" lautet, könnte das Inhalts Attribut "Rock" lauten.</span><span class="sxs-lookup"><span data-stu-id="bb99b-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="bb99b-114">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="bb99b-114">Parent/Child Elements</span></span>



| <span data-ttu-id="bb99b-115">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="bb99b-115">Hierarchy</span></span> | <span data-ttu-id="bb99b-116">Elemente</span><span class="sxs-lookup"><span data-stu-id="bb99b-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="bb99b-117">Parent</span><span class="sxs-lookup"><span data-stu-id="bb99b-117">Parent</span></span>    | [<span data-ttu-id="bb99b-118">head</span><span class="sxs-lookup"><span data-stu-id="bb99b-118">head</span></span>](head-element.md) |
| <span data-ttu-id="bb99b-119">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="bb99b-119">Child</span></span>     | <span data-ttu-id="bb99b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="bb99b-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="bb99b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb99b-121">Remarks</span></span>

<span data-ttu-id="bb99b-122">Der Ersteller einer Windows-Medienwiedergabe Liste kann das Name-Attribut eines Meta-Elements auf eine beliebige Zeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="bb99b-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="bb99b-123">In der folgenden Liste sind einige typische namens Attribute aufgeführt, die in Windows Media-Wiedergabelisten enthalten sind, die von Windows Media Player und anderen Microsoft-Komponenten erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bb99b-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="bb99b-124">Autor</span><span class="sxs-lookup"><span data-stu-id="bb99b-124">Author</span></span>
-   <span data-ttu-id="bb99b-125">Category</span><span class="sxs-lookup"><span data-stu-id="bb99b-125">Category</span></span>
-   <span data-ttu-id="bb99b-126">Genre</span><span class="sxs-lookup"><span data-stu-id="bb99b-126">Genre</span></span>
-   <span data-ttu-id="bb99b-127">UserName</span><span class="sxs-lookup"><span data-stu-id="bb99b-127">UserName</span></span>
-   <span data-ttu-id="bb99b-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="bb99b-128">UserRating</span></span>
-   <span data-ttu-id="bb99b-129">Generator</span><span class="sxs-lookup"><span data-stu-id="bb99b-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="bb99b-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb99b-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="bb99b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb99b-131">Requirements</span></span>



| <span data-ttu-id="bb99b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb99b-132">Requirement</span></span> | <span data-ttu-id="bb99b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="bb99b-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="bb99b-134">Version</span><span class="sxs-lookup"><span data-stu-id="bb99b-134">Version</span></span><br/> | <span data-ttu-id="bb99b-135">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="bb99b-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb99b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb99b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb99b-137">**Head-Element**</span><span class="sxs-lookup"><span data-stu-id="bb99b-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="bb99b-138">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="bb99b-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





