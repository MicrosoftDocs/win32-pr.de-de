---
description: 'InkCollector.CursorDown-Ereignis: Tritt auf, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.'
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: InkCollector.CursorDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110298"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="0a4ef-103">InkCollector.CursorDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="0a4ef-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="0a4ef-104">Tritt ein, wenn die Cursorspitze die digitalisierende Tablet-Oberfläche kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a4ef-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="0a4ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a4ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4ef-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0a4ef-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4ef-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorDown-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="0a4ef-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0a4ef-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4ef-110">Das [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das gestartet wurde, als das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das **CursorDown-Ereignis** ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4ef-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a4ef-111">Return value</span></span>

<span data-ttu-id="0a4ef-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4ef-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a4ef-113">Remarks</span></span>

<span data-ttu-id="0a4ef-114">Diese Ereignismethode wird in den \_ IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents definiert.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="0a4ef-115">Die \_ Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und IInkPictureEvents implementieren die IDispatch-Schnittstelle mit dem Bezeichner \_ DISPID [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="0a4ef-116">Verwenden Sie dieses Ereignis sorgfältig, da es sich negativ auf die Ink-Leistung auswirken kann, wenn in den Ereignishandlern zu viel Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="0a4ef-117">Um die Leistung von Ink in Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkcollector-mousedown.md) und [**MouseUp-Ereignishandlern**](inkcollector-mouseup.md) aus oder ein.</span><span class="sxs-lookup"><span data-stu-id="0a4ef-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4ef-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a4ef-118">Requirements</span></span>



| <span data-ttu-id="0a4ef-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a4ef-119">Requirement</span></span> | <span data-ttu-id="0a4ef-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0a4ef-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4ef-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a4ef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4ef-122">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="0a4ef-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a4ef-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a4ef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4ef-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0a4ef-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0a4ef-125">Header</span><span class="sxs-lookup"><span data-stu-id="0a4ef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a4ef-126"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ef-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0a4ef-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a4ef-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a4ef-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ef-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0a4ef-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a4ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ef-130">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="0a4ef-131">**CursorButtonDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="0a4ef-132">**CursorButtonUp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="0a4ef-133">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="0a4ef-134">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0a4ef-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

