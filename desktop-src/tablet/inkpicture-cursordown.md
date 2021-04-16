---
description: Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: InkPicture. currsordown-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529897"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="5f047-103">InkPicture. currsordown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f047-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="5f047-104">Tritt auf, wenn die Cursor-QuickInfo die digitalisierende Tablet-Oberfläche kontaktiert</span><span class="sxs-lookup"><span data-stu-id="5f047-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f047-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f047-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="5f047-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f047-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f047-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f047-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt, das das **CursorDown** -Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="5f047-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="5f047-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f047-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f047-110">Das [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das gestartet wurde, **als das "** [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) "-Objekt ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="5f047-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f047-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f047-111">Return value</span></span>

<span data-ttu-id="5f047-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5f047-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f047-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f047-113">Remarks</span></span>

<span data-ttu-id="5f047-114">Diese Ereignis Methoden werden in den Schnittstellen **\_ iinkcollectorevents**, **\_ iinkoverlayevents** und **\_ iinkpictureevents** definiert.</span><span class="sxs-lookup"><span data-stu-id="5f047-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="5f047-115">Die **\_ iinkcollector Events**-, **\_ iinkoverlayevents**-und **\_ iinkpictureevents** -Schnittstelle implementieren die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ icecursordown.</span><span class="sxs-lookup"><span data-stu-id="5f047-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="5f047-116">Verwenden Sie dieses Ereignis sorgfältig, da dies eine negative Auswirkung auf die Handschrift Leistung haben kann, wenn zu viel Code in den Ereignis Handlern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f047-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="5f047-117">Um die Echtzeitleistung zu verbessern, blenden Sie den Mauszeiger in den [**MouseDown**](inkpicture-mousedown.md) -und [**MouseUp**](inkpicture-mouseup.md) -Ereignis Handlern aus, oder zeigen Sie ihn an.</span><span class="sxs-lookup"><span data-stu-id="5f047-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f047-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f047-118">Requirements</span></span>



| <span data-ttu-id="5f047-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f047-119">Requirement</span></span> | <span data-ttu-id="5f047-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5f047-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f047-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f047-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f047-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f047-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5f047-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f047-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f047-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f047-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5f047-125">Header</span><span class="sxs-lookup"><span data-stu-id="5f047-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f047-126"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5f047-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f047-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f047-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f047-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f047-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5f047-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f047-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f047-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="5f047-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5f047-131">**Currsorbuttonup-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5f047-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="5f047-132">**Currsorbuttondown-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="5f047-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="5f047-133">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f047-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5f047-134">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f047-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

