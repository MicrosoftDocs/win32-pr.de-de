---
description: 'InkPicture.CursorDown-Ereignis: Tritt ein, wenn die Cursorspitze mit der digitalisierenden Tablettoberfläche in Kontakt tritt.'
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: InkPicture.CursorDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4b6128589ba2d0b87d4369e8bb58aa66eabf23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116698"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="680d7-103">InkPicture.CursorDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="680d7-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="680d7-104">Tritt ein, wenn die Cursorspitze die digitalisierende Tablettoberfläche kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="680d7-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="680d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="680d7-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="680d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="680d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="680d7-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="680d7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="680d7-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorDown-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="680d7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="680d7-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="680d7-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="680d7-110">Das [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das gestartet wurde, als das [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das **CursorDown-Ereignis** ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="680d7-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="680d7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="680d7-111">Return value</span></span>

<span data-ttu-id="680d7-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="680d7-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="680d7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="680d7-113">Remarks</span></span>

<span data-ttu-id="680d7-114">Diese Ereignismethoden werden in den Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** definiert.</span><span class="sxs-lookup"><span data-stu-id="680d7-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="680d7-115">Die Schnittstellen **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** implementieren die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="680d7-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="680d7-116">Verwenden Sie dieses Ereignis sorgfältig, da es negative Auswirkungen auf die Ink-Leistung haben kann, wenn zu viel Code in den Ereignishandlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="680d7-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="680d7-117">Um die Leistung von Ink-Echtzeit zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignishandlern**](inkpicture-mouseup.md) aus oder ein.</span><span class="sxs-lookup"><span data-stu-id="680d7-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="680d7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="680d7-118">Requirements</span></span>



| <span data-ttu-id="680d7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="680d7-119">Requirement</span></span> | <span data-ttu-id="680d7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="680d7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="680d7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="680d7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="680d7-122">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="680d7-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="680d7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="680d7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="680d7-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="680d7-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="680d7-125">Header</span><span class="sxs-lookup"><span data-stu-id="680d7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="680d7-126"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="680d7-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="680d7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="680d7-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="680d7-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="680d7-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="680d7-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="680d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680d7-130">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="680d7-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="680d7-131">**CursorButtonUp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="680d7-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="680d7-132">**CursorButtonDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="680d7-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="680d7-133">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="680d7-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="680d7-134">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="680d7-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

