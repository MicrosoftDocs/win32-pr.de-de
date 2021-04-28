---
description: 'InkCollector.Gesture-Ereignis: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.'
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: InkCollector.Gesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110188"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="6dae1-103">InkCollector.Gesture-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6dae1-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="6dae1-104">Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6dae1-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dae1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dae1-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6dae1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dae1-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6dae1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae1-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das Gestenereignis **generiert** hat.</span><span class="sxs-lookup"><span data-stu-id="6dae1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="6dae1-109">*Striche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6dae1-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae1-110">Die [IInkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die von der -Erkannte als Geste zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6dae1-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6dae1-111">*Gesten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6dae1-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae1-112">Ein Array von [**IInkGesture-Objekten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in der Reihenfolge der Konfidenz aus der -Erkannte.</span><span class="sxs-lookup"><span data-stu-id="6dae1-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="6dae1-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="6dae1-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6dae1-114">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6dae1-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dae1-115">**VARIANT \_ TRUE,** wenn diese Geste abgebrochen werden soll; andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="6dae1-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dae1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6dae1-116">Return value</span></span>

<span data-ttu-id="6dae1-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6dae1-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dae1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6dae1-118">Remarks</span></span>

<span data-ttu-id="6dae1-119">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICEGesture definiert.</span><span class="sxs-lookup"><span data-stu-id="6dae1-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="6dae1-120">Wenn [**die CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des **Gestenereigniss** ein fester Wert, den Sie nicht programmgesteuert ändern können.</span><span class="sxs-lookup"><span data-stu-id="6dae1-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="6dae1-121">Die Gestenerkennung ist im **InkAndGesture-Modus** schneller.</span><span class="sxs-lookup"><span data-stu-id="6dae1-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="6dae1-122">So verhindern Sie die Sammlung von Ink-Daten im [**InkAndGesture-Modus:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)</span><span class="sxs-lookup"><span data-stu-id="6dae1-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="6dae1-123">Legen [**Sie CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**InkAndGesture fest.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)</span><span class="sxs-lookup"><span data-stu-id="6dae1-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="6dae1-124">Löschen Sie den Strich im [**Stroke-Ereignis.**](inkcollector-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="6dae1-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="6dae1-125">Verarbeiten Sie die Geste im **Gestenereignis.**</span><span class="sxs-lookup"><span data-stu-id="6dae1-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="6dae1-126">Um den Fluss von Ink während der Gesturierung zu verhindern, legen Sie [**die DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) auf **FALSE** fest.</span><span class="sxs-lookup"><span data-stu-id="6dae1-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="6dae1-127">Zusätzlich zum Einfügen von Ink wird das **Gestenereignis** im Auswahl- oder Löschmodus ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6dae1-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="6dae1-128">Sie sind für die Nachverfolgung des Bearbeitungsmodus verantwortlich und sollten den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="6dae1-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="6dae1-129">Um Gesten zu erkennen, müssen Sie ein Objekt oder Steuerelement verwenden, das Ink erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="6dae1-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="6dae1-130">Anwendungsgesten werden als Gesten definiert, die in Ihrer Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6dae1-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="6dae1-131">Damit dieses Ereignis eintritt, muss das Objekt oder Steuerelement an einer Reihe von Anwendungsgesten interessiert sein.</span><span class="sxs-lookup"><span data-stu-id="6dae1-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="6dae1-132">Um die Objekte oder Steuerelemente festzulegen, die für eine Reihe von Gesten von Interesse sind, rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) des Objekts oder Steuerelements auf.</span><span class="sxs-lookup"><span data-stu-id="6dae1-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="6dae1-133">Eine Liste der spezifischen Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)</span><span class="sxs-lookup"><span data-stu-id="6dae1-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dae1-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dae1-134">Requirements</span></span>



| <span data-ttu-id="6dae1-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6dae1-135">Requirement</span></span> | <span data-ttu-id="6dae1-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6dae1-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dae1-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6dae1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6dae1-138">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6dae1-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6dae1-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6dae1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6dae1-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6dae1-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6dae1-141">Header</span><span class="sxs-lookup"><span data-stu-id="6dae1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dae1-142"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="6dae1-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6dae1-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6dae1-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="6dae1-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dae1-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6dae1-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6dae1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dae1-146">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6dae1-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="6dae1-147">**InkApplicationGesture-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="6dae1-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="6dae1-148">**SetGestureStatus-Methode**</span><span class="sxs-lookup"><span data-stu-id="6dae1-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="6dae1-149">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="6dae1-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

