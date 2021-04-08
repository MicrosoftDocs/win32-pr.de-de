---
description: Tritt auf, wenn der Benutzer ein neues IInkStrokeDisp-Objekt für ein beliebiges iinktablet-Objekt zeichnet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: InkEdit. Stroke-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759540"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="5f5b7-103">InkEdit. Stroke-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f5b7-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="5f5b7-104">Tritt auf, wenn der Benutzer ein neues [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt für ein beliebiges [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt zeichnet.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f5b7-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="5f5b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f5b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f5b7-107">*Cursor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f5b7-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5b7-108">Das [**iinkcursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="5f5b7-109">*Strich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f5b7-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5b7-110">Das gesammelte [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="5f5b7-111">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5f5b7-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5b7-112">**Variant \_ TRUE** , wenn die Auflistung des [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekts abgebrochen werden soll. **Variant \_ FALSE** , um das **IInkStrokeDisp** -Objekt zu erfassen und auch mit dem **Strich** fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f5b7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f5b7-113">Return value</span></span>

<span data-ttu-id="5f5b7-114">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f5b7-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f5b7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f5b7-116">Remarks</span></span>

<span data-ttu-id="5f5b7-117">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="5f5b7-118">Die **\_ iinkeditevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner DISPID \_ ieestroke.</span><span class="sxs-lookup"><span data-stu-id="5f5b7-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5b7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f5b7-119">Requirements</span></span>



| <span data-ttu-id="5f5b7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f5b7-120">Requirement</span></span> | <span data-ttu-id="5f5b7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5f5b7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5b7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f5b7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5b7-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f5b7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f5b7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f5b7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5b7-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f5b7-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5f5b7-126">Header</span><span class="sxs-lookup"><span data-stu-id="5f5b7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5b7-127"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="5f5b7-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f5b7-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f5b7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f5b7-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f5b7-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5f5b7-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f5b7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5b7-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="5f5b7-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5f5b7-132">**Iinkcursor-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f5b7-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="5f5b7-133">**IInkStrokeDisp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5f5b7-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

