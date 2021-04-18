---
title: REPEAT-Element
description: Das Repeat-Element definiert, wie oft Windows Media Player ein oder mehrere Entry-oder ENTRYREF-Elemente wiederholt.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Windows-Element Media Player wiederholen
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371704"
---
# <a name="repeat-element"></a><span data-ttu-id="67b1b-104">REPEAT-Element</span><span class="sxs-lookup"><span data-stu-id="67b1b-104">REPEAT Element</span></span>

<span data-ttu-id="67b1b-105">Das **Repeat** -Element definiert, wie oft Windows Media Player ein oder mehrere **Entry** -oder **ENTRYREF** -Elemente wiederholt.</span><span class="sxs-lookup"><span data-stu-id="67b1b-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="67b1b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="67b1b-106">Attributes</span></span>

<span data-ttu-id="67b1b-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="67b1b-107">**COUNT**</span></span>

<span data-ttu-id="67b1b-108">Eine ganze Zahl, die angibt, wie oft Windows Media Player den **Eintrag** und die **ENTRYREF** -Elemente innerhalb des Gültigkeits Bereichs dieses Elements wiederholt.</span><span class="sxs-lookup"><span data-stu-id="67b1b-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="67b1b-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="67b1b-109">Parent/Child Elements</span></span>



| <span data-ttu-id="67b1b-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="67b1b-110">Hierarchy</span></span>       | <span data-ttu-id="67b1b-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="67b1b-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="67b1b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67b1b-112">Parent elements</span></span> | <span data-ttu-id="67b1b-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="67b1b-113">**ASX**</span></span>                 |
| <span data-ttu-id="67b1b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67b1b-114">Child elements</span></span>  | <span data-ttu-id="67b1b-115">**Eintrag**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="67b1b-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="67b1b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67b1b-116">Remarks</span></span>

<span data-ttu-id="67b1b-117">Dieses Element definiert, wie oft Windows Media Player wiederholt oder durchläuft, die durch die **Entry** -und **ENTRYREF** -Elemente innerhalb des Gültigkeits Bereichs dieses Elements definierten Clips.</span><span class="sxs-lookup"><span data-stu-id="67b1b-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="67b1b-118">Nur das erste **Wiederholungs** Element in einer Metadatei ist gültig. nachfolgende **Wiederholungs** Elemente werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="67b1b-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="67b1b-119">Wenn kein **count** -Attribut definiert ist, wiederholt der Inhalt im zugeordneten **Entry** -Element und im **ENTRYREF** -Element unendlich viele Male.</span><span class="sxs-lookup"><span data-stu-id="67b1b-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="67b1b-120">Der Wert 0 (null) bewirkt, dass Windows Media Player das **Repeat** -Element ignoriert und den Inhalt einmal wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="67b1b-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="67b1b-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67b1b-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="67b1b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67b1b-122">Requirements</span></span>



| <span data-ttu-id="67b1b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67b1b-123">Requirement</span></span> | <span data-ttu-id="67b1b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="67b1b-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="67b1b-125">Version</span><span class="sxs-lookup"><span data-stu-id="67b1b-125">Version</span></span><br/> | <span data-ttu-id="67b1b-126">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="67b1b-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67b1b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67b1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b1b-128">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="67b1b-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="67b1b-129">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="67b1b-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





