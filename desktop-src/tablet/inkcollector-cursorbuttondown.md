---
description: 'InkCollector.CursorButtonDown-Ereignis: Tritt auf, wenn die InkCollector-Klasse eine schaltfläche erkennt, die heruntergefahren ist.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: InkCollector.CursorButtonDown-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110328"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="c89ad-103">InkCollector.CursorButtonDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c89ad-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="c89ad-104">Tritt ein, wenn [**die InkCollector-Klasse**](inkcollector-class.md) eine Cursorschaltfläche erkennt, die nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c89ad-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="c89ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c89ad-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="c89ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c89ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c89ad-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c89ad-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89ad-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorButtonDown-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="c89ad-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="c89ad-109">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c89ad-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89ad-110">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="c89ad-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c89ad-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c89ad-111">Return value</span></span>

<span data-ttu-id="c89ad-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c89ad-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c89ad-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c89ad-113">Remarks</span></span>

<span data-ttu-id="c89ad-114">Eine Schaltfläche auf einer Stiftspitze ist nach unten, wenn der Benutzer den Stift auf den Digitizer heruntersendt und mit der Ablaufverfolgung eines Strichs beginnt.</span><span class="sxs-lookup"><span data-stu-id="c89ad-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="c89ad-115">Wenn die Schaltfläche gedrückt wird, ist eine Schaltfläche auf einer Knopffläche nicht mehr zu sehen.</span><span class="sxs-lookup"><span data-stu-id="c89ad-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="c89ad-116">Wenn Sie die rechte Maustaste drücken, erhalten Sie tatsächlich zwei **CursorButtonDown-Ereignisse** : eines für die gedrückte rechte Schaltfläche und eines für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="c89ad-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="c89ad-117">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonDown definiert.</span><span class="sxs-lookup"><span data-stu-id="c89ad-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="c89ad-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c89ad-118">Requirements</span></span>



| <span data-ttu-id="c89ad-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c89ad-119">Requirement</span></span> | <span data-ttu-id="c89ad-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c89ad-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c89ad-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c89ad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c89ad-122">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="c89ad-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c89ad-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c89ad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c89ad-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c89ad-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c89ad-125">Header</span><span class="sxs-lookup"><span data-stu-id="c89ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c89ad-126"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="c89ad-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c89ad-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c89ad-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c89ad-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c89ad-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c89ad-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c89ad-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c89ad-130">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c89ad-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="c89ad-131">**CursorDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="c89ad-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="c89ad-132">**CursorButtonUp-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="c89ad-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="c89ad-133">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c89ad-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="c89ad-134">**IInkCursorButton-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c89ad-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




