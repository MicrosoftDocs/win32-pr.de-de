---
description: Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: InkPicture. Stroke-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b85d2410141c2d6d5f7ae92408b7d6da49a447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351524"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="3e04b-103">InkPicture. Stroke-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3e04b-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="3e04b-104">Tritt ein, wenn der Benutzer einen neuen Strich auf einem Tablet zeichnet.</span><span class="sxs-lookup"><span data-stu-id="3e04b-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e04b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e04b-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3e04b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e04b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e04b-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04b-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **Stroke** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="3e04b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="3e04b-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04b-110">Das gesammelte [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e04b-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="3e04b-111">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e04b-112">**Variant \_ TRUE** , wenn die Auflistung des Strichs abgebrochen werden soll. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="3e04b-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e04b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e04b-113">Return value</span></span>

<span data-ttu-id="3e04b-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3e04b-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e04b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e04b-115">Remarks</span></span>

<span data-ttu-id="3e04b-116">Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icestroke definiert.</span><span class="sxs-lookup"><span data-stu-id="3e04b-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="3e04b-117">Das **Stroke** -Ereignis tritt im Modus zum auswählen oder löschen auf, nicht nur beim Einfügen von frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3e04b-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="3e04b-118">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="3e04b-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="3e04b-119">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="3e04b-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="3e04b-120">Das **Stroke** -Ereignis tritt auf, wenn der Benutzer das Zeichnen eines Strichs beendet, nicht, wenn der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ein Strich hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3e04b-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="3e04b-121">Wenn der Benutzer erstmalig mit dem Zeichnen eines Strichs beginnt, wird er sofort der inkstrokes-Auflistung hinzugefügt. Das **Stroke** -Ereignis tritt jedoch erst auf, wenn der Strich beendet ist.</span><span class="sxs-lookup"><span data-stu-id="3e04b-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="3e04b-122">Daher können Striche in der inkstrokes-Auflistung vorhanden sein, die der **Stroke** -Ereignishandler nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="3e04b-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e04b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e04b-123">Requirements</span></span>



| <span data-ttu-id="3e04b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e04b-124">Requirement</span></span> | <span data-ttu-id="3e04b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3e04b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e04b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e04b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e04b-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e04b-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3e04b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e04b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e04b-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3e04b-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3e04b-130">Header</span><span class="sxs-lookup"><span data-stu-id="3e04b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e04b-131"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e04b-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e04b-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e04b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e04b-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e04b-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3e04b-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e04b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e04b-135">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3e04b-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="3e04b-136">[**Ereignis inkbild-Steuerelement für StrokesAdded \[\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="3e04b-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="3e04b-137">[**Ereignis inkbild-Steuerelement für StrokesDeleted \[\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="3e04b-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="3e04b-138">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3e04b-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="3e04b-139">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3e04b-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

