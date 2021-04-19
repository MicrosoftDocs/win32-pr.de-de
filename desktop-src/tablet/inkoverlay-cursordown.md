---
description: Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: InkOverlay. currsordown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0bd76d8836ae31c6e17877ddc4870dafaaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360632"
---
# <a name="inkoverlaycursordown-event"></a><span data-ttu-id="b0e78-103">InkOverlay. currsordown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b0e78-103">InkOverlay.CursorDown event</span></span>

<span data-ttu-id="b0e78-104">Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert</span><span class="sxs-lookup"><span data-stu-id="b0e78-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e78-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e78-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="b0e78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e78-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0e78-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e78-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**CursorDown**](inkcollector-cursordown.md) -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="b0e78-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorDown**](inkcollector-cursordown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="b0e78-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0e78-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e78-110">Das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das gestartet wurde, [**als das "**](inkcollector-cursordown.md) [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) "-Objekt ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="b0e78-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the [**CursorDown**](inkcollector-cursordown.md) event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e78-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0e78-111">Return value</span></span>

<span data-ttu-id="b0e78-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e78-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e78-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0e78-113">Remarks</span></span>

<span data-ttu-id="b0e78-114">Diese Ereignismethode ist in den \_ iinkcollectorevents-, \_ iinkoverlayevents-und \_ iinkpictureevents-Ereignissen definiert.</span><span class="sxs-lookup"><span data-stu-id="b0e78-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="b0e78-115">die \_ iinkcollector Events \_ -, iinkoverlayevents-und \_ iinkpictureevents-Schnittstelle implementieren die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ icecursordown.</span><span class="sxs-lookup"><span data-stu-id="b0e78-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="b0e78-116">Verwenden Sie dieses Ereignis sorgfältig, da dies eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0e78-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="b0e78-117">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkcollector-mousedown.md) -und [**MouseUp**](inkcollector-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="b0e78-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e78-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0e78-118">Requirements</span></span>



| <span data-ttu-id="b0e78-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e78-119">Requirement</span></span> | <span data-ttu-id="b0e78-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e78-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e78-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e78-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e78-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b0e78-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0e78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e78-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b0e78-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b0e78-125">Header</span><span class="sxs-lookup"><span data-stu-id="b0e78-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e78-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b0e78-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b0e78-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0e78-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0e78-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e78-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b0e78-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0e78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e78-130">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b0e78-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="b0e78-131">**Currsorbuttondown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="b0e78-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="b0e78-132">**Currsorbuttonup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="b0e78-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b0e78-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0e78-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b0e78-134">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b0e78-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

