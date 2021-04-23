---
description: Das Übergangselement definiert ein Übergangsobjekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. B. einem zusammengesetzten Stream oder einer Spur) zu einem anderen führt.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: transition-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910038"
---
# <a name="transition-element"></a><span data-ttu-id="15ca6-104">transition-Element</span><span class="sxs-lookup"><span data-stu-id="15ca6-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="15ca6-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="15ca6-105">\[Deprecated.</span></span> <span data-ttu-id="15ca6-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="15ca6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15ca6-107">Das `transition` -Element definiert ein Übergangsobjekt.</span><span class="sxs-lookup"><span data-stu-id="15ca6-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="15ca6-108">Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. B. einem zusammengesetzten Stream oder einer Spur) zu einem anderen führt.</span><span class="sxs-lookup"><span data-stu-id="15ca6-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="15ca6-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="15ca6-109">Attributes</span></span>

<span data-ttu-id="15ca6-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="15ca6-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="15ca6-111">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="15ca6-111">Parent/Child Information</span></span>



| <span data-ttu-id="15ca6-112">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="15ca6-112">Label</span></span> | <span data-ttu-id="15ca6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="15ca6-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="15ca6-114">Parent</span><span class="sxs-lookup"><span data-stu-id="15ca6-114">Parent</span></span>   | <span data-ttu-id="15ca6-115">[**zusammengesetzte**](composite-element.md), [ **Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="15ca6-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="15ca6-116">Children</span><span class="sxs-lookup"><span data-stu-id="15ca6-116">Children</span></span> | [<span data-ttu-id="15ca6-117">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="15ca6-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="15ca6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15ca6-118">Remarks</span></span>

<span data-ttu-id="15ca6-119">Das **clsid-Attribut** gibt das Unterobjekt an, das den Übergang erstellt.</span><span class="sxs-lookup"><span data-stu-id="15ca6-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="15ca6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15ca6-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="15ca6-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15ca6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ca6-122">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="15ca6-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



