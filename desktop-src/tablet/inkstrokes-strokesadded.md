---
description: Tritt auf, wenn der inkstrokes-Auflistung ein oder mehrere Striche hinzugefügt werden.
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: Inkstrokes. StrokesAdded-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353564"
---
# <a name="inkstrokesstrokesadded-event"></a><span data-ttu-id="78780-103">Inkstrokes. StrokesAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="78780-103">InkStrokes.StrokesAdded event</span></span>

<span data-ttu-id="78780-104">Tritt auf, wenn der [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ein oder mehrere Striche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="78780-104">Occurs when one or more strokes are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="78780-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78780-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="78780-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78780-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78780-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78780-108">Das ganzzahlige Array von bezeichgern für jedes [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das bei Auftreten dieses Ereignisses hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="78780-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="78780-109">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="78780-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78780-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78780-110">Return value</span></span>

<span data-ttu-id="78780-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78780-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78780-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78780-112">Remarks</span></span>

<span data-ttu-id="78780-113">Diese Ereignismethode wird in der \_ iinkevents-Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="78780-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="78780-114">Die \_ iinkevents-Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID" \_ .</span><span class="sxs-lookup"><span data-stu-id="78780-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="78780-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78780-115">Requirements</span></span>



| <span data-ttu-id="78780-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78780-116">Requirement</span></span> | <span data-ttu-id="78780-117">Wert</span><span class="sxs-lookup"><span data-stu-id="78780-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78780-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78780-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78780-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78780-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="78780-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78780-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78780-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="78780-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="78780-122">Header</span><span class="sxs-lookup"><span data-stu-id="78780-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78780-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78780-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78780-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78780-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="78780-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78780-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="78780-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78780-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="78780-127">[Inkstrokes-Auflistung](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78780-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="78780-128">[**Method inkstriche-Auflistung hinzufügen \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span><span class="sxs-lookup"><span data-stu-id="78780-128">[**Add Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span></span>
</dt> <dt>

[<span data-ttu-id="78780-129">**InkDisp-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78780-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

