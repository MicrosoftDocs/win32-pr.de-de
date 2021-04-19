---
title: Startmarker-Element
description: Das Startmarker-Element gibt einen Marker an, aus dem Windows Media Player mit dem Rendern des Streams beginnt.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Startmarker-Element, Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370286"
---
# <a name="startmarker-element"></a><span data-ttu-id="f26ba-104">Startmarker-Element</span><span class="sxs-lookup"><span data-stu-id="f26ba-104">STARTMARKER Element</span></span>

<span data-ttu-id="f26ba-105">Das **Startmarker** -Element gibt einen Marker an, aus dem Windows Media Player mit dem Rendern des Streams beginnt.</span><span class="sxs-lookup"><span data-stu-id="f26ba-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="f26ba-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f26ba-106">Attributes</span></span>

<span data-ttu-id="f26ba-107">**Einigen**</span><span class="sxs-lookup"><span data-stu-id="f26ba-107">**NUMBER**</span></span>

<span data-ttu-id="f26ba-108">Die Nummer eines numerischen Markers im Index.</span><span class="sxs-lookup"><span data-stu-id="f26ba-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="f26ba-109">Der Standardwert ist der Anfang von on-Demand-Inhalten oder die aktuelle Position in einem Echtzeitdaten Strom.</span><span class="sxs-lookup"><span data-stu-id="f26ba-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="f26ba-110">**NAME**</span><span class="sxs-lookup"><span data-stu-id="f26ba-110">**NAME**</span></span>

<span data-ttu-id="f26ba-111">Der Name eines benannten Markers im Index.</span><span class="sxs-lookup"><span data-stu-id="f26ba-111">The name of a named marker in the index.</span></span> <span data-ttu-id="f26ba-112">Der Standardwert ist der Anfang von on-Demand-Inhalten oder die aktuelle Position in einem Echtzeitdaten Strom.</span><span class="sxs-lookup"><span data-stu-id="f26ba-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f26ba-113">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="f26ba-113">Parent/Child Elements</span></span>



| <span data-ttu-id="f26ba-114">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f26ba-114">Hierarchy</span></span>       | <span data-ttu-id="f26ba-115">Elemente</span><span class="sxs-lookup"><span data-stu-id="f26ba-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="f26ba-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f26ba-116">Parent elements</span></span> | <span data-ttu-id="f26ba-117">**Eintrag**, **ref**</span><span class="sxs-lookup"><span data-stu-id="f26ba-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="f26ba-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f26ba-118">Child elements</span></span>  | <span data-ttu-id="f26ba-119">Keine</span><span class="sxs-lookup"><span data-stu-id="f26ba-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="f26ba-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f26ba-120">Remarks</span></span>

<span data-ttu-id="f26ba-121">Dieses Element gibt den Marker an, von dem Windows-Media Player das Rendern des Datenstroms beginnen soll, der im übergeordneten **Eintrag** oder **ref** -Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f26ba-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="f26ba-122">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="f26ba-122">**Note**</span></span>

<span data-ttu-id="f26ba-123">Verwenden Sie dieses Element entweder mit dem **Number** -oder dem **Name** -Attribut, jedoch nicht mit beiden.</span><span class="sxs-lookup"><span data-stu-id="f26ba-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="f26ba-124">Ein in einem **ref** -Element definiertes **Startmarker** -Element hat Vorrang vor einem **Startmarker** -Element, das im übergeordneten **Entry** -Element des **ref** -Elements definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f26ba-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="f26ba-125">Ein **Startmarker** -Element hat auch Vorrang vor einem **StartTime** -Element.</span><span class="sxs-lookup"><span data-stu-id="f26ba-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="f26ba-126">Wenn der von einem **Startmarker** -Element angegebene Marker später im Stream als der von einem **endmarkerelement** definierte Marker auftritt, wird kein Inhalt wiedergegeben, aber es wird kein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="f26ba-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="f26ba-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f26ba-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="f26ba-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f26ba-128">Requirements</span></span>



| <span data-ttu-id="f26ba-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f26ba-129">Requirement</span></span> | <span data-ttu-id="f26ba-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f26ba-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="f26ba-131">Version</span><span class="sxs-lookup"><span data-stu-id="f26ba-131">Version</span></span><br/> | <span data-ttu-id="f26ba-132">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="f26ba-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f26ba-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f26ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26ba-134">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="f26ba-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f26ba-135">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="f26ba-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





