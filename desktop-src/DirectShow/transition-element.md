---
description: Das Übergangs Element definiert ein Übergangs Objekt. Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. b. einer zusammengesetzten oder einer Spur) zu einem anderen führt.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Transition-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368812"
---
# <a name="transition-element"></a><span data-ttu-id="6f881-104">Transition-Element</span><span class="sxs-lookup"><span data-stu-id="6f881-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="6f881-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6f881-105">\[Deprecated.</span></span> <span data-ttu-id="6f881-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6f881-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6f881-107">Das- `transition` Element definiert ein Übergangs Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f881-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="6f881-108">Ein Übergang ist eine Transformation mit zwei Eingaben, die zu einem Übergang von einem Stream (z. b. einer zusammengesetzten oder einer Spur) zu einem anderen führt.</span><span class="sxs-lookup"><span data-stu-id="6f881-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="6f881-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f881-109">Attributes</span></span>

<span data-ttu-id="6f881-110">[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Start**](start-attribute.md), [**Stopps**](stop-attribute.md), [**Swap**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="6f881-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="6f881-111">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="6f881-111">Parent/Child Information</span></span>



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="6f881-112">Parent</span><span class="sxs-lookup"><span data-stu-id="6f881-112">Parent</span></span>   | <span data-ttu-id="6f881-113">[**Composite**](composite-element.md), [ **Track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="6f881-113">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="6f881-114">Children</span><span class="sxs-lookup"><span data-stu-id="6f881-114">Children</span></span> | [<span data-ttu-id="6f881-115">**param**</span><span class="sxs-lookup"><span data-stu-id="6f881-115">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="6f881-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f881-116">Remarks</span></span>

<span data-ttu-id="6f881-117">Das **CLSID** -Attribut gibt das untergeordnete Objekt an, das den Übergang erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f881-117">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="6f881-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f881-118">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="6f881-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6f881-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f881-120">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="6f881-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



