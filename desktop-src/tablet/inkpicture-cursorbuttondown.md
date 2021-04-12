---
description: Tritt auf, wenn die InkCollector-Klasse eine nicht herunter gebrannte Cursor Schaltfläche erkennt.
ms.assetid: 9ee2c19e-8a44-428b-a4c1-3c7250dcdeda
title: InkPicture. currsorbuttondown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4531f41ce597d9cbb1fa0b8665a1821a8a32dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217674"
---
# <a name="inkpicturecursorbuttondown-event"></a><span data-ttu-id="3fd5f-103">InkPicture. currsorbuttondown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3fd5f-103">InkPicture.CursorButtonDown event</span></span>

<span data-ttu-id="3fd5f-104">Tritt auf, wenn die [**InkCollector-Klasse**](inkcollector-class.md) eine nicht herunter gebrannte Cursor Schaltfläche erkennt.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd5f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd5f-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="3fd5f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd5f-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd5f-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd5f-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorButtonDown** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="3fd5f-109">*Schaltfläche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fd5f-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fd5f-110">Die Schaltfläche, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd5f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fd5f-111">Return value</span></span>

<span data-ttu-id="3fd5f-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd5f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd5f-113">Remarks</span></span>

<span data-ttu-id="3fd5f-114">Eine Schaltfläche auf einer Stift Spitze ist nicht mehr angezeigt, wenn der Benutzer den Stift auf den Digitalisierer senkt und die Ablauf Verfolgung für einen Strich startet.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="3fd5f-115">Wenn die Schaltfläche gedrückt wird, wird eine Schaltfläche auf einem Fass heruntergedrückt.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="3fd5f-116">Wenn Sie mit der rechten Maustaste auf die Rechte Maustaste klicken, erhalten Sie tatsächlich zwei **Cursor buttondown** -Ereignisse: einen für die Rechte Taste gedrückt und einen für die linke Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="3fd5f-117">Diese Ereignismethode wird in **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only Interface (Dispinterfaces) mit der ID DISPID \_ icecursorbuttondown definiert.</span><span class="sxs-lookup"><span data-stu-id="3fd5f-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd5f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fd5f-118">Requirements</span></span>



| <span data-ttu-id="3fd5f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fd5f-119">Requirement</span></span> | <span data-ttu-id="3fd5f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd5f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd5f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fd5f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd5f-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fd5f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3fd5f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fd5f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd5f-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3fd5f-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3fd5f-125">Header</span><span class="sxs-lookup"><span data-stu-id="3fd5f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd5f-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3fd5f-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3fd5f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3fd5f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="3fd5f-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd5f-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3fd5f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd5f-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3fd5f-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3fd5f-131">**Ereignis "Cursor"**</span><span class="sxs-lookup"><span data-stu-id="3fd5f-131">**CursorDown Event**</span></span>](inkpicture-cursordown.md)
</dt> <dt>

[<span data-ttu-id="3fd5f-132">**Currsorbuttonup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="3fd5f-132">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="3fd5f-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3fd5f-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="3fd5f-134">**Iinkcursor Button-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3fd5f-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




