---
description: Tritt auf, wenn ein oder mehrere IInkStrokeDisp-Objekte zur inkstrokes-Auflistung hinzugefügt werden.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: InkPicture. StrokesAdded-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e79d87a4315068cbb0cf9db25b6532bc4c09943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353833"
---
# <a name="inkpicturestrokesadded-event"></a><span data-ttu-id="fb58c-103">InkPicture. StrokesAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fb58c-103">InkPicture.StrokesAdded event</span></span>

<span data-ttu-id="fb58c-104">Tritt auf, wenn ein oder mehrere [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte zur [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fb58c-104">Occurs when one or more [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb58c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb58c-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="fb58c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb58c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb58c-107">*StrokeIds* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb58c-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb58c-108">Das ganzzahlige Array von bezeichgern für jedes [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt, das bei Auftreten dieses Ereignisses hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fb58c-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="fb58c-109">Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="fb58c-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb58c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb58c-110">Return value</span></span>

<span data-ttu-id="fb58c-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb58c-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb58c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb58c-112">Remarks</span></span>

<span data-ttu-id="fb58c-113">Diese Ereignismethode wird in der **\_ iinkstrokesevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="fb58c-113">This event method is defined in the **\_IInkStrokesEvents** interface.</span></span> <span data-ttu-id="fb58c-114">Die **\_ iinkstrokesevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID" \_ .</span><span class="sxs-lookup"><span data-stu-id="fb58c-114">The **\_IInkStrokesEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb58c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb58c-115">Requirements</span></span>



| <span data-ttu-id="fb58c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb58c-116">Requirement</span></span> | <span data-ttu-id="fb58c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="fb58c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb58c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb58c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fb58c-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb58c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fb58c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb58c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fb58c-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fb58c-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fb58c-122">Header</span><span class="sxs-lookup"><span data-stu-id="fb58c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb58c-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fb58c-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fb58c-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb58c-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb58c-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb58c-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fb58c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb58c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb58c-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fb58c-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

