---
description: 'InkOverlay.Stroke-Ereignis: Tritt auf, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.'
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: InkOverlay.Stroke-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408c44cf47ecfbf3ea0cfd0f8306be61efb0f8e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116848"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="60ca8-103">InkOverlay.Stroke-Ereignis</span><span class="sxs-lookup"><span data-stu-id="60ca8-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="60ca8-104">Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.</span><span class="sxs-lookup"><span data-stu-id="60ca8-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ca8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60ca8-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="60ca8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60ca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ca8-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="60ca8-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca8-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Stroke-Ereignis [**generiert**](inkcollector-stroke.md) hat.</span><span class="sxs-lookup"><span data-stu-id="60ca8-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="60ca8-109">*Strich* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="60ca8-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca8-110">Das [**gesammelte IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)</span><span class="sxs-lookup"><span data-stu-id="60ca8-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="60ca8-111">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60ca8-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60ca8-112">Gibt an, ob das Ereignis abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="60ca8-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="60ca8-113">True **gibt an,** dass die Auflistung des Strichs abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="60ca8-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ca8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60ca8-114">Return value</span></span>

<span data-ttu-id="60ca8-115">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="60ca8-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60ca8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60ca8-116">Remarks</span></span>

<span data-ttu-id="60ca8-117">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEStroke definiert.</span><span class="sxs-lookup"><span data-stu-id="60ca8-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="60ca8-118">Das [**Stroke-Ereignis**](inkcollector-stroke.md) wird im Auswahl- oder Löschmodus ausgelöst, nicht nur beim Einfügen von Ink.</span><span class="sxs-lookup"><span data-stu-id="60ca8-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="60ca8-119">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="60ca8-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="60ca8-120">Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.</span><span class="sxs-lookup"><span data-stu-id="60ca8-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="60ca8-121">Das [**Stroke-Ereignis**](inkcollector-stroke.md) wird beim Zeichnen eines Strichs durch den Benutzer und nicht beim Hinzugefügt eines Strichs zur [InkStrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60ca8-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="60ca8-122">Wenn der Benutzer zum ersten Mal mit dem Zeichnen eines Strichs beginnt, wird er sofort der InkStrokes-Auflistung hinzugefügt. Das **Stroke-Ereignis** wird jedoch erst dann aus, wenn der Strich abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="60ca8-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="60ca8-123">Daher können Striche in der InkStrokes-Auflistung vorhanden sein, die der **Stroke-Ereignishandler** nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="60ca8-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60ca8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ca8-124">Requirements</span></span>



| <span data-ttu-id="60ca8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60ca8-125">Requirement</span></span> | <span data-ttu-id="60ca8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="60ca8-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ca8-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60ca8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="60ca8-128">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="60ca8-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="60ca8-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60ca8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="60ca8-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="60ca8-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="60ca8-131">Header</span><span class="sxs-lookup"><span data-stu-id="60ca8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="60ca8-132"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="60ca8-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="60ca8-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60ca8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="60ca8-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60ca8-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="60ca8-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60ca8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ca8-136">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="60ca8-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="60ca8-137">[**StrokesAdded Event \[ InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="60ca8-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="60ca8-138">[**StrokesDeleted-Ereignis \[ inkOverlay-Klasse\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="60ca8-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="60ca8-139">**IInkCursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="60ca8-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="60ca8-140">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="60ca8-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

