---
description: Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.
ms.assetid: d05b240c-ba64-4008-b25d-e06c052eb5b0
title: InkCollector. Cursor Event Range-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c1d59927f9ed0a932fe28a2c5243f328a223c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525274"
---
# <a name="inkcollectorcursorinrange-event"></a><span data-ttu-id="89b73-103">InkCollector. Cursor Event Range-Ereignis</span><span class="sxs-lookup"><span data-stu-id="89b73-103">InkCollector.CursorInRange event</span></span>

<span data-ttu-id="89b73-104">Tritt auf, wenn ein Cursor in den physischen Erkennungsbereich (Near) des Tablet-Kontexts eintritt.</span><span class="sxs-lookup"><span data-stu-id="89b73-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89b73-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="89b73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89b73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b73-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89b73-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89b73-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorInRange** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="89b73-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="89b73-109">*NewCursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89b73-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89b73-110">**Variant \_ TRUE** , um anzugeben, dass dies das erste Mal ist, dass dieser frei Hand Sammler mit dem [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt kontaktiert wird, das das **CursorInRange** -Ereignis generiert hat. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="89b73-110">**VARIANT\_TRUE** to indicate that this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="89b73-111">*Buttonsstate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89b73-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89b73-112">Der Zustand der Schaltflächen für den Cursor, der das **CursorInRange** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="89b73-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="89b73-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="89b73-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89b73-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89b73-114">Return value</span></span>

<span data-ttu-id="89b73-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89b73-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89b73-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89b73-116">Remarks</span></span>

<span data-ttu-id="89b73-117">TDiese Ereignismethode wird in den \_ \_ Dispatch-only-Schnittstellen iinkcollectorevents, iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ icecursorinrange definiert.</span><span class="sxs-lookup"><span data-stu-id="89b73-117">TThis event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="89b73-118">Das Ereignis **Cursor** wird auch dann ausgelöst, wenn es sich im Modus auswählen oder löschen befindet, nicht nur im frei Hand Modus.</span><span class="sxs-lookup"><span data-stu-id="89b73-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="89b73-119">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="89b73-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="89b73-120">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="89b73-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b73-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89b73-121">Requirements</span></span>



| <span data-ttu-id="89b73-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89b73-122">Requirement</span></span> | <span data-ttu-id="89b73-123">Wert</span><span class="sxs-lookup"><span data-stu-id="89b73-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b73-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89b73-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89b73-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89b73-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="89b73-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89b73-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89b73-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="89b73-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="89b73-128">Header</span><span class="sxs-lookup"><span data-stu-id="89b73-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="89b73-129"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="89b73-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="89b73-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89b73-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="89b73-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b73-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="89b73-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89b73-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b73-133">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="89b73-133">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="89b73-134">**Cursor-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="89b73-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="89b73-135">**Inkcurrsorbuttonstate-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="89b73-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="89b73-136">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="89b73-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




