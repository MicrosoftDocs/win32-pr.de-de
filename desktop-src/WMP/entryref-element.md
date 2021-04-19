---
title: ENTRYREF-Element
description: Das ENTRYREF-Element verweist auf die Eintrags Elemente in einer externen Metadatei.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Fenster "ENTRYREF-Element" Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369570"
---
# <a name="entryref-element"></a><span data-ttu-id="f412f-104">ENTRYREF-Element</span><span class="sxs-lookup"><span data-stu-id="f412f-104">ENTRYREF Element</span></span>

<span data-ttu-id="f412f-105">Das **ENTRYREF** -Element verweist auf die **Eintrags** Elemente in einer externen Metadatei.</span><span class="sxs-lookup"><span data-stu-id="f412f-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="f412f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f412f-106">Attributes</span></span>

<span data-ttu-id="f412f-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f412f-107">**HREF** (required)</span></span>

<span data-ttu-id="f412f-108">URL zu einer Metadatei, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f412f-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="f412f-109">**Clientbind**</span><span class="sxs-lookup"><span data-stu-id="f412f-109">**CLIENTBIND**</span></span>

<span data-ttu-id="f412f-110">Dieses Attribut wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f412f-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f412f-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="f412f-111">Parent/Child Elements</span></span>



| <span data-ttu-id="f412f-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f412f-112">Hierarchy</span></span>       | <span data-ttu-id="f412f-113">Elemente</span><span class="sxs-lookup"><span data-stu-id="f412f-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="f412f-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f412f-114">Parent elements</span></span> | <span data-ttu-id="f412f-115">**ASX**, **Ereignis**, **Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="f412f-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="f412f-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f412f-116">Child elements</span></span>  | <span data-ttu-id="f412f-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f412f-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="f412f-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f412f-118">Remarks</span></span>

<span data-ttu-id="f412f-119">Dieses Element verweist auf den Inhalt einer externen Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="f412f-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="f412f-120">Windows Media Player verarbeitet die **Einstiegs** Elemente der Metadatei, auf die verwiesen wird, als wären Sie in der primären Metadatendatei an der Position des **ENTRYREF** -Elements enthalten.</span><span class="sxs-lookup"><span data-stu-id="f412f-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="f412f-121">Allerdings werden alle **Eingabe** Elemente in der Metadatei, auf die verwiesen wird, ausgelassen, deren **skipifref** -Attribut auf "yes" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f412f-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="f412f-122">In Windows Media Player 7,0, 7,1 und Windows Media Player für Windows XP werden alle **ENTRYREF** -Elemente in der Metadatei ignoriert, auf die verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="f412f-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="f412f-123">Folglich können Metadateien nur eine Ebene tief verschachtelt werden, wenn diese Versionen des Players verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f412f-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="f412f-124">Windows Media Player ignoriert auch das Element " **ASX** " in der Datei, auf die verwiesen wird, sowie die zugehörigen Attribute.</span><span class="sxs-lookup"><span data-stu-id="f412f-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="f412f-125">Windows Media Player 9 oder höher unterstützt das Schachteln von Metadateien mit einer Tiefe von bis zu fünf Ebenen.</span><span class="sxs-lookup"><span data-stu-id="f412f-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="f412f-126">Die im **href** -Attribut angegebene URL wird zur Basis-URL für alle relativen URLs in der externen Metadatendatei.</span><span class="sxs-lookup"><span data-stu-id="f412f-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="f412f-127">Diese URL wird verwendet, wenn ein Eintrag aus der externen Metadatei abgespielt wird und der Benutzer Sie der Bibliothek hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f412f-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="f412f-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f412f-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="f412f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f412f-129">Requirements</span></span>



| <span data-ttu-id="f412f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f412f-130">Requirement</span></span> | <span data-ttu-id="f412f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f412f-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="f412f-132">Version</span><span class="sxs-lookup"><span data-stu-id="f412f-132">Version</span></span><br/> | <span data-ttu-id="f412f-133">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="f412f-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f412f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f412f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f412f-135">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="f412f-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f412f-136">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="f412f-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





