---
description: Das Effect-Element definiert ein Audio- oder Videoeffektobjekt. Ein Effekt wird auf einen einzelnen Stream angewendet (z. B. eine Komposition, ein Titel oder eine Quelle).
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: effect-Element (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908658"
---
# <a name="effect-element"></a><span data-ttu-id="f399a-104">effect-Element</span><span class="sxs-lookup"><span data-stu-id="f399a-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="f399a-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f399a-105">\[Deprecated.</span></span> <span data-ttu-id="f399a-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f399a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f399a-107">Das `effect` -Element definiert ein Audio- oder Videoeffektobjekt.</span><span class="sxs-lookup"><span data-stu-id="f399a-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="f399a-108">Ein Effekt wird auf einen einzelnen Stream angewendet (z. B. eine Komposition, ein Titel oder eine Quelle).</span><span class="sxs-lookup"><span data-stu-id="f399a-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="f399a-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="f399a-109">Attributes</span></span>

<span data-ttu-id="f399a-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="f399a-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="f399a-111">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="f399a-111">Parent/Child Information</span></span>



| <span data-ttu-id="f399a-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f399a-112">Label</span></span> | <span data-ttu-id="f399a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f399a-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f399a-114">Parent</span><span class="sxs-lookup"><span data-stu-id="f399a-114">Parent</span></span>   | <span data-ttu-id="f399a-115">[**Zusammengesetzt,**](composite-element.md) [**Gruppe,**](group-element.md) [**Clip,**](clip-element.md) [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="f399a-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="f399a-116">Children</span><span class="sxs-lookup"><span data-stu-id="f399a-116">Children</span></span> | [<span data-ttu-id="f399a-117">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="f399a-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f399a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f399a-118">Remarks</span></span>

<span data-ttu-id="f399a-119">Das **clsid-Attribut** gibt das Unterobjekt an, das den Effekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="f399a-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="f399a-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f399a-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="f399a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f399a-121">Requirements</span></span>



| <span data-ttu-id="f399a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f399a-122">Requirement</span></span> | <span data-ttu-id="f399a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f399a-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f399a-124">Header</span><span class="sxs-lookup"><span data-stu-id="f399a-124">Header</span></span><br/> | <dl> <span data-ttu-id="f399a-125"><dt>Gdipluseffects.h</dt></span><span class="sxs-lookup"><span data-stu-id="f399a-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f399a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f399a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f399a-127">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="f399a-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




