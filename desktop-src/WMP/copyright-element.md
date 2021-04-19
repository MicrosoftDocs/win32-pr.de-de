---
title: Copyright-Element (msfeeds. h)
description: Das Copyright-Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein ASX-oder Entry-Element angibt.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Copyright Element-Fenster Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358640"
---
# <a name="copyright-element"></a><span data-ttu-id="da23d-104">Copyright-Element</span><span class="sxs-lookup"><span data-stu-id="da23d-104">COPYRIGHT Element</span></span>

<span data-ttu-id="da23d-105">Das **Copyright** -Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein **ASX** -oder **Entry** -Element angibt.</span><span class="sxs-lookup"><span data-stu-id="da23d-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="da23d-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="da23d-106">Attributes</span></span>

<span data-ttu-id="da23d-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="da23d-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="da23d-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="da23d-108">Parent/Child Elements</span></span>



| <span data-ttu-id="da23d-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="da23d-109">Hierarchy</span></span>       | <span data-ttu-id="da23d-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="da23d-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="da23d-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da23d-111">Parent elements</span></span> | <span data-ttu-id="da23d-112">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="da23d-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="da23d-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da23d-113">Child elements</span></span>  | <span data-ttu-id="da23d-114">Keine</span><span class="sxs-lookup"><span data-stu-id="da23d-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="da23d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da23d-115">Remarks</span></span>

<span data-ttu-id="da23d-116">Dieses Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein **ASX** -oder **Entry** -Element angibt.</span><span class="sxs-lookup"><span data-stu-id="da23d-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="da23d-117">Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird die Copyright Zeichenfolge nur als **Anzeige** Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da23d-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="da23d-118">Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als Clip Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da23d-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="da23d-119">Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Copyright** Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="da23d-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="da23d-120">Mehrere **Copyright** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da23d-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="da23d-121">Die Zeichen für Copyright-und Marken Registrierungs Symbole (oder) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist.</span><span class="sxs-lookup"><span data-stu-id="da23d-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="da23d-122">Wenn Sie in diesem Fall eines dieser Symbole für alle Benutzer ordnungsgemäß anzeigen möchten, können Sie stattdessen die ASCII-Entsprechungen (c) und (R) verwenden.</span><span class="sxs-lookup"><span data-stu-id="da23d-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="da23d-123">Wenn die Metadatendatei mit UTF-8 codiert wird, werden Copyright-und Marken Symbole ordnungsgemäß angezeigt.</span><span class="sxs-lookup"><span data-stu-id="da23d-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="da23d-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da23d-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="da23d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da23d-125">Requirements</span></span>



| <span data-ttu-id="da23d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da23d-126">Requirement</span></span> | <span data-ttu-id="da23d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="da23d-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da23d-128">Version</span><span class="sxs-lookup"><span data-stu-id="da23d-128">Version</span></span><br/> | <span data-ttu-id="da23d-129">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="da23d-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="da23d-130">Header</span><span class="sxs-lookup"><span data-stu-id="da23d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="da23d-131"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="da23d-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da23d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da23d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da23d-133">**Hinzufügen von Copyright Zeichen zu Metafiles**</span><span class="sxs-lookup"><span data-stu-id="da23d-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="da23d-134">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="da23d-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="da23d-135">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="da23d-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





