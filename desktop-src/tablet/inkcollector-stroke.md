---
description: 'InkCollector.Stroke-Ereignis: Tritt auf, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.'
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: InkCollector.Stroke-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49cb90b02ab3fca60a8fa17089b6a76f959a60e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110055"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="86c4e-103">InkCollector.Stroke-Ereignis</span><span class="sxs-lookup"><span data-stu-id="86c4e-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="86c4e-104">Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.</span><span class="sxs-lookup"><span data-stu-id="86c4e-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86c4e-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="86c4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86c4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c4e-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="86c4e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c4e-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Stroke-Ereignis **generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="86c4e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="86c4e-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="86c4e-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86c4e-110">Das [**gesammelte IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="86c4e-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="86c4e-111">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="86c4e-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="86c4e-112">**VARIANT \_ TRUE zum** Abbrechen des Ereignisses; andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="86c4e-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c4e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86c4e-113">Return value</span></span>

<span data-ttu-id="86c4e-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="86c4e-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c4e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c4e-115">Remarks</span></span>

<span data-ttu-id="86c4e-116">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEStroke definiert.</span><span class="sxs-lookup"><span data-stu-id="86c4e-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="86c4e-117">Das **Stroke-Ereignis** wird ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink.</span><span class="sxs-lookup"><span data-stu-id="86c4e-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="86c4e-118">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="86c4e-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="86c4e-119">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="86c4e-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="86c4e-120">Das **Stroke-Ereignis** wird beim Zeichnen eines Strichs durch den Benutzer und nicht beim Hinzugefügt eines Strichs zur [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="86c4e-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="86c4e-121">Wenn der Benutzer zum ersten Mal mit dem Zeichnen eines Strichs beginnt, wird er sofort der InkStrokes-Auflistung hinzugefügt. Das **Stroke-Ereignis** wird jedoch erst dann aus, wenn der Strich abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="86c4e-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="86c4e-122">Daher können Striche in der InkStrokes-Auflistung vorhanden sein, die der **Stroke-Ereignishandler** nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="86c4e-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86c4e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c4e-123">Requirements</span></span>



| <span data-ttu-id="86c4e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c4e-124">Requirement</span></span> | <span data-ttu-id="86c4e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="86c4e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c4e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86c4e-127">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="86c4e-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="86c4e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86c4e-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="86c4e-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="86c4e-130">Header</span><span class="sxs-lookup"><span data-stu-id="86c4e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c4e-131"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="86c4e-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="86c4e-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86c4e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="86c4e-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c4e-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="86c4e-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86c4e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c4e-135">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="86c4e-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="86c4e-136">[**StrokesAdded Event \[ InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="86c4e-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="86c4e-137">[**StrokesDeleted-Ereignis \[ inkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="86c4e-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="86c4e-138">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="86c4e-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="86c4e-139">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="86c4e-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

