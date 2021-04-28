---
description: 'InkPicture.CursorInRange-Ereignis: Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.'
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: InkPicture.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05d703022e8d97df0d8d74a73e20af3d91b8531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086578"
---
# <a name="inkpicturecursorinrange-event"></a><span data-ttu-id="182f8-103">InkPicture.CursorInRange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="182f8-103">InkPicture.CursorInRange event</span></span>

<span data-ttu-id="182f8-104">Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tabletkontexts eintritt.</span><span class="sxs-lookup"><span data-stu-id="182f8-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="182f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="182f8-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="182f8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="182f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182f8-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="182f8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182f8-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorInRange-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="182f8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="182f8-109">*NewCursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="182f8-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182f8-110">**VARIANT \_ TRUE,** wenn dieser Freihandsammler zum ersten Mal Kontakt mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) hat, das das **CursorInRange-Ereignis** generiert hat. Andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="182f8-110">**VARIANT\_TRUE** if this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="182f8-111">*ButtonsState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="182f8-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="182f8-112">Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="182f8-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="182f8-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="182f8-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182f8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="182f8-114">Return value</span></span>

<span data-ttu-id="182f8-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="182f8-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="182f8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="182f8-116">Remarks</span></span>

<span data-ttu-id="182f8-117">Diese Ereignismethode wird in der **\_ IInkCollectorEvents-,** **\_ IInkOverlayEvents-** und **\_ IInkPictureEvents-Dispatch-Only-Schnittstelle** (dispinterfaces) mit der ID DISPID \_ ICECursorInRange definiert.</span><span class="sxs-lookup"><span data-stu-id="182f8-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="182f8-118">Das **CursorInRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus.</span><span class="sxs-lookup"><span data-stu-id="182f8-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="182f8-119">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="182f8-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="182f8-120">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="182f8-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="182f8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182f8-121">Requirements</span></span>



| <span data-ttu-id="182f8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="182f8-122">Requirement</span></span> | <span data-ttu-id="182f8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="182f8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="182f8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="182f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="182f8-125">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="182f8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="182f8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="182f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="182f8-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="182f8-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="182f8-128">Header</span><span class="sxs-lookup"><span data-stu-id="182f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="182f8-129"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="182f8-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="182f8-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="182f8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="182f8-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="182f8-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="182f8-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="182f8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182f8-133">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="182f8-133">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="182f8-134">**CursorOutOfRange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="182f8-134">**CursorOutOfRange Event**</span></span>](inkpicture-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="182f8-135">**InkCursorButtonState-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="182f8-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="182f8-136">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="182f8-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




