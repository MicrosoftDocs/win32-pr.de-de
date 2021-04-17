---
description: Tritt auf, wenn das InkOverlay-Objekt oder InkPicture-Steuerelement das erneute zeichnen selbst abgeschlossen hat.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: InkOverlay. gezeichnet-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485763"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="903c0-103">InkOverlay. gezeichnet-Ereignis</span><span class="sxs-lookup"><span data-stu-id="903c0-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="903c0-104">Tritt auf, wenn das [**InkOverlay**](inkoverlay-class.md) -Objekt oder [InkPicture](inkpicture-control-reference.md) -Steuerelement das erneute zeichnen selbst abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="903c0-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="903c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="903c0-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="903c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="903c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903c0-107">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="903c0-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903c0-108">Der Gerätekontext, in dem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="903c0-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="903c0-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="903c0-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="903c0-110">Das [**inkrechteck**](inkrectangle-class.md) , das neu gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="903c0-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="903c0-111">Return value</span></span>

<span data-ttu-id="903c0-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="903c0-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="903c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="903c0-113">Remarks</span></span>

<span data-ttu-id="903c0-114">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioegezeichnet definiert.</span><span class="sxs-lookup"><span data-stu-id="903c0-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="903c0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="903c0-115">Requirements</span></span>



| <span data-ttu-id="903c0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="903c0-116">Requirement</span></span> | <span data-ttu-id="903c0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="903c0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903c0-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="903c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="903c0-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="903c0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="903c0-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="903c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="903c0-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="903c0-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="903c0-122">Header</span><span class="sxs-lookup"><span data-stu-id="903c0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="903c0-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="903c0-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="903c0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="903c0-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="903c0-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="903c0-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="903c0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="903c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903c0-127">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="903c0-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




