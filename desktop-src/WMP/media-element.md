---
title: Media-Element
description: Das Media-Element gibt eines der Medienelemente in einer Wiedergabeliste an.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Windows-Media Player für Medien Element
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361263"
---
# <a name="media-element"></a><span data-ttu-id="67163-104">Media-Element</span><span class="sxs-lookup"><span data-stu-id="67163-104">media Element</span></span>

<span data-ttu-id="67163-105">Das **Media** -Element gibt eines der Medienelemente in einer Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="67163-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="67163-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="67163-106">Attributes</span></span>



| <span data-ttu-id="67163-107">Begriff</span><span class="sxs-lookup"><span data-stu-id="67163-107">Term</span></span>                                                                                                                       | <span data-ttu-id="67163-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67163-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67163-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="67163-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="67163-110">Die URL eines Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="67163-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="67163-111"><span id="cid"></span><span id="CID"></span>**zid**</span><span class="sxs-lookup"><span data-stu-id="67163-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="67163-112">Die Inhalts-ID, die für dieses Medien Element eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="67163-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="67163-113"><span id="tid"></span><span id="TID"></span>**Drüse**</span><span class="sxs-lookup"><span data-stu-id="67163-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="67163-114">Die Nachverfolgungs-ID, die verwendet werden kann, um das Datei System Objekt für dieses Medien Element nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="67163-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="67163-115">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="67163-115">Parent/Child Elements</span></span>



| <span data-ttu-id="67163-116">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="67163-116">Hierarchy</span></span> | <span data-ttu-id="67163-117">Elemente</span><span class="sxs-lookup"><span data-stu-id="67163-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="67163-118">Parent</span><span class="sxs-lookup"><span data-stu-id="67163-118">Parent</span></span>    | [<span data-ttu-id="67163-119">Seq</span><span class="sxs-lookup"><span data-stu-id="67163-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="67163-120">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="67163-120">Child</span></span>     | <span data-ttu-id="67163-121">Keine</span><span class="sxs-lookup"><span data-stu-id="67163-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="67163-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67163-122">Remarks</span></span>

<span data-ttu-id="67163-123">Das **CID** -Attribut (die Inhalts-ID) wird durch den Windows-Media Player als Möglichkeit zum eindeutigen Identifizieren eines Medien Inhalts aufgefüllt, auch wenn seine Metadatenattribute geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="67163-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="67163-124">Dies ermöglicht die gemeinsame Nutzung von Wiedergabelisten auf allen Computern, da der Inhalt auf einem anderen Computer identifiziert werden kann und der Pfad zu ihm von der Windows Media-Wiedergabeliste automatisch repariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="67163-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="67163-125">Das **TID** -Attribut (die Überwachungs-ID) verwendet das Windows-Dateisystem, um den Pfad zu den Medien automatisch zu reparieren, wenn der Name oder Speicherort der Datei geändert wird.</span><span class="sxs-lookup"><span data-stu-id="67163-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="67163-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67163-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="67163-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67163-127">Requirements</span></span>



| <span data-ttu-id="67163-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67163-128">Requirement</span></span> | <span data-ttu-id="67163-129">Wert</span><span class="sxs-lookup"><span data-stu-id="67163-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="67163-130">Version</span><span class="sxs-lookup"><span data-stu-id="67163-130">Version</span></span><br/> | <span data-ttu-id="67163-131">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="67163-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67163-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67163-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67163-133">**ENQ-Element**</span><span class="sxs-lookup"><span data-stu-id="67163-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="67163-134">**Referenz zu Windows Media-Wiedergabelisten Elementen**</span><span class="sxs-lookup"><span data-stu-id="67163-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





