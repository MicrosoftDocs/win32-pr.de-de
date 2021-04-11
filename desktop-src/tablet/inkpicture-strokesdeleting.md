---
description: Tritt auf, bevor IInkStrokeDisp-Objekte aus der Ink-Eigenschaft gelöscht werden.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: InkPicture. strokeslösch-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042718"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="1ed67-103">InkPicture. strokeslösch-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1ed67-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="1ed67-104">Tritt auf, bevor [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) -Eigenschaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1ed67-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ed67-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="1ed67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ed67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed67-107">*Striche* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed67-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed67-108">Die [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung, die beim Auslösen des **strokeslösch** -Ereignisses gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="1ed67-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed67-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ed67-109">Return value</span></span>

<span data-ttu-id="1ed67-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1ed67-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed67-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ed67-111">Remarks</span></span>

<span data-ttu-id="1ed67-112">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID "DISPID \_ ioestrokeslösch" definiert.</span><span class="sxs-lookup"><span data-stu-id="1ed67-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed67-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ed67-113">Requirements</span></span>



| <span data-ttu-id="1ed67-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ed67-114">Requirement</span></span> | <span data-ttu-id="1ed67-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1ed67-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed67-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ed67-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed67-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ed67-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1ed67-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ed67-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed67-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ed67-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1ed67-120">Header</span><span class="sxs-lookup"><span data-stu-id="1ed67-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed67-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1ed67-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1ed67-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ed67-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ed67-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ed67-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1ed67-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ed67-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed67-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1ed67-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

