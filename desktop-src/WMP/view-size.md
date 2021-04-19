---
title: View. Size
description: Die size-Methode ändert die Ansicht an einem angegebenen Rand.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Ansicht. Größen Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369450"
---
# <a name="viewsize"></a><span data-ttu-id="2db44-104">View. Size</span><span class="sxs-lookup"><span data-stu-id="2db44-104">VIEW.size</span></span>

<span data-ttu-id="2db44-105">Die **size** -Methode ändert die **Ansicht** an einem angegebenen Rand.</span><span class="sxs-lookup"><span data-stu-id="2db44-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="2db44-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2db44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2db44-107"><span id="handle"></span><span id="HANDLE"></span>*bewältigen*</span><span class="sxs-lookup"><span data-stu-id="2db44-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="2db44-108">Eine Zeichenfolge, die den zu Verschieb nden Rand oder die Ecke angibt</span><span class="sxs-lookup"><span data-stu-id="2db44-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="2db44-109">Diese Zeichenfolge muss einen der folgenden acht Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2db44-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="2db44-110">Edge</span><span class="sxs-lookup"><span data-stu-id="2db44-110">Edge</span></span>   | <span data-ttu-id="2db44-111">Ecke</span><span class="sxs-lookup"><span data-stu-id="2db44-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="2db44-112">top</span><span class="sxs-lookup"><span data-stu-id="2db44-112">top</span></span>    | <span data-ttu-id="2db44-113">oberen rechten</span><span class="sxs-lookup"><span data-stu-id="2db44-113">topright</span></span>    |
| <span data-ttu-id="2db44-114">Rechts</span><span class="sxs-lookup"><span data-stu-id="2db44-114">right</span></span>  | <span data-ttu-id="2db44-115">BottomRight</span><span class="sxs-lookup"><span data-stu-id="2db44-115">bottomright</span></span> |
| <span data-ttu-id="2db44-116">bottom</span><span class="sxs-lookup"><span data-stu-id="2db44-116">bottom</span></span> | <span data-ttu-id="2db44-117">BottomLeft</span><span class="sxs-lookup"><span data-stu-id="2db44-117">bottomleft</span></span>  |
| <span data-ttu-id="2db44-118">Linker Join</span><span class="sxs-lookup"><span data-stu-id="2db44-118">left</span></span>   | <span data-ttu-id="2db44-119">TopLeft</span><span class="sxs-lookup"><span data-stu-id="2db44-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2db44-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2db44-120">Return Value</span></span>

<span data-ttu-id="2db44-121">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2db44-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2db44-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2db44-122">Remarks</span></span>

<span data-ttu-id="2db44-123">Diese Methode wird in der Regel innerhalb eines **onmouondown** -Handlers aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2db44-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="2db44-124">Sie kümmert sich um die Größe der Größe, während der Mauszeiger gezogen wird, und beendet die Größe, wenn die Maustaste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="2db44-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="2db44-125">Wenn die Größe der **Ansicht** eingeschränkt ist, können Sie die Maus nicht ziehen, um die Größe der **Ansicht** über die eingeschränkten Begrenzungen hinaus zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2db44-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="2db44-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2db44-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="2db44-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2db44-127">Requirements</span></span>



| <span data-ttu-id="2db44-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2db44-128">Requirement</span></span> | <span data-ttu-id="2db44-129">Wert</span><span class="sxs-lookup"><span data-stu-id="2db44-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2db44-130">Version</span><span class="sxs-lookup"><span data-stu-id="2db44-130">Version</span></span><br/> | <span data-ttu-id="2db44-131">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2db44-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2db44-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2db44-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2db44-133">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="2db44-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





