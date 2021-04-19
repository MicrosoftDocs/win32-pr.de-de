---
title: Title-Element (Metadatei)
description: Das Title-Element definiert eine Text Zeichenfolge, die den Titel für ein ASX-oder Entry-Element angibt.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Title-Element (Metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356027"
---
# <a name="title-element-metafile"></a><span data-ttu-id="8fe83-104">Title-Element (Metadatei)</span><span class="sxs-lookup"><span data-stu-id="8fe83-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="8fe83-105">Das **Title** -Element definiert eine Text Zeichenfolge, die den Titel für ein **ASX** -oder **Entry** -Element angibt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="8fe83-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="8fe83-106">Attributes</span></span>

<span data-ttu-id="8fe83-107">Dieses Element weist keine Attribute auf.</span><span class="sxs-lookup"><span data-stu-id="8fe83-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8fe83-108">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="8fe83-108">Parent/Child Elements</span></span>



| <span data-ttu-id="8fe83-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8fe83-109">Hierarchy</span></span>       | <span data-ttu-id="8fe83-110">Elemente</span><span class="sxs-lookup"><span data-stu-id="8fe83-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="8fe83-111">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fe83-111">Parent elements</span></span> | <span data-ttu-id="8fe83-112">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="8fe83-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="8fe83-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8fe83-113">Child elements</span></span>  | <span data-ttu-id="8fe83-114">Keine</span><span class="sxs-lookup"><span data-stu-id="8fe83-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8fe83-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fe83-115">Remarks</span></span>

<span data-ttu-id="8fe83-116">Dieses Element definiert eine Text Zeichenfolge, die den Titel eines **ASX** -oder **Entry** -Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="8fe83-117">Der Titel wird im Anzeigebereich und im **Eigenschaften** Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="8fe83-118">Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird der Text als **Anzeige** Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="8fe83-119">Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als **Clip** Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="8fe83-120">Wenn ein **morumfo** -Element auch mit dem zugeordneten (übergeordneten) Element verwendet wird, ist dies der Titeltext, auf den der Benutzer klickt, um auf die im **Moran FO** -Element definierte URL zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="8fe83-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="8fe83-121">Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Title** -Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="8fe83-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="8fe83-122">Mehrere **Titel** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8fe83-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="8fe83-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fe83-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="8fe83-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fe83-124">Requirements</span></span>



| <span data-ttu-id="8fe83-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fe83-125">Requirement</span></span> | <span data-ttu-id="8fe83-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8fe83-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="8fe83-127">Version</span><span class="sxs-lookup"><span data-stu-id="8fe83-127">Version</span></span><br/> | <span data-ttu-id="8fe83-128">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="8fe83-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fe83-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fe83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe83-130">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="8fe83-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8fe83-131">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="8fe83-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





