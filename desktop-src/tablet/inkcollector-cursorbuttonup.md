---
description: Tritt auf, wenn der InkCollector eine Cursor Schaltfläche erkennt, die aktiv ist.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: InkCollector. currsorbuttonup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344259"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="c160b-103">InkCollector. currsorbuttonup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="c160b-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="c160b-104">Tritt auf, wenn der [**InkCollector**](inkcollector-class.md) eine Cursor Schaltfläche erkennt, die aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c160b-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="c160b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c160b-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="c160b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c160b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c160b-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c160b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c160b-108">Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das **CursorButtonUp** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c160b-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="c160b-109">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c160b-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c160b-110">Die Schaltfläche, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="c160b-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c160b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c160b-111">Return value</span></span>

<span data-ttu-id="c160b-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c160b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c160b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c160b-113">Remarks</span></span>

<span data-ttu-id="c160b-114">Eine Schaltfläche auf einer Stift Spitze ist aktiv, wenn der Benutzer einen Strich abschließt und den Stift vom Digitalisierer abhebt.</span><span class="sxs-lookup"><span data-stu-id="c160b-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="c160b-115">Eine Schaltfläche auf einem Fass ist aktiv, wenn die Schaltfläche nicht gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="c160b-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="c160b-116">Wenn Sie die Rechte Maustaste loslassen, erhalten Sie tatsächlich zwei **Cursor BUTTONUP** -Ereignisse: einen für die Rechte Taste nach oben und einen für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="c160b-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="c160b-117">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursorbuttonup definiert.</span><span class="sxs-lookup"><span data-stu-id="c160b-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="c160b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c160b-118">Requirements</span></span>



| <span data-ttu-id="c160b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c160b-119">Requirement</span></span> | <span data-ttu-id="c160b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c160b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c160b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c160b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c160b-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c160b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c160b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c160b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c160b-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c160b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c160b-125">Header</span><span class="sxs-lookup"><span data-stu-id="c160b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c160b-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c160b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c160b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c160b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="c160b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c160b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c160b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c160b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c160b-130">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c160b-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="c160b-131">**Currsorbuttondown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="c160b-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="c160b-132">**Ereignis "Cursor"**</span><span class="sxs-lookup"><span data-stu-id="c160b-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="c160b-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c160b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="c160b-134">**Iinkcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c160b-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




