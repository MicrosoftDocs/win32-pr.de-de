---
description: Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: InkOverlay. Stroke-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759529"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="196aa-103">InkOverlay. Stroke-Ereignis</span><span class="sxs-lookup"><span data-stu-id="196aa-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="196aa-104">Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.</span><span class="sxs-lookup"><span data-stu-id="196aa-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="196aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="196aa-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="196aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="196aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="196aa-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="196aa-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="196aa-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**Stroke**](inkcollector-stroke.md) -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="196aa-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="196aa-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="196aa-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="196aa-110">Das gesammelte [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="196aa-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="196aa-111">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="196aa-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="196aa-112">Gibt an, ob das Ereignis abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="196aa-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="196aa-113">**True** gibt an, dass die Auflistung des Strichs abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="196aa-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="196aa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="196aa-114">Return value</span></span>

<span data-ttu-id="196aa-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="196aa-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="196aa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="196aa-116">Remarks</span></span>

<span data-ttu-id="196aa-117">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icestroke definiert.</span><span class="sxs-lookup"><span data-stu-id="196aa-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="196aa-118">Das [**Stroke**](inkcollector-stroke.md) -Ereignis wird im Modus zum auswählen oder löschen ausgelöst, nicht nur beim Einfügen von frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="196aa-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="196aa-119">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="196aa-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="196aa-120">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="196aa-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="196aa-121">Das [**Stroke**](inkcollector-stroke.md) -Ereignis wird ausgelöst, wenn der Benutzer das Zeichnen eines Strichs beendet, nicht, wenn der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ein Strich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="196aa-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="196aa-122">Wenn der Benutzer erstmalig mit dem Zeichnen eines Strichs beginnt, wird er sofort der inkstrokes-Auflistung hinzugefügt. Das **Stroke** -Ereignis wird jedoch erst ausgelöst, wenn der Strich beendet ist.</span><span class="sxs-lookup"><span data-stu-id="196aa-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="196aa-123">Daher können Striche in der inkstrokes-Auflistung vorhanden sein, die der **Stroke** -Ereignishandler nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="196aa-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="196aa-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="196aa-124">Requirements</span></span>



| <span data-ttu-id="196aa-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="196aa-125">Requirement</span></span> | <span data-ttu-id="196aa-126">Wert</span><span class="sxs-lookup"><span data-stu-id="196aa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="196aa-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="196aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="196aa-128">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="196aa-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="196aa-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="196aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="196aa-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="196aa-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="196aa-131">Header</span><span class="sxs-lookup"><span data-stu-id="196aa-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="196aa-132"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="196aa-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="196aa-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="196aa-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="196aa-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="196aa-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="196aa-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="196aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="196aa-136">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="196aa-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="196aa-137">[**StrokesAdded-Auflistung für Ereignis \[ inkstrokes\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="196aa-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="196aa-138">[**StrokesDeleted-Ereignis \[ InkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="196aa-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="196aa-139">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="196aa-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="196aa-140">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="196aa-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

