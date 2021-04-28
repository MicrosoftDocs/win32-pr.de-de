---
description: 'InkCollector.MouseWheel-Ereignis: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector- oder InkOverlay-Objekt den Fokus besitzt.'
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: InkCollector.MouseWheel-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110138"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="1784d-103">InkCollector.MouseWheel-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1784d-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="1784d-104">Tritt ein, wenn sich das Mausrad bewegt, während [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="1784d-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="1784d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1784d-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="1784d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1784d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1784d-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1784d-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-108">Die gedrückte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="1784d-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="1784d-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1784d-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="1784d-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="1784d-111">*Delta* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1784d-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-112">Eine Anzahl mit Vorzeichen für die Anzahl der Detententen, die das Mausrad gedreht hat.</span><span class="sxs-lookup"><span data-stu-id="1784d-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="1784d-113">Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.</span><span class="sxs-lookup"><span data-stu-id="1784d-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="1784d-114">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1784d-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-115">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1784d-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="1784d-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1784d-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-117">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1784d-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="1784d-118">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1784d-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1784d-119">**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="1784d-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="1784d-120">Der Standardwert ist **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="1784d-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1784d-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1784d-121">Return value</span></span>

<span data-ttu-id="1784d-122">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1784d-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1784d-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1784d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1784d-124">Die Eigenschaften *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1784d-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="1784d-125">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="1784d-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="1784d-126">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseWheel definiert.</span><span class="sxs-lookup"><span data-stu-id="1784d-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="1784d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1784d-127">Requirements</span></span>



| <span data-ttu-id="1784d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1784d-128">Requirement</span></span> | <span data-ttu-id="1784d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1784d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1784d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1784d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1784d-131">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1784d-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1784d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1784d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1784d-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1784d-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1784d-134">Header</span><span class="sxs-lookup"><span data-stu-id="1784d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1784d-135"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="1784d-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1784d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1784d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="1784d-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1784d-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1784d-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1784d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1784d-139">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1784d-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="1784d-140">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="1784d-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="1784d-141">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="1784d-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




