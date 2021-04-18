---
description: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: InkPicture. Gesten-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94581369554b4aef16530c9ddc8b3fd1a31ad861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351027"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="54003-103">InkPicture. Gesten-Ereignis</span><span class="sxs-lookup"><span data-stu-id="54003-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="54003-104">Tritt auf, wenn eine anwendungsspezifische *Geste* erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="54003-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="54003-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54003-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="54003-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54003-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54003-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54003-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **Gesten** Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="54003-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="54003-109">*Striche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54003-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54003-110">Die [iinkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die die Erkennung als Geste zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="54003-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="54003-111">*Gesten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54003-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54003-112">Ein Array von [**iinkgesten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) -Objekten, in der Reihenfolge der Sicherheit, von der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="54003-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="54003-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="54003-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="54003-114">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="54003-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="54003-115">**Variant \_ TRUE** , wenn dieses Ereignis abgebrochen werden soll, z. b., wenn es nicht gelöscht werden soll und das [**Stroke**](inkpicture-stroke.md) -Ereignis ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="54003-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="54003-116">Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="54003-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54003-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54003-117">Return value</span></span>

<span data-ttu-id="54003-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="54003-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54003-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54003-119">Remarks</span></span>

<span data-ttu-id="54003-120">Diese Ereignismethode wird in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icegesten definiert.</span><span class="sxs-lookup"><span data-stu-id="54003-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="54003-121">Wenn die [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) -Eigenschaft auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Zeitpunkt, zu dem ein Benutzer eine Geste hinzufügt, und dem Auftreten des **Gesten** Ereignisses ein fester Wert, den Sie nicht Programm gesteuert ändern können.</span><span class="sxs-lookup"><span data-stu-id="54003-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="54003-122">Die Gestenerkennung ist schneller im **inkandgesten** -Modus.</span><span class="sxs-lookup"><span data-stu-id="54003-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="54003-123">So verhindern Sie die Sammlung von frei Hand Eingaben im [**inkandgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) -Modus:</span><span class="sxs-lookup"><span data-stu-id="54003-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="54003-124">Legen Sie [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) auf [**inkandgeste**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)fest.</span><span class="sxs-lookup"><span data-stu-id="54003-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="54003-125">Löschen Sie den Strich im [**Stroke**](inkpicture-stroke.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="54003-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="54003-126">Verarbeiten Sie die Geste im **Gesten** Ereignis.</span><span class="sxs-lookup"><span data-stu-id="54003-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="54003-127">Legen Sie die [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) -Eigenschaft auf **false** fest, um den Fluss von frei Hand Eingaben zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="54003-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="54003-128">Zusätzlich zum Einfügen von frei Hand Eingaben wird das **Gesten** Ereignis ausgelöst, wenn Sie sich im SELECT-oder Erase-Modus befinden.</span><span class="sxs-lookup"><span data-stu-id="54003-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="54003-129">Sie sind verantwortlich für die Nachverfolgung des Bearbeitungsmodus und sollten den Modus vor der Interpretation des Ereignisses beachten.</span><span class="sxs-lookup"><span data-stu-id="54003-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="54003-130">Um Gesten zu erkennen, müssen Sie ein Objekt oder ein Steuerelement verwenden, das frei Hand Eingaben erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="54003-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="54003-131">Anwendungs Gesten werden als Gesten definiert, die in der Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="54003-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="54003-132">Damit dieses Ereignis auftritt, muss das Objekt oder Steuerelement für eine Reihe von Anwendungs Gesten von Interesse sein.</span><span class="sxs-lookup"><span data-stu-id="54003-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="54003-133">Um die Objekte oder Steuerelemente festzulegen, die für einen Satz von Gesten relevant sind, müssen Sie die [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) -Methode des Objekts oder Steuer Elements aufrufen.</span><span class="sxs-lookup"><span data-stu-id="54003-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="54003-134">Eine Liste der spezifischen Anwendungs Gesten finden Sie unter dem [**Enumerationstyp inkapplicationgesten**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="54003-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="54003-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54003-135">Requirements</span></span>



| <span data-ttu-id="54003-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54003-136">Requirement</span></span> | <span data-ttu-id="54003-137">Wert</span><span class="sxs-lookup"><span data-stu-id="54003-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54003-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54003-138">Minimum supported client</span></span><br/> | <span data-ttu-id="54003-139">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54003-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="54003-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54003-140">Minimum supported server</span></span><br/> | <span data-ttu-id="54003-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="54003-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="54003-142">Header</span><span class="sxs-lookup"><span data-stu-id="54003-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="54003-143"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="54003-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54003-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54003-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="54003-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54003-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="54003-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54003-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54003-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="54003-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="54003-148">**Inkapplicationgesten-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="54003-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="54003-149">**SetGestureStatus-Methode**</span><span class="sxs-lookup"><span data-stu-id="54003-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="54003-150">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="54003-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

