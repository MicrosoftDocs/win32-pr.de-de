---
description: 'InkOverlay.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine Cursorschaltfläche erkennt, die nicht aktiv ist.'
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: InkOverlay.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcae13afb67be0312959939e0793d89d99c841ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117078"
---
# <a name="inkoverlaycursorbuttondown-event"></a><span data-ttu-id="f21ea-103">InkOverlay.CursorButtonDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f21ea-103">InkOverlay.CursorButtonDown event</span></span>

<span data-ttu-id="f21ea-104">Tritt ein, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f21ea-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="f21ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f21ea-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="f21ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f21ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f21ea-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f21ea-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21ea-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**CursorButtonDown-Ereignis**](inkcollector-cursorbuttondown.md) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="f21ea-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonDown**](inkcollector-cursorbuttondown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="f21ea-109">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f21ea-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f21ea-110">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="f21ea-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f21ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f21ea-111">Return value</span></span>

<span data-ttu-id="f21ea-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f21ea-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f21ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f21ea-113">Remarks</span></span>

<span data-ttu-id="f21ea-114">Eine Schaltfläche auf einer Stiftspitze ist nach unten geschaltet, wenn der Benutzer den Stift auf den Digitizer heruntersenkt und mit der Ablaufverfolgung eines Strichs beginnt.</span><span class="sxs-lookup"><span data-stu-id="f21ea-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="f21ea-115">Eine Schaltfläche an einem Fass ist nach dem Drücken der Schaltfläche nicht mehr zu haben.</span><span class="sxs-lookup"><span data-stu-id="f21ea-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="f21ea-116">Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei [**CursorButtonDown-Ereignisse:**](inkcollector-cursorbuttondown.md) eines für die gedrückte rechte Schaltfläche und eines für die gedrückte linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="f21ea-116">When you press the right mouse button, you actually receive two [**CursorButtonDown**](inkcollector-cursorbuttondown.md) events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="f21ea-117">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.</span><span class="sxs-lookup"><span data-stu-id="f21ea-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="f21ea-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f21ea-118">Requirements</span></span>



| <span data-ttu-id="f21ea-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f21ea-119">Requirement</span></span> | <span data-ttu-id="f21ea-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f21ea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f21ea-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f21ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f21ea-122">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f21ea-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f21ea-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f21ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f21ea-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f21ea-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f21ea-125">Header</span><span class="sxs-lookup"><span data-stu-id="f21ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f21ea-126"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="f21ea-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f21ea-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f21ea-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f21ea-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f21ea-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f21ea-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f21ea-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f21ea-130">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f21ea-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f21ea-131">**CursorDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="f21ea-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="f21ea-132">**CursorButtonUp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="f21ea-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="f21ea-133">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f21ea-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="f21ea-134">**IInkCursorButton-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f21ea-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




