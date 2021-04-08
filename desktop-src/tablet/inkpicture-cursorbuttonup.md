---
description: Tritt auf, wenn der InkCollector eine Cursor Schaltfläche erkennt, die aktiv ist.
ms.assetid: bb10b032-a88d-4b52-9062-c0b63dfe98e9
title: InkPicture. currsorbuttonup-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6dbee586b3179f35593c95c2d62109a379c3216
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867727"
---
# <a name="inkpicturecursorbuttonup-event"></a><span data-ttu-id="5f014-103">InkPicture. currsorbuttonup-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f014-103">InkPicture.CursorButtonUp event</span></span>

<span data-ttu-id="5f014-104">Tritt auf, wenn der [**InkCollector**](inkcollector-class.md) eine Cursor Schaltfläche erkennt, die aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5f014-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f014-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f014-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="5f014-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f014-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f014-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f014-108">Das [**iinkcursor-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt, das das **CursorButtonUp** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="5f014-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="5f014-109">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f014-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f014-110">Die Schaltfläche, die freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="5f014-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f014-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f014-111">Return value</span></span>

<span data-ttu-id="5f014-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5f014-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f014-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f014-113">Remarks</span></span>

<span data-ttu-id="5f014-114">Eine Schaltfläche auf einer Stift Spitze ist aktiv, wenn der Benutzer einen Strich abschließt und den Stift vom Digitalisierer abhebt.</span><span class="sxs-lookup"><span data-stu-id="5f014-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="5f014-115">Eine Schaltfläche auf einem Fass ist aktiv, wenn die Schaltfläche nicht gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5f014-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="5f014-116">Wenn Sie die Rechte Maustaste loslassen, erhalten Sie tatsächlich zwei **Cursor BUTTONUP** -Ereignisse: einen für die Rechte Taste nach oben und einen für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="5f014-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="5f014-117">Diese Ereignismethode wird in den DISP **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** mit der ID DISPID \_ icecursorbuttonup definiert.</span><span class="sxs-lookup"><span data-stu-id="5f014-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f014-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f014-118">Requirements</span></span>



| <span data-ttu-id="5f014-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f014-119">Requirement</span></span> | <span data-ttu-id="5f014-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5f014-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f014-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f014-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f014-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f014-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5f014-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f014-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f014-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f014-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5f014-125">Header</span><span class="sxs-lookup"><span data-stu-id="5f014-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f014-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5f014-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f014-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f014-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f014-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f014-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5f014-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f014-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f014-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="5f014-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5f014-131">**Currsorbuttondown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5f014-131">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="5f014-132">**Ereignis "Cursor"**</span><span class="sxs-lookup"><span data-stu-id="5f014-132">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="5f014-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f014-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5f014-134">**Iinkcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f014-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




