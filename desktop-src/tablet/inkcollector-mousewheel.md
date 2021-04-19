---
description: Tritt auf, wenn das Mausrad bewegt wird, während das InkCollector-oder InkOverlay-Objekt den Fokus besitzt.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: InkCollector. mouswheel-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346304"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="fde7a-103">InkCollector. mouswheel-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fde7a-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="fde7a-104">Tritt auf, wenn das Mausrad bewegt wird, während das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="fde7a-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fde7a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fde7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fde7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde7a-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-108">Die Maustaste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="fde7a-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="fde7a-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="fde7a-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="fde7a-111">*Delta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-112">Eine Anzahl mit Vorzeichen, die die Anzahl der Aufzählungs Zeichen des Mausrades gedreht hat.</span><span class="sxs-lookup"><span data-stu-id="fde7a-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="fde7a-113">Eine Arretierung (Rastpunkt) ist eine Kerbe des Mausrades.</span><span class="sxs-lookup"><span data-stu-id="fde7a-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="fde7a-114">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-115">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fde7a-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fde7a-116">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-117">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fde7a-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="fde7a-118">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fde7a-119">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="fde7a-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="fde7a-120">Der Standardwert ist **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="fde7a-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde7a-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fde7a-121">Return value</span></span>

<span data-ttu-id="fde7a-122">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fde7a-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde7a-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fde7a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fde7a-124">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fde7a-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="fde7a-125">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="fde7a-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="fde7a-126">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousewheel definiert.</span><span class="sxs-lookup"><span data-stu-id="fde7a-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde7a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fde7a-127">Requirements</span></span>



| <span data-ttu-id="fde7a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fde7a-128">Requirement</span></span> | <span data-ttu-id="fde7a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fde7a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fde7a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fde7a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fde7a-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fde7a-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fde7a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fde7a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fde7a-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fde7a-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fde7a-134">Header</span><span class="sxs-lookup"><span data-stu-id="fde7a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde7a-135"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fde7a-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fde7a-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fde7a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="fde7a-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde7a-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fde7a-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fde7a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde7a-139">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fde7a-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="fde7a-140">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fde7a-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="fde7a-141">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="fde7a-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




