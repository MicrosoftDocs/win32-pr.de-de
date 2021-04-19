---
title: Duration-Element
description: Mit dem Duration-Element wird die Zeitspanne definiert, mit der Windows Media Player den zugehörigen Wiedergabelisten Eintrag render.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Fenster "Duration"-Element Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371711"
---
# <a name="duration-element"></a><span data-ttu-id="f43f8-104">Duration-Element</span><span class="sxs-lookup"><span data-stu-id="f43f8-104">DURATION Element</span></span>

<span data-ttu-id="f43f8-105">Mit dem **Duration** -Element wird die Zeitspanne definiert, mit der Windows Media Player den zugehörigen Wiedergabelisten Eintrag render.</span><span class="sxs-lookup"><span data-stu-id="f43f8-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="f43f8-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f43f8-106">Attributes</span></span>

<span data-ttu-id="f43f8-107">**Wert** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="f43f8-107">**VALUE** (required)</span></span>

<span data-ttu-id="f43f8-108">Die Zeitspanne in Stunden, Minuten, Sekunden und Hundertstel Sekunden, in der ein Eintrag von Windows Media Player gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="f43f8-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="f43f8-109">Der Standardwert ist die gesamte Länge des Eintrags.</span><span class="sxs-lookup"><span data-stu-id="f43f8-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="f43f8-110">Wenn es sich bei dem Eintrag um eine Grafikdatei handelt, muss ein Duration-Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f43f8-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f43f8-111">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="f43f8-111">Parent/Child Elements</span></span>



| <span data-ttu-id="f43f8-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="f43f8-112">Hierarchy</span></span>       | <span data-ttu-id="f43f8-113">Elemente</span><span class="sxs-lookup"><span data-stu-id="f43f8-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="f43f8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f43f8-114">Parent elements</span></span> | <span data-ttu-id="f43f8-115">**Eintrag**, **ref**</span><span class="sxs-lookup"><span data-stu-id="f43f8-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="f43f8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f43f8-116">Child elements</span></span>  | <span data-ttu-id="f43f8-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f43f8-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="f43f8-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f43f8-118">Remarks</span></span>

<span data-ttu-id="f43f8-119">Dieses Element definiert die Zeitspanne, für die ein Stream gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f43f8-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="f43f8-120">Wenn das **value** -Attribut die Länge des Inhaltsstreams überschreitet, wird der Stream am normalen Endpunkt beendet.</span><span class="sxs-lookup"><span data-stu-id="f43f8-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="f43f8-121">Dieses Element kann entweder in einem **ref** -Element oder in einem **Entry** -Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="f43f8-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="f43f8-122">Ein Duration-Element, das in einem **ref** -Element definiert ist, überschreibt jedoch ein **Duration** -Element, das im übergeordneten **Entry** -Element des **ref** -Elements</span><span class="sxs-lookup"><span data-stu-id="f43f8-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="f43f8-123">Das **Duration** -Element überschreibt ein **previewduration** -Element.</span><span class="sxs-lookup"><span data-stu-id="f43f8-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="f43f8-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f43f8-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="f43f8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f43f8-125">Requirements</span></span>



| <span data-ttu-id="f43f8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f43f8-126">Requirement</span></span> | <span data-ttu-id="f43f8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f43f8-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f43f8-128">Version</span><span class="sxs-lookup"><span data-stu-id="f43f8-128">Version</span></span><br/> | <span data-ttu-id="f43f8-129">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f43f8-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f43f8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f43f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f43f8-131">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="f43f8-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="f43f8-132">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="f43f8-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





