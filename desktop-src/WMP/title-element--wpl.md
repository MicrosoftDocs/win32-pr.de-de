---
title: Title-Element (WPL)
description: Das Title-Element gibt einen Titel für die Wiedergabeliste an.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Windows-Media Player des title-Elements (WPL)
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367061"
---
# <a name="title-element-wpl"></a><span data-ttu-id="725b3-104">Title-Element (WPL)</span><span class="sxs-lookup"><span data-stu-id="725b3-104">title Element (WPL)</span></span>

<span data-ttu-id="725b3-105">Das **Title** -Element gibt einen Titel für die Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="725b3-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="725b3-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="725b3-106">Attributes</span></span>

<span data-ttu-id="725b3-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="725b3-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="725b3-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="725b3-108">Parent/Child Elements</span></span>



| <span data-ttu-id="725b3-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="725b3-109">Hierarchy</span></span> | <span data-ttu-id="725b3-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="725b3-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="725b3-111">Parent</span><span class="sxs-lookup"><span data-stu-id="725b3-111">Parent</span></span>    | [<span data-ttu-id="725b3-112">head</span><span class="sxs-lookup"><span data-stu-id="725b3-112">head</span></span>](head-element.md) |
| <span data-ttu-id="725b3-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="725b3-113">Child</span></span>     | <span data-ttu-id="725b3-114">Keine</span><span class="sxs-lookup"><span data-stu-id="725b3-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="725b3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="725b3-115">Remarks</span></span>

<span data-ttu-id="725b3-116">Wenn Sie einen Titel für eine Windows Media-Wiedergabeliste (WPL) auswählen, sollten Sie Bedenken, dass der Inhalt der Wiedergabeliste dynamisch sein kann.</span><span class="sxs-lookup"><span data-stu-id="725b3-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="725b3-117">Ein guter Ansatz besteht darin, den Titel auf der Logik in den **Argument** Elementen zu basieren, da der Inhalt der Wiedergabeliste von diesem definiert wird.</span><span class="sxs-lookup"><span data-stu-id="725b3-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="725b3-118">Beispiele hierfür sind "meine bevorzugten Rock-Lieder aus 1966" oder "Tanzlieder, die ich vor kurzem nicht gespielt habe".</span><span class="sxs-lookup"><span data-stu-id="725b3-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="725b3-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="725b3-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="725b3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="725b3-120">Requirements</span></span>



| <span data-ttu-id="725b3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="725b3-121">Requirement</span></span> | <span data-ttu-id="725b3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="725b3-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="725b3-123">Version</span><span class="sxs-lookup"><span data-stu-id="725b3-123">Version</span></span><br/> | <span data-ttu-id="725b3-124">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="725b3-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="725b3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="725b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725b3-126">**Argument-Element**</span><span class="sxs-lookup"><span data-stu-id="725b3-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="725b3-127">**Head-Element**</span><span class="sxs-lookup"><span data-stu-id="725b3-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="725b3-128">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="725b3-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





