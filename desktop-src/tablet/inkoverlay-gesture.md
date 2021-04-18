---
description: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: InkOverlay. Gesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3db800db2d1fca9ee1b00620c698a592ac2121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351066"
---
# <a name="inkoverlaygesture-event"></a><span data-ttu-id="beaf7-103">InkOverlay. Gesten-Ereignis</span><span class="sxs-lookup"><span data-stu-id="beaf7-103">InkOverlay.Gesture event</span></span>

<span data-ttu-id="beaf7-104">Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="beaf7-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="beaf7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="beaf7-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="beaf7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="beaf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beaf7-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="beaf7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beaf7-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das [**Gesten**](inkcollector-gesture.md) Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="beaf7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Gesture**](inkcollector-gesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="beaf7-109">*Striche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="beaf7-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beaf7-110">Die [iinkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die die Erkennung als Geste zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="beaf7-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="beaf7-111">*Gesten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="beaf7-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beaf7-112">Ein Array von [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekten, in der Reihenfolge der Sicherheit, von der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="beaf7-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="beaf7-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="beaf7-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="beaf7-114">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="beaf7-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="beaf7-115">Gibt an, ob die Auflistung dieser Geste abgebrochen werden soll, z. b. nicht, um die frei Hand Eingabe zu löschen und das [**Stroke**](inkcollector-stroke.md) -Ereignis auszulösen.</span><span class="sxs-lookup"><span data-stu-id="beaf7-115">Whether the collection of this gesture should be canceled, such as not to erase the ink and to fire the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beaf7-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="beaf7-116">Return value</span></span>

<span data-ttu-id="beaf7-117">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="beaf7-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="beaf7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beaf7-118">Remarks</span></span>

<span data-ttu-id="beaf7-119">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icegesten definiert.</span><span class="sxs-lookup"><span data-stu-id="beaf7-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="beaf7-120">Wenn die [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) -Eigenschaft auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des [**Gesten**](inkcollector-gesture.md) Ereignisses ein fester Wert, den Sie nicht Programm gesteuert ändern können.</span><span class="sxs-lookup"><span data-stu-id="beaf7-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the [**Gesture**](inkcollector-gesture.md) event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="beaf7-121">Die Gestenerkennung ist schneller im **inkandgesten** -Modus.</span><span class="sxs-lookup"><span data-stu-id="beaf7-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="beaf7-122">So verhindern Sie die Sammlung von frei Hand Eingaben im [**inkandgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Modus:</span><span class="sxs-lookup"><span data-stu-id="beaf7-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="beaf7-123">Legen Sie [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) auf [**inkandgeste**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)fest.</span><span class="sxs-lookup"><span data-stu-id="beaf7-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="beaf7-124">Löschen Sie den Strich im [**Stroke**](inkcollector-stroke.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="beaf7-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="beaf7-125">Verarbeiten Sie die Geste im [**Gesten**](inkcollector-gesture.md) Ereignis.</span><span class="sxs-lookup"><span data-stu-id="beaf7-125">Process the gesture in the [**Gesture**](inkcollector-gesture.md) event.</span></span>

<span data-ttu-id="beaf7-126">Legen Sie die [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) -Eigenschaft auf **false** fest, um den Fluss von frei Hand Eingaben zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="beaf7-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="beaf7-127">Zusätzlich zum Einfügen von frei Hand Eingaben wird das [**Gesten**](inkcollector-gesture.md) Ereignis ausgelöst, wenn Sie sich im SELECT-oder Erase-Modus befinden.</span><span class="sxs-lookup"><span data-stu-id="beaf7-127">In addition to when inserting ink, the [**Gesture**](inkcollector-gesture.md) event is fired when in select or erase mode.</span></span> <span data-ttu-id="beaf7-128">Sie sind verantwortlich für die Nachverfolgung des Bearbeitungsmodus und sollten den Modus vor der Interpretation des Ereignisses beachten.</span><span class="sxs-lookup"><span data-stu-id="beaf7-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="beaf7-129">Um Gesten zu erkennen, müssen Sie ein Objekt oder ein Steuerelement verwenden, das frei Hand Eingaben erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="beaf7-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="beaf7-130">Anwendungs Gesten werden als Gesten definiert, die in der Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="beaf7-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="beaf7-131">Damit dieses Ereignis auftritt, muss das Objekt oder Steuerelement für eine Reihe von Anwendungs Gesten von Interesse sein.</span><span class="sxs-lookup"><span data-stu-id="beaf7-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="beaf7-132">Um die Objekte oder Steuerelemente festzulegen, die für einen Satz von Gesten relevant sind, müssen Sie die [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) -Methode des Objekts oder Steuer Elements aufrufen.</span><span class="sxs-lookup"><span data-stu-id="beaf7-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="beaf7-133">Eine Liste der spezifischen Anwendungs Gesten finden Sie unter dem [**Enumerationstyp inkapplicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="beaf7-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="beaf7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beaf7-134">Requirements</span></span>



| <span data-ttu-id="beaf7-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beaf7-135">Requirement</span></span> | <span data-ttu-id="beaf7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="beaf7-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beaf7-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="beaf7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="beaf7-138">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beaf7-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="beaf7-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="beaf7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="beaf7-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="beaf7-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="beaf7-141">Header</span><span class="sxs-lookup"><span data-stu-id="beaf7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="beaf7-142"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="beaf7-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="beaf7-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="beaf7-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="beaf7-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beaf7-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="beaf7-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beaf7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beaf7-146">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="beaf7-146">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="beaf7-147">**Inkapplicationgesten-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="beaf7-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="beaf7-148">**SetGestureStatus-Methode**</span><span class="sxs-lookup"><span data-stu-id="beaf7-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="beaf7-149">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="beaf7-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

