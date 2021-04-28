---
description: 'InkPicture.Gesture-Ereignis: Tritt auf, wenn eine anwendungsspezifische Geste erkannt wird.'
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: InkPicture.Gesture-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 915557f304d722ed2819af75dd40284db119abfb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086588"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="03550-103">InkPicture.Gesture-Ereignis</span><span class="sxs-lookup"><span data-stu-id="03550-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="03550-104">Tritt ein, wenn eine anwendungsspezifische *Geste* erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="03550-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="03550-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03550-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="03550-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03550-107">*Cursor* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03550-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03550-108">Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das **Gesture-Ereignis** generiert hat.</span><span class="sxs-lookup"><span data-stu-id="03550-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="03550-109">*Striche* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03550-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03550-110">Die [IInkStrokes-Auflistung,](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) die die Erkennung als Geste zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="03550-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="03550-111">*Gesten* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="03550-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03550-112">Ein Array von [**IInkGesture-Objekten**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) in der Reihenfolge der Zuverlässigkeit aus der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="03550-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="03550-113">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="03550-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="03550-114">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="03550-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="03550-115">**VARIANT \_ TRUE,** wenn dieses Ereignis abgebrochen werden soll, z. B. um die Ink-Datei nicht zu löschen und das [**Stroke-Ereignis**](inkpicture-stroke.md) auszulöschen.</span><span class="sxs-lookup"><span data-stu-id="03550-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="03550-116">Andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="03550-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03550-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03550-117">Return value</span></span>

<span data-ttu-id="03550-118">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="03550-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03550-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03550-119">Remarks</span></span>

<span data-ttu-id="03550-120">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICEGesture definiert.</span><span class="sxs-lookup"><span data-stu-id="03550-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="03550-121">Wenn die [**CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) auf [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)festgelegt ist, ist das Timeout zwischen dem Hinzufügen einer Geste durch einen Benutzer und dem Auftreten des **Gestenereignisses** ein fester Wert, den Sie nicht programmgesteuert ändern können.</span><span class="sxs-lookup"><span data-stu-id="03550-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="03550-122">Die Gestenerkennung ist im **InkAndGesture-Modus** schneller.</span><span class="sxs-lookup"><span data-stu-id="03550-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="03550-123">So verhindern Sie das Sammeln von Freihand im [**InkAndGesture-Modus:**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)</span><span class="sxs-lookup"><span data-stu-id="03550-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="03550-124">Legen Sie [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) auf [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode)fest.</span><span class="sxs-lookup"><span data-stu-id="03550-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="03550-125">Löschen Sie den Strich im [**Stroke-Ereignis.**](inkpicture-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="03550-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="03550-126">Verarbeiten Sie die Geste im **Gestenereignis.**</span><span class="sxs-lookup"><span data-stu-id="03550-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="03550-127">Um den Fluss von Ink während der Gesturierung zu verhindern, legen Sie [**die DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) auf **FALSE** fest.</span><span class="sxs-lookup"><span data-stu-id="03550-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="03550-128">Zusätzlich zum Einfügen von Ink wird das **Gestenereignis** im Auswahl- oder Löschmodus ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="03550-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="03550-129">Sie sind für die Nachverfolgung des Bearbeitungsmodus verantwortlich und sollten den Modus kennen, bevor Sie das Ereignis interpretieren.</span><span class="sxs-lookup"><span data-stu-id="03550-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="03550-130">Um Gesten zu erkennen, müssen Sie ein Objekt oder Steuerelement verwenden, das Ink erfassen kann.</span><span class="sxs-lookup"><span data-stu-id="03550-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="03550-131">Anwendungsgesten werden als Gesten definiert, die in Ihrer Anwendung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="03550-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="03550-132">Damit dieses Ereignis eintritt, muss das Objekt oder Steuerelement an einer Reihe von Anwendungsgesten interessiert sein.</span><span class="sxs-lookup"><span data-stu-id="03550-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="03550-133">Um die Objekte oder Steuerelemente festzulegen, die für eine Reihe von Gesten von Interesse sind, rufen Sie die [**SetGestureStatus-Methode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) des Objekts oder Steuerelements auf.</span><span class="sxs-lookup"><span data-stu-id="03550-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="03550-134">Eine Liste der spezifischen Anwendungsgesten finden Sie unter [**InkApplicationGesture-Enumerationstyp.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)</span><span class="sxs-lookup"><span data-stu-id="03550-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="03550-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03550-135">Requirements</span></span>



| <span data-ttu-id="03550-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03550-136">Requirement</span></span> | <span data-ttu-id="03550-137">Wert</span><span class="sxs-lookup"><span data-stu-id="03550-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03550-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03550-138">Minimum supported client</span></span><br/> | <span data-ttu-id="03550-139">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="03550-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="03550-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03550-140">Minimum supported server</span></span><br/> | <span data-ttu-id="03550-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="03550-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="03550-142">Header</span><span class="sxs-lookup"><span data-stu-id="03550-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="03550-143"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="03550-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="03550-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03550-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="03550-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03550-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="03550-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="03550-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03550-147">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="03550-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="03550-148">**InkApplicationGesture-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="03550-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="03550-149">**SetGestureStatus-Methode**</span><span class="sxs-lookup"><span data-stu-id="03550-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="03550-150">Verwenden von Gesten</span><span class="sxs-lookup"><span data-stu-id="03550-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

