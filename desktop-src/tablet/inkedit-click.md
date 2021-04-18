---
description: Tritt auf, wenn ein Benutzer auf das InkEdit-Steuerelement klickt.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350855"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="9fed2-103">InkEdit. Click-Ereignis</span><span class="sxs-lookup"><span data-stu-id="9fed2-103">InkEdit.Click event</span></span>

<span data-ttu-id="9fed2-104">Tritt auf, wenn ein Benutzer auf das [InkEdit](inkedit-control-reference.md) -Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="9fed2-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fed2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fed2-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="9fed2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fed2-106">Parameters</span></span>

<span data-ttu-id="9fed2-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="9fed2-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9fed2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fed2-108">Return value</span></span>

<span data-ttu-id="9fed2-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9fed2-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fed2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fed2-110">Remarks</span></span>

<span data-ttu-id="9fed2-111">Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**mousdown**](inkedit-mousedown.md) -und [**mousup**](inkedit-mouseup.md) -Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="9fed2-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="9fed2-112">Verwenden Sie das [**MouseDown**](inkedit-mousedown.md) -und das [**MouseUp**](inkedit-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9fed2-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="9fed2-113">Wenn im **Click** -Ereignis Code vorhanden ist, wird das [**DblClick**](inkedit-dblclick.md) -Ereignis nie auslöst, da das **Click** -Ereignis das erste Ereignis ist, das zwischen beiden angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fed2-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="9fed2-114">Folglich wird der Maus Klick von dem **Click** -Ereignis abgefangen, sodass das **DblClick** -Ereignis nicht auftritt.</span><span class="sxs-lookup"><span data-stu-id="9fed2-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="9fed2-115">Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="9fed2-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="9fed2-116">Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ieeclick**.</span><span class="sxs-lookup"><span data-stu-id="9fed2-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fed2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fed2-117">Requirements</span></span>



| <span data-ttu-id="9fed2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fed2-118">Requirement</span></span> | <span data-ttu-id="9fed2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9fed2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fed2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fed2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9fed2-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fed2-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9fed2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fed2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9fed2-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9fed2-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9fed2-124">Header</span><span class="sxs-lookup"><span data-stu-id="9fed2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fed2-125"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="9fed2-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9fed2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9fed2-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9fed2-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fed2-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9fed2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fed2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fed2-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="9fed2-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




