---
description: Tritt auf, wenn auf das InkEdit-Steuerelement Doppel geklickt wird.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: InkEdit. DblClick-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369828"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="d5390-103">InkEdit. DblClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d5390-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="d5390-104">Tritt auf, wenn auf das [InkEdit](inkedit-control-reference.md) -Steuerelement Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="d5390-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5390-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5390-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d5390-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5390-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5390-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d5390-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5390-108">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="d5390-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5390-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5390-109">Return value</span></span>

<span data-ttu-id="d5390-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5390-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5390-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5390-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5390-112">Verwenden Sie das [**MouseDown**](inkedit-mousedown.md) -und das [**MouseUp**](inkedit-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d5390-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="d5390-113">Wenn im [**Click**](inkedit-click.md) -Ereignis Code vorhanden ist, wird das **DblClick** -Ereignis nie auslöst.</span><span class="sxs-lookup"><span data-stu-id="d5390-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="d5390-114">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="d5390-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="d5390-115">Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ieedblclick**.</span><span class="sxs-lookup"><span data-stu-id="d5390-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5390-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5390-116">Requirements</span></span>



| <span data-ttu-id="d5390-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5390-117">Requirement</span></span> | <span data-ttu-id="d5390-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d5390-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5390-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5390-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5390-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5390-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d5390-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5390-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5390-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5390-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d5390-123">Header</span><span class="sxs-lookup"><span data-stu-id="d5390-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5390-124"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="d5390-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5390-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5390-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5390-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5390-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d5390-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5390-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5390-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="d5390-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




