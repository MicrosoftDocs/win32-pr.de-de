---
description: Tritt auf, wenn ein Benutzer auf das InkPicture-Steuerelement klickt.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture. Click-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867728"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="a7721-103">InkPicture. Click-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a7721-103">InkPicture.Click event</span></span>

<span data-ttu-id="a7721-104">Tritt auf, wenn ein Benutzer auf das [InkPicture](inkpicture-control-reference.md) -Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="a7721-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7721-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7721-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="a7721-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7721-106">Parameters</span></span>

<span data-ttu-id="a7721-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="a7721-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7721-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7721-108">Return value</span></span>

<span data-ttu-id="a7721-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a7721-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7721-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7721-110">Remarks</span></span>

<span data-ttu-id="a7721-111">Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**mousdown**](inkpicture-mousedown.md) -und [**mousup**](inkpicture-mouseup.md) -Ereignisse generiert.</span><span class="sxs-lookup"><span data-stu-id="a7721-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="a7721-112">Verwenden Sie das [**MouseDown**](inkpicture-mousedown.md) -und das [**MouseUp**](inkpicture-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="a7721-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="a7721-113">Wenn im **Click** -Ereignis Code vorhanden ist, wird das [**DblClick**](inkpicture-dblclick.md) -Ereignis nie auslöst, da das **Click** -Ereignis das erste Ereignis ist, das zwischen beiden angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a7721-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="a7721-114">Folglich wird der Maus Klick von dem **Click** -Ereignis abgefangen, sodass das **DblClick** -Ereignis nicht auftritt.</span><span class="sxs-lookup"><span data-stu-id="a7721-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="a7721-115">Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="a7721-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="a7721-116">Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ipeclick**.</span><span class="sxs-lookup"><span data-stu-id="a7721-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7721-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7721-117">Requirements</span></span>



| <span data-ttu-id="a7721-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7721-118">Requirement</span></span> | <span data-ttu-id="a7721-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a7721-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7721-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7721-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7721-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7721-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a7721-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7721-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7721-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a7721-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a7721-124">Header</span><span class="sxs-lookup"><span data-stu-id="a7721-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7721-125"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7721-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7721-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7721-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7721-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7721-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a7721-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7721-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7721-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a7721-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




