---
description: Tritt auf, wenn ein Strich aus dem InkDisp-Objekt gelöscht wird.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: InkDisp. InkDeleted-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341183"
---
# <a name="inkdispinkdeleted-event"></a><span data-ttu-id="f280d-103">InkDisp. InkDeleted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f280d-103">InkDisp.InkDeleted event</span></span>

<span data-ttu-id="f280d-104">Tritt auf, wenn ein Strich aus dem [**InkDisp**](inkdisp-class.md) -Objekt gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="f280d-104">Occurs when a stroke is deleted from the [**InkDisp**](inkdisp-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f280d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f280d-105">Syntax</span></span>


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="f280d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f280d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f280d-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f280d-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f280d-108">Gibt das ganzzahlige Array von Stroke ID-Informationen für alle Striche an, die bei Auftreten dieses Ereignisses gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="f280d-108">Specifies the integer array of stroke ID information for all of the strokes that have been deleted when this event occurs.</span></span>

<span data-ttu-id="f280d-109">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="f280d-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f280d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f280d-110">Return value</span></span>

<span data-ttu-id="f280d-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f280d-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f280d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f280d-112">Remarks</span></span>

<span data-ttu-id="f280d-113">Wenn Sie das [**InkOverlay**](inkoverlay-class.md) -Objekt oder das [InkPicture](inkpicture-control-reference.md) -Steuerelement verwenden (wobei [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) auf " [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) " und " [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) " auf " [**strokeerase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)" festgelegt ist) und den Radierer über einen Strich übergeben, erhalten Sie die folgende Abfolge von Ereignissen:</span><span class="sxs-lookup"><span data-stu-id="f280d-113">If you use the [**InkOverlay**](inkoverlay-class.md) object or the [InkPicture](inkpicture-control-reference.md) control (where [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) equals [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) and [**EraserMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) equals [**StrokeErase**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) and pass the eraser over a stroke, you get the following sequence of events:</span></span>

-   <span data-ttu-id="f280d-114">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="f280d-114">**InkDeleted**</span></span>
-   [<span data-ttu-id="f280d-115">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="f280d-115">**InkAdded**</span></span>](inkdisp-inkadded.md)
-   <span data-ttu-id="f280d-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="f280d-116">**InkDeleted**</span></span>

<span data-ttu-id="f280d-117">Die zusätzlichen [**InkAdded**](inkdisp-inkadded.md) -und **InkDeleted** -Ereignisse treten auf, da der zugrunde liegende Code einen internen, unsichtbaren Strich hinzufügt, um den Radierer zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f280d-117">The additional [**InkAdded**](inkdisp-inkadded.md) and **InkDeleted** events occur because the underlying code adds an internal, invisible stroke to track the eraser.</span></span>

<span data-ttu-id="f280d-118">Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="f280d-118">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="f280d-119">Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ ieinkdeleted".</span><span class="sxs-lookup"><span data-stu-id="f280d-119">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IEInkDeleted.</span></span>

<span data-ttu-id="f280d-120">Das Ereignis **InkDeleted** wird auch dann ausgelöst, wenn Sie sich im Modus auswählen oder löschen befinden, nicht nur beim Einfügen von frei Hand Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f280d-120">The **InkDeleted** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="f280d-121">Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie für die Festlegung verantwortlich sind) und den Modus beachten, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="f280d-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="f280d-122">Der Vorteil dieser Anforderung ist, dass die Innovationen auf der Plattform durch ein höheres Bewusstsein für Platt Form Ereignisse verstärkt werden.</span><span class="sxs-lookup"><span data-stu-id="f280d-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f280d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f280d-123">Requirements</span></span>



| <span data-ttu-id="f280d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f280d-124">Requirement</span></span> | <span data-ttu-id="f280d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f280d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f280d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f280d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f280d-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f280d-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f280d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f280d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f280d-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f280d-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f280d-130">Header</span><span class="sxs-lookup"><span data-stu-id="f280d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f280d-131"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f280d-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f280d-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f280d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f280d-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f280d-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f280d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f280d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f280d-135">**InkDisp-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f280d-135">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

<span data-ttu-id="f280d-136">[**EditingMode-Eigenschaft \[ InkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span><span class="sxs-lookup"><span data-stu-id="f280d-136">[**EditingMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)</span></span>
</dt> <dt>

<span data-ttu-id="f280d-137">[**EraserMode-Eigenschaft ( \[ InkOverlay-Klasse)\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span><span class="sxs-lookup"><span data-stu-id="f280d-137">[**EraserMode Property \[InkOverlay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)</span></span>
</dt> <dt>

[<span data-ttu-id="f280d-138">**InkAdded-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="f280d-138">**InkAdded Event**</span></span>](inkdisp-inkadded.md)
</dt> <dt>

[<span data-ttu-id="f280d-139">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f280d-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="f280d-140">InkPicture-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="f280d-140">InkPicture Control Reference</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f280d-141">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="f280d-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

