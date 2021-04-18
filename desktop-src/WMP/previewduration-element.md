---
title: Previewduration-Element
description: Das previewduration-Element definiert die Zeitspanne, während der ein Clip im Vorschaumodus abgespielt wird.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Previewduration-Element, Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364618"
---
# <a name="previewduration-element"></a><span data-ttu-id="f9aa5-104">Previewduration-Element</span><span class="sxs-lookup"><span data-stu-id="f9aa5-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="f9aa5-105">Das **previewduration** -Element definiert die Zeitspanne, während der ein Clip im Vorschaumodus abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="f9aa5-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9aa5-106">Attributes</span></span>

<span data-ttu-id="f9aa5-107">**Wert** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f9aa5-107">**VALUE** (required)</span></span>

<span data-ttu-id="f9aa5-108">Zeitspanne (in Stunden, Minuten, Sekunden und Hundertstel Sekunden), die der Clip im Vorschaumodus abspielt.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f9aa5-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="f9aa5-109">Parent/Child Elements</span></span>



| <span data-ttu-id="f9aa5-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f9aa5-110">Hierarchy</span></span>       | <span data-ttu-id="f9aa5-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="f9aa5-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="f9aa5-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9aa5-112">Parent elements</span></span> | <span data-ttu-id="f9aa5-113">**ASX**, **Eintrag**, **ref**</span><span class="sxs-lookup"><span data-stu-id="f9aa5-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="f9aa5-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9aa5-114">Child elements</span></span>  | <span data-ttu-id="f9aa5-115">Keine</span><span class="sxs-lookup"><span data-stu-id="f9aa5-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="f9aa5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9aa5-116">Remarks</span></span>

<span data-ttu-id="f9aa5-117">Dieses Element definiert die Zeitspanne, in der ein Clip im Vorschaumodus abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="f9aa5-118">Wenn dieses Element in einem **Entry** -Element oder einem **ref** -Element angezeigt wird, gilt es für den Clip, der durch dieses Element definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="f9aa5-119">Wenn Sie im Gültigkeitsbereich eines **ASX** -Elements angezeigt wird, gilt sie für jeden Clip in der Metadatei.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="f9aa5-120">Ein **previewduration** -Element in einem **ref** - **Element hat Vorrang** vor einem Element in einem Entry-Element und hat entweder Vorrang vor einem **previewduration** -Element in einem **ASX** -Element.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="f9aa5-121">Wenn kein **previewduration** -Element für einen Clip definiert ist, beträgt die Standard Vorschau Zeit 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="f9aa5-122">Wenn ein **StartTime** -oder **Startmarker** -Element für den Clip vorhanden ist, rendert Windows Media Player den Clip, beginnend an dem Punkt, der von einem dieser Elemente definiert wurde. Andernfalls wird Sie am Anfang des Clips gerendert.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="f9aa5-123">Der Clip wird normal beendet, wenn er kürzer ist als die Zeit, die vom **previewduration** -Element definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="f9aa5-124">Das **Duration** -Element überschreibt ein **previewduration** -Element.</span><span class="sxs-lookup"><span data-stu-id="f9aa5-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="f9aa5-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9aa5-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="f9aa5-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9aa5-126">Requirements</span></span>



| <span data-ttu-id="f9aa5-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9aa5-127">Requirement</span></span> | <span data-ttu-id="f9aa5-128">Wert</span><span class="sxs-lookup"><span data-stu-id="f9aa5-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="f9aa5-129">Version</span><span class="sxs-lookup"><span data-stu-id="f9aa5-129">Version</span></span><br/> | <span data-ttu-id="f9aa5-130">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="f9aa5-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9aa5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9aa5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9aa5-132">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="f9aa5-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f9aa5-133">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="f9aa5-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





