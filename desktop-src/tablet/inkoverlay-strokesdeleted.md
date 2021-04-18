---
description: Tritt auf, nachdem Striche aus der Ink-Eigenschaft gelöscht wurden.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: InkOverlay. StrokesDeleted-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216412"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="ddb45-103">InkOverlay. StrokesDeleted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ddb45-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="ddb45-104">Tritt auf, nachdem Striche aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ddb45-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb45-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddb45-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="ddb45-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddb45-106">Parameters</span></span>

<span data-ttu-id="ddb45-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="ddb45-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ddb45-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ddb45-108">Return value</span></span>

<span data-ttu-id="ddb45-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ddb45-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb45-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb45-110">Remarks</span></span>

<span data-ttu-id="ddb45-111">Es sind keine Ereignisdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ddb45-111">There is no event data.</span></span>

<span data-ttu-id="ddb45-112">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID "DISPID \_ ioestrokesdeleted" definiert.</span><span class="sxs-lookup"><span data-stu-id="ddb45-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb45-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddb45-113">Requirements</span></span>



| <span data-ttu-id="ddb45-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddb45-114">Requirement</span></span> | <span data-ttu-id="ddb45-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ddb45-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb45-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddb45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb45-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddb45-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ddb45-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddb45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb45-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ddb45-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ddb45-120">Header</span><span class="sxs-lookup"><span data-stu-id="ddb45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddb45-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb45-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ddb45-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ddb45-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddb45-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb45-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ddb45-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddb45-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb45-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ddb45-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="ddb45-126">[**Ink \[ -Eigenschaft InkCollector/InkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="ddb45-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




