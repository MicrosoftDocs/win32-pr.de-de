---
description: Tritt auf, bevor Striche aus der Ink-Eigenschaft gelöscht werden.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: InkOverlay. strokeslösch-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960501"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="75fca-103">InkOverlay. strokeslösch-Ereignis</span><span class="sxs-lookup"><span data-stu-id="75fca-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="75fca-104">Tritt auf, bevor Striche aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) -Eigenschaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="75fca-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="75fca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75fca-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="75fca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75fca-107">*Striche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75fca-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75fca-108">Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die beim Auslösen des **strokeslösch** -Ereignisses gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="75fca-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75fca-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75fca-109">Return value</span></span>

<span data-ttu-id="75fca-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="75fca-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75fca-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75fca-111">Remarks</span></span>

<span data-ttu-id="75fca-112">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID "DISPID \_ ioestrokeslösch" definiert.</span><span class="sxs-lookup"><span data-stu-id="75fca-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="75fca-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75fca-113">Requirements</span></span>



| <span data-ttu-id="75fca-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75fca-114">Requirement</span></span> | <span data-ttu-id="75fca-115">Wert</span><span class="sxs-lookup"><span data-stu-id="75fca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75fca-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75fca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="75fca-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75fca-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="75fca-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75fca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="75fca-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75fca-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="75fca-120">Header</span><span class="sxs-lookup"><span data-stu-id="75fca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="75fca-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="75fca-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="75fca-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75fca-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="75fca-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75fca-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="75fca-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75fca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75fca-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="75fca-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="75fca-126">[**Ink \[ -Eigenschaft InkCollector/InkOverlay-Klasse\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="75fca-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

