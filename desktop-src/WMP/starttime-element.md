---
title: StartTime-Element
description: Das StartTime-Element definiert einen Zeit Index, von dem aus Windows Media Player das Rendern des Streams startet.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- StartTime-Element Fenster Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366952"
---
# <a name="starttime-element"></a><span data-ttu-id="8d52e-104">StartTime-Element</span><span class="sxs-lookup"><span data-stu-id="8d52e-104">STARTTIME Element</span></span>

<span data-ttu-id="8d52e-105">Das **StartTime** -Element definiert einen Zeit Index, von dem aus Windows Media Player das Rendern des Streams startet.</span><span class="sxs-lookup"><span data-stu-id="8d52e-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="8d52e-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d52e-106">Attributes</span></span>

<span data-ttu-id="8d52e-107">**Wert** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="8d52e-107">**VALUE** (required)</span></span>

<span data-ttu-id="8d52e-108">Der Zeit Index (in Stunden, Minuten, Sekunden und Hundertstel Sekunden), aus dem Windows Media Player mit der Wiedergabe eines Datenstroms beginnt, der im zugeordneten Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d52e-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8d52e-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="8d52e-109">Parent/Child Elements</span></span>



| <span data-ttu-id="8d52e-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="8d52e-110">Hierarchy</span></span>       | <span data-ttu-id="8d52e-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="8d52e-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="8d52e-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d52e-112">Parent elements</span></span> | <span data-ttu-id="8d52e-113">**Eintrag**, **ref**</span><span class="sxs-lookup"><span data-stu-id="8d52e-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="8d52e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d52e-114">Child elements</span></span>  | <span data-ttu-id="8d52e-115">Keine</span><span class="sxs-lookup"><span data-stu-id="8d52e-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8d52e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d52e-116">Remarks</span></span>

<span data-ttu-id="8d52e-117">Dieses Element definiert einen Zeit Index in den Inhalt, in dem Windows Media Player das Rendern des Streams starten soll.</span><span class="sxs-lookup"><span data-stu-id="8d52e-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="8d52e-118">Dieses Element kann nur mit gespeicherten on-Demand-Inhalten verwendet werden, die indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="8d52e-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="8d52e-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d52e-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="8d52e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d52e-120">Requirements</span></span>



| <span data-ttu-id="8d52e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d52e-121">Requirement</span></span> | <span data-ttu-id="8d52e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8d52e-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="8d52e-123">Version</span><span class="sxs-lookup"><span data-stu-id="8d52e-123">Version</span></span><br/> | <span data-ttu-id="8d52e-124">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d52e-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d52e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d52e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d52e-126">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="8d52e-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8d52e-127">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="8d52e-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





