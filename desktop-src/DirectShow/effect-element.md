---
description: Das Effect-Element definiert ein audiobild oder Videoeffekt Objekt. Ein Effekt wird auf einen einzelnen Stream (z. b. eine Komposition, eine Spur oder eine Quelle) angewendet.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Effect-Element (gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371292"
---
# <a name="effect-element"></a><span data-ttu-id="cfb9a-104">Effect-Element</span><span class="sxs-lookup"><span data-stu-id="cfb9a-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="cfb9a-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cfb9a-105">\[Deprecated.</span></span> <span data-ttu-id="cfb9a-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="cfb9a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cfb9a-107">Das `effect` -Element definiert ein audiobild oder Videoeffekt Objekt.</span><span class="sxs-lookup"><span data-stu-id="cfb9a-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="cfb9a-108">Ein Effekt wird auf einen einzelnen Stream (z. b. eine Komposition, eine Spur oder eine Quelle) angewendet.</span><span class="sxs-lookup"><span data-stu-id="cfb9a-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="cfb9a-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="cfb9a-109">Attributes</span></span>

<span data-ttu-id="cfb9a-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Start**](start-attribute.md), [**Ende**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="cfb9a-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="cfb9a-111">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="cfb9a-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb9a-112">Parent</span><span class="sxs-lookup"><span data-stu-id="cfb9a-112">Parent</span></span>   | <span data-ttu-id="cfb9a-113">[**Composite**](composite-element.md), [**Group**](group-element.md), [**Clip**](clip-element.md), [**Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="cfb9a-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="cfb9a-114">Children</span><span class="sxs-lookup"><span data-stu-id="cfb9a-114">Children</span></span> | [<span data-ttu-id="cfb9a-115">**param**</span><span class="sxs-lookup"><span data-stu-id="cfb9a-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="cfb9a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfb9a-116">Remarks</span></span>

<span data-ttu-id="cfb9a-117">Das **CLSID** -Attribut gibt das untergeordnete Objekt an, das den Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="cfb9a-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="cfb9a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cfb9a-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="cfb9a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfb9a-119">Requirements</span></span>



| <span data-ttu-id="cfb9a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfb9a-120">Requirement</span></span> | <span data-ttu-id="cfb9a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cfb9a-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb9a-122">Header</span><span class="sxs-lookup"><span data-stu-id="cfb9a-122">Header</span></span><br/> | <dl> <span data-ttu-id="cfb9a-123"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb9a-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfb9a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfb9a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb9a-125">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="cfb9a-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




