---
title: Author-Element
description: Das Author-Element enthält den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Fenster "Author Element Windows Media Player"
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357954"
---
# <a name="author-element"></a><span data-ttu-id="d1c8f-104">Author-Element</span><span class="sxs-lookup"><span data-stu-id="d1c8f-104">AUTHOR Element</span></span>

<span data-ttu-id="d1c8f-105">Das **Author** -Element enthält den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="d1c8f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1c8f-106">Attributes</span></span>

<span data-ttu-id="d1c8f-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d1c8f-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="d1c8f-108">Parent/Child Elements</span></span>



| <span data-ttu-id="d1c8f-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d1c8f-109">Hierarchy</span></span>       | <span data-ttu-id="d1c8f-110">Element</span><span class="sxs-lookup"><span data-stu-id="d1c8f-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="d1c8f-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1c8f-111">Parent elements</span></span> | <span data-ttu-id="d1c8f-112">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="d1c8f-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="d1c8f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1c8f-113">Child elements</span></span>  | <span data-ttu-id="d1c8f-114">Keine</span><span class="sxs-lookup"><span data-stu-id="d1c8f-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="d1c8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1c8f-115">Remarks</span></span>

<span data-ttu-id="d1c8f-116">Dieses Element enthält eine Text Zeichenfolge, die den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips darstellt.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="d1c8f-117">Sie können das **Author** -Element innerhalb des **ASX** -Elements und innerhalb der **Entry** -Elemente verwenden.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="d1c8f-118">Wenn dieses Element im Element " **ASX** " angezeigt wird, wird der Text als "Informationen **anzeigen** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="d1c8f-119">Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als Clip-Autor angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="d1c8f-120">Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Author** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="d1c8f-121">Mehrere **Autoren** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1c8f-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="d1c8f-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1c8f-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="d1c8f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1c8f-123">Requirements</span></span>



| <span data-ttu-id="d1c8f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1c8f-124">Requirement</span></span> | <span data-ttu-id="d1c8f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d1c8f-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d1c8f-126">Version</span><span class="sxs-lookup"><span data-stu-id="d1c8f-126">Version</span></span><br/> | <span data-ttu-id="d1c8f-127">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="d1c8f-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1c8f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1c8f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c8f-129">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="d1c8f-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d1c8f-130">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="d1c8f-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





