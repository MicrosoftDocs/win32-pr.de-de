---
title: Abstract-Element
description: Das abstrakte Element enthält Text, der den zugeordneten ASX, das Banner oder das Einstiegs Element beschreibt.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Abstrakte Element Fenster Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371247"
---
# <a name="abstract-element"></a><span data-ttu-id="019ec-104">Abstract-Element</span><span class="sxs-lookup"><span data-stu-id="019ec-104">ABSTRACT Element</span></span>

<span data-ttu-id="019ec-105">Das **abstrakte** Element enthält Text, der den zugeordneten **ASX**, das **Banner** oder das **Einstiegs** Element beschreibt.</span><span class="sxs-lookup"><span data-stu-id="019ec-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="019ec-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="019ec-106">Attributes</span></span>

<span data-ttu-id="019ec-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="019ec-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="019ec-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="019ec-108">Parent/Child Elements</span></span>



| <span data-ttu-id="019ec-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="019ec-109">Hierarchy</span></span> | <span data-ttu-id="019ec-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="019ec-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="019ec-111">Parent</span><span class="sxs-lookup"><span data-stu-id="019ec-111">Parent</span></span>    | <span data-ttu-id="019ec-112">**ASX**, **Eintrag**, **Banner**</span><span class="sxs-lookup"><span data-stu-id="019ec-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="019ec-113">Untergeordnet</span><span class="sxs-lookup"><span data-stu-id="019ec-113">Child</span></span>     | <span data-ttu-id="019ec-114">Keine</span><span class="sxs-lookup"><span data-stu-id="019ec-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="019ec-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="019ec-115">Remarks</span></span>

<span data-ttu-id="019ec-116">Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird der Text als QuickInfo angezeigt, wenn mit dem Mauszeiger auf den Show-Titel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="019ec-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="019ec-117">Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als QuickInfo angezeigt, wenn mit dem Mauszeiger auf den Clip Titel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="019ec-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="019ec-118">Wenn dieses Element innerhalb eines **Banner** Elements angezeigt wird, wird der Text als QuickInfo für die Banner Grafik angezeigt.</span><span class="sxs-lookup"><span data-stu-id="019ec-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="019ec-119">Verwenden Sie nur ein **abstraktes** Element pro Bereich.</span><span class="sxs-lookup"><span data-stu-id="019ec-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="019ec-120">Wenn eine Metadatendatei verarbeitet wird, wird nur das erste **abstrakte** Element innerhalb des Gültigkeits Bereichs eines anderen Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="019ec-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="019ec-121">Alle nachfolgenden **abstrakten** Elemente in diesem Bereich werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="019ec-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="019ec-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="019ec-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="019ec-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="019ec-123">Requirements</span></span>



| <span data-ttu-id="019ec-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="019ec-124">Requirement</span></span> | <span data-ttu-id="019ec-125">Wert</span><span class="sxs-lookup"><span data-stu-id="019ec-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="019ec-126">Version</span><span class="sxs-lookup"><span data-stu-id="019ec-126">Version</span></span><br/> | <span data-ttu-id="019ec-127">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="019ec-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="019ec-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="019ec-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019ec-129">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="019ec-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="019ec-130">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="019ec-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





