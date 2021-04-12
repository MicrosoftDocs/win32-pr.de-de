---
description: Tritt auf, wenn der InkCollector eine Cursor Schaltfläche erkennt, die aktiv ist.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay. currsorbuttonup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348678"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="8fb6b-103">InkOverlay. currsorbuttonup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8fb6b-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="8fb6b-104">Tritt auf, wenn der [**InkCollector**](inkcollector-class.md) eine Cursor Schaltfläche erkennt, die aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fb6b-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="8fb6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fb6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb6b-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fb6b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb6b-108">Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das [**CursorButtonUp**](inkcollector-cursorbuttonup.md) -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="8fb6b-109">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8fb6b-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb6b-110">Die Schaltfläche, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb6b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fb6b-111">Return value</span></span>

<span data-ttu-id="8fb6b-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb6b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fb6b-113">Remarks</span></span>

<span data-ttu-id="8fb6b-114">Eine Schaltfläche auf einer Stift Spitze ist aktiv, wenn der Benutzer einen Strich abschließt und den Stift vom Digitalisierer abhebt.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="8fb6b-115">Eine Schaltfläche auf einem Fass ist aktiv, wenn die Schaltfläche nicht gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="8fb6b-116">Wenn Sie die Rechte Maustaste loslassen, erhalten Sie tatsächlich zwei [**Cursor BUTTONUP**](inkcollector-cursorbuttonup.md) -Ereignisse: einen für die Rechte Taste nach oben und einen für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="8fb6b-117">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icecursorbuttonup definiert.</span><span class="sxs-lookup"><span data-stu-id="8fb6b-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb6b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fb6b-118">Requirements</span></span>



| <span data-ttu-id="8fb6b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fb6b-119">Requirement</span></span> | <span data-ttu-id="8fb6b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8fb6b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb6b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fb6b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fb6b-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fb6b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8fb6b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fb6b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fb6b-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8fb6b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8fb6b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8fb6b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fb6b-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8fb6b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8fb6b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8fb6b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fb6b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fb6b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8fb6b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fb6b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb6b-130">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8fb6b-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8fb6b-131">**Currsorbuttondown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="8fb6b-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8fb6b-132">**Ereignis "Cursor"**</span><span class="sxs-lookup"><span data-stu-id="8fb6b-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="8fb6b-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8fb6b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="8fb6b-134">**Iinkcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8fb6b-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




