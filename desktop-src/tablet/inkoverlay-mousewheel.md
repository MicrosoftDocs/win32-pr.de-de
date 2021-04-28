---
description: 'InkOverlay.MouseWheel-Ereignis: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector- oder InkOverlay-Objekt den Fokus besitzt.'
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: InkOverlay.MouseWheel-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468dbdac09fd40144768e8342791d5712a570bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116888"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="e2e1f-103">InkOverlay.MouseWheel-Ereignis</span><span class="sxs-lookup"><span data-stu-id="e2e1f-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="e2e1f-104">Tritt ein, wenn sich das Mausrad bewegt, während [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e1f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e1f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="e2e1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e1f-107">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-108">Die gedrückte Maustaste.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="e2e1f-109">*Umschalten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="e2e1f-111">*Delta* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-112">Eine Anzahl mit Vorzeichen für die Anzahl der Detenten, die das Mausrad gedreht hat.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="e2e1f-113">Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="e2e1f-114">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-115">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="e2e1f-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-117">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="e2e1f-118">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e1f-119">Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="e2e1f-120">Der Standardwert ist **FALSE,** der angibt, dass das Ereignis nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e1f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e1f-121">Return value</span></span>

<span data-ttu-id="e2e1f-122">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e1f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2e1f-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e2e1f-124">Die Eigenschaften *pX* und *pY* befinden sich in Pixeln und nicht in den HIMETRIC-Einheiten, die dem Freiraum zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="e2e1f-125">Dies liegt daran, dass dieses Ereignis das zugehörige Mausereignis einer Nicht-Stiftanwendung ersetzt und diese Art von Anwendung nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="e2e1f-126">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEMouseWheel definiert.</span><span class="sxs-lookup"><span data-stu-id="e2e1f-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e1f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e1f-127">Requirements</span></span>



| <span data-ttu-id="e2e1f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e1f-128">Requirement</span></span> | <span data-ttu-id="e2e1f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e1f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e1f-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2e1f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e1f-131">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e2e1f-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2e1f-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2e1f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e1f-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e2e1f-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e2e1f-134">Header</span><span class="sxs-lookup"><span data-stu-id="e2e1f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e1f-135"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="e2e1f-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2e1f-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2e1f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2e1f-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e1f-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e2e1f-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2e1f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e1f-139">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e2e1f-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="e2e1f-140">**InkMouseButton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e2e1f-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="e2e1f-141">**InkShiftKeyModifierFlags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="e2e1f-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




