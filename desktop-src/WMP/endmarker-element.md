---
title: Endmarker-Element
description: Das Endmarker-Element gibt einen Marker an, bei dem Windows Media Player das Rendern des Streams beendet.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Endmarker-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367188"
---
# <a name="endmarker-element"></a><span data-ttu-id="b3c75-104">Endmarker-Element</span><span class="sxs-lookup"><span data-stu-id="b3c75-104">ENDMARKER Element</span></span>

<span data-ttu-id="b3c75-105">Das **Endmarker** -Element gibt einen Marker an, bei dem Windows Media Player das Rendern des Streams beendet.</span><span class="sxs-lookup"><span data-stu-id="b3c75-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="b3c75-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="b3c75-106">Attributes</span></span>

<span data-ttu-id="b3c75-107">**Einigen**</span><span class="sxs-lookup"><span data-stu-id="b3c75-107">**NUMBER**</span></span>

<span data-ttu-id="b3c75-108">Die Nummer eines numerischen Markers im Index.</span><span class="sxs-lookup"><span data-stu-id="b3c75-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="b3c75-109">Der Standardwert ist das Ende des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="b3c75-109">The default value is the end of the content.</span></span>

<span data-ttu-id="b3c75-110">**NAME**</span><span class="sxs-lookup"><span data-stu-id="b3c75-110">**NAME**</span></span>

<span data-ttu-id="b3c75-111">Der Name eines benannten Markers im Index.</span><span class="sxs-lookup"><span data-stu-id="b3c75-111">The name of a named marker in the index.</span></span> <span data-ttu-id="b3c75-112">Der Standardwert ist das Ende des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="b3c75-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b3c75-113">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="b3c75-113">Parent/Child Elements</span></span>



| <span data-ttu-id="b3c75-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="b3c75-114">Hierarchy</span></span>       | <span data-ttu-id="b3c75-115">Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c75-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="b3c75-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c75-116">Parent elements</span></span> | <span data-ttu-id="b3c75-117">**Eintrag**, **ref**</span><span class="sxs-lookup"><span data-stu-id="b3c75-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="b3c75-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b3c75-118">Child elements</span></span>  | <span data-ttu-id="b3c75-119">Keine</span><span class="sxs-lookup"><span data-stu-id="b3c75-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="b3c75-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3c75-120">Remarks</span></span>

<span data-ttu-id="b3c75-121">Dieses Element gibt den Marker an, in dem Windows Media Player das Rendern des Datenstroms beendet, der im übergeordneten **Eintrag** oder **ref** -Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b3c75-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="b3c75-122">Hinweis</span><span class="sxs-lookup"><span data-stu-id="b3c75-122">Note</span></span>

<span data-ttu-id="b3c75-123">Verwenden Sie das **Endmarker** -Element entweder mit dem **Number** -oder dem **Name** -Attribut, jedoch nicht mit beiden.</span><span class="sxs-lookup"><span data-stu-id="b3c75-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="b3c75-124">Im Vorschaumodus wird durch das Erreichen eines endmarkers die Vorschau beendet, auch wenn die vom **previewduration** -Element angegebene Zeit nicht verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="b3c75-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="b3c75-125">Das **Endmarker** -Element hat auch Vorrang vor dem **Duration** -Element.</span><span class="sxs-lookup"><span data-stu-id="b3c75-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="b3c75-126">Ein in einem **ref** -Element definiertes **endmarkerelement** hat Vorrang vor einem **Endmarker** , der im übergeordneten **Entry** -Element des **ref** -Elements definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b3c75-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="b3c75-127">Wenn der von einem **endmarkerelement** angegebene Marker vor dem durch ein **Startmarker** -Element definierten Marker auftritt, wird kein Inhalt abgespielt, es wird jedoch kein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="b3c75-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="b3c75-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3c75-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="b3c75-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3c75-129">Requirements</span></span>



| <span data-ttu-id="b3c75-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3c75-130">Requirement</span></span> | <span data-ttu-id="b3c75-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b3c75-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b3c75-132">Version</span><span class="sxs-lookup"><span data-stu-id="b3c75-132">Version</span></span><br/> | <span data-ttu-id="b3c75-133">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="b3c75-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3c75-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3c75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c75-135">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="b3c75-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b3c75-136">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="b3c75-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





