---
description: Tritt auf, wenn der Mauszeiger über das InkCollector-oder InkOverlay-Objekt bewegt wird.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: InkOverlay. moutarmove-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218050"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="5ccc1-103">InkOverlay. moutarmove-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5ccc1-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="5ccc1-104">Tritt auf, wenn der Mauszeiger über das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ccc1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ccc1-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="5ccc1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ccc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ccc1-107">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc1-108">Die Maustaste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc1-109">*UMSCHALT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc1-110">Der Zustand der UMSCHALTTASTE.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc1-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc1-112">Die x-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc1-113">*pY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc1-114">Die y-Koordinate eines Mausklicks in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="5ccc1-115">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ccc1-116">Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="5ccc1-117">Der Standardwert ist **false**. er gibt an, dass das Ereignis nicht abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ccc1-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ccc1-118">Return value</span></span>

<span data-ttu-id="5ccc1-119">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ccc1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ccc1-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5ccc1-121">Die Eigenschaften *px* und *pY* befinden sich in Pixel und nicht in den HIMETRIC-Einheiten, die dem frei Handbereich zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="5ccc1-122">Dies liegt daran, dass dieses Ereignis das verknüpfte Maus Ereignis einer Anwendung, für die ein Stift nicht gilt, ersetzt und dieser Anwendungstyp nur Pixel versteht.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="5ccc1-123">Einige Steuerelemente basieren auf einer bestimmten Beziehung zwischen [**mouledown**](inkcollector-mousedown.md)-, [**mousermove**](inkcollector-mousemove.md)-und [**mouberup**](inkcollector-mouseup.md) -Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="5ccc1-124">Das Abbrechen einiger dieser Ereignisse kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="5ccc1-125">Diese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ipemousemove definiert.</span><span class="sxs-lookup"><span data-stu-id="5ccc1-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ccc1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ccc1-126">Requirements</span></span>



| <span data-ttu-id="5ccc1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ccc1-127">Requirement</span></span> | <span data-ttu-id="5ccc1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="5ccc1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ccc1-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ccc1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ccc1-130">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ccc1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ccc1-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ccc1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ccc1-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5ccc1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5ccc1-133">Header</span><span class="sxs-lookup"><span data-stu-id="5ccc1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ccc1-134"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ccc1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5ccc1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ccc1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ccc1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ccc1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ccc1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ccc1-138">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5ccc1-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="5ccc1-139">**Inkmouerbutton-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5ccc1-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="5ccc1-140">**Inkshiftkeymodifierflags-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="5ccc1-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




