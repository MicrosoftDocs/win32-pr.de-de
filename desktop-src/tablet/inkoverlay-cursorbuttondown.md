---
description: Tritt auf, wenn die InkCollector-Klasse eine nicht herunter gebrannte Cursor Schaltfläche erkennt.
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: InkOverlay. currsorbuttondown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393949be4d7b0f172805aa0b81ce86eac3cf3b3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362939"
---
# <a name="inkoverlaycursorbuttondown-event"></a><span data-ttu-id="9d8bb-103">InkOverlay. currsorbuttondown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9d8bb-103">InkOverlay.CursorButtonDown event</span></span>

<span data-ttu-id="9d8bb-104">Tritt auf, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine nicht herunter gebrannte Cursor Schaltfläche erkennt.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8bb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d8bb-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="9d8bb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d8bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d8bb-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d8bb-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8bb-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**CursorButtonDown**](inkcollector-cursorbuttondown.md) -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonDown**](inkcollector-cursorbuttondown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="9d8bb-109">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d8bb-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d8bb-110">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d8bb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d8bb-111">Return value</span></span>

<span data-ttu-id="9d8bb-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8bb-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d8bb-113">Remarks</span></span>

<span data-ttu-id="9d8bb-114">Eine Schaltfläche auf einer Stift Spitze ist nicht mehr angezeigt, wenn der Benutzer den Stift auf den Digitalisierer senkt und die Ablauf Verfolgung für einen Strich startet.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="9d8bb-115">Wenn die Schaltfläche gedrückt wird, wird eine Schaltfläche auf einem Fass heruntergedrückt.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="9d8bb-116">Wenn Sie mit der rechten Maustaste auf die Rechte Maustaste klicken, erhalten Sie tatsächlich zwei [**Cursor buttondown**](inkcollector-cursorbuttondown.md) -Ereignisse: einen für die Rechte Taste gedrückt und einen für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-116">When you press the right mouse button, you actually receive two [**CursorButtonDown**](inkcollector-cursorbuttondown.md) events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="9d8bb-117">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursorbuttondown definiert.</span><span class="sxs-lookup"><span data-stu-id="9d8bb-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8bb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d8bb-118">Requirements</span></span>



| <span data-ttu-id="9d8bb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d8bb-119">Requirement</span></span> | <span data-ttu-id="9d8bb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9d8bb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8bb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d8bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8bb-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d8bb-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9d8bb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d8bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8bb-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d8bb-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9d8bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d8bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8bb-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9d8bb-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9d8bb-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d8bb-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d8bb-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d8bb-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9d8bb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d8bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8bb-130">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9d8bb-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9d8bb-131">**Ereignis "Cursor"**</span><span class="sxs-lookup"><span data-stu-id="9d8bb-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="9d8bb-132">**Currsorbuttonup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="9d8bb-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="9d8bb-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9d8bb-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="9d8bb-134">**Iinkcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9d8bb-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




