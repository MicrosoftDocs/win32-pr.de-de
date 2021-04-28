---
description: 'InkOverlay.CursorButtonUp-Ereignis: Tritt auf, wenn der InkCollector eine Cursorschaltfläche erkennt, die aktiv ist.'
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: InkOverlay.CursorButtonUp-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086848"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="91d7b-103">InkOverlay.CursorButtonUp-Ereignis</span><span class="sxs-lookup"><span data-stu-id="91d7b-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="91d7b-104">Tritt ein, wenn [**der InkCollector**](inkcollector-class.md) eine cursor-Schaltfläche erkennt, die aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="91d7b-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d7b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91d7b-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="91d7b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="91d7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="91d7b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-108">Das [**IInkCursor-Schnittstellenobjekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**CursorButtonUp-Ereignis**](inkcollector-cursorbuttonup.md) generiert hat.</span><span class="sxs-lookup"><span data-stu-id="91d7b-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-109">*Schaltfläche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="91d7b-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-110">Die Schaltfläche, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="91d7b-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d7b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91d7b-111">Return value</span></span>

<span data-ttu-id="91d7b-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="91d7b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d7b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91d7b-113">Remarks</span></span>

<span data-ttu-id="91d7b-114">Eine Schaltfläche auf einer Stiftspitze wird angezeigt, wenn der Benutzer einen Strich abschließt und den Stift aus dem Digitizer hebt.</span><span class="sxs-lookup"><span data-stu-id="91d7b-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="91d7b-115">Eine Schaltfläche an einem Fass ist hoch, wenn die Schaltfläche nicht gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="91d7b-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="91d7b-116">Wenn Sie die rechte Maustaste loslassen, erhalten Sie tatsächlich zwei [**CursorButtonUp-Ereignisse:**](inkcollector-cursorbuttonup.md) eines für die rechte Schaltfläche nach oben und eines für die linke Schaltfläche nach oben.</span><span class="sxs-lookup"><span data-stu-id="91d7b-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="91d7b-117">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorButtonUp definiert.</span><span class="sxs-lookup"><span data-stu-id="91d7b-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d7b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91d7b-118">Requirements</span></span>



| <span data-ttu-id="91d7b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91d7b-119">Requirement</span></span> | <span data-ttu-id="91d7b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="91d7b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d7b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91d7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91d7b-122">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="91d7b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="91d7b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91d7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91d7b-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="91d7b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="91d7b-125">Header</span><span class="sxs-lookup"><span data-stu-id="91d7b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d7b-126"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="91d7b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="91d7b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91d7b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="91d7b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91d7b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="91d7b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="91d7b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d7b-130">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="91d7b-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="91d7b-131">**CursorButtonDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="91d7b-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="91d7b-132">**CursorDown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="91d7b-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="91d7b-133">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91d7b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="91d7b-134">**IInkCursorButton-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="91d7b-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




