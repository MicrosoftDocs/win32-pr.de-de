---
description: 'InkCollector.CursorInRange-Ereignis: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.'
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: InkCollector.CursorInRange-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9b7cd6204b2dbb29f9a46e48ecb12569e1301f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110288"
---
# <a name="inkcollectorcursorinrange-event"></a><span data-ttu-id="b9ff6-103">InkCollector.CursorInRange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="b9ff6-103">InkCollector.CursorInRange event</span></span>

<span data-ttu-id="b9ff6-104">Tritt ein, wenn ein Cursor in den physischen Erkennungsbereich (Näherung) des Tablet-Kontexts eintritt.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ff6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9ff6-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="b9ff6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9ff6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9ff6-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b9ff6-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff6-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **CursorInRange-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="b9ff6-109">*NewCursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b9ff6-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff6-110">**VARIANT \_ TRUE,** um anzugeben, dass dieser Ink-Collector zum ersten Mal mit dem [**IInkCursor-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) in Kontakt gekommen ist, das das **CursorInRange-Ereignis generiert** hat. andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-110">**VARIANT\_TRUE** to indicate that this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b9ff6-111">*ButtonsState* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b9ff6-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9ff6-112">Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange-Ereignis generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="b9ff6-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="b9ff6-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9ff6-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9ff6-114">Return value</span></span>

<span data-ttu-id="b9ff6-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9ff6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9ff6-116">Remarks</span></span>

<span data-ttu-id="b9ff6-117">Die TThis-Ereignismethode ist in den \_ Dispatchschnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICECursorInRange definiert.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-117">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="b9ff6-118">Das **CursorInRange-Ereignis** wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur im Ink-Modus.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="b9ff6-119">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="b9ff6-120">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="b9ff6-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9ff6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9ff6-121">Requirements</span></span>



| <span data-ttu-id="b9ff6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9ff6-122">Requirement</span></span> | <span data-ttu-id="b9ff6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b9ff6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ff6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9ff6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b9ff6-125">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="b9ff6-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b9ff6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9ff6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b9ff6-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b9ff6-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b9ff6-128">Header</span><span class="sxs-lookup"><span data-stu-id="b9ff6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9ff6-129"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff6-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b9ff6-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9ff6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9ff6-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ff6-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b9ff6-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9ff6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ff6-133">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b9ff6-133">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b9ff6-134">**CursorOutOfRange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="b9ff6-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="b9ff6-135">**InkCursorButtonState-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="b9ff6-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="b9ff6-136">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b9ff6-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




