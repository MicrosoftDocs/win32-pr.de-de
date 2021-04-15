---
description: Tritt ein, bevor das InkOverlay-Objekt oder InkPicture das erneute Zeichnen von sich selbst abgeschlossen hat.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: InkOverlay. Paint-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529903"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="210c2-103">InkOverlay. Paint-Ereignis</span><span class="sxs-lookup"><span data-stu-id="210c2-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="210c2-104">Tritt ein, bevor das [**InkOverlay**](inkoverlay-class.md) -Objekt oder [InkPicture](inkpicture-control-reference.md) das erneute Zeichnen von sich selbst abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="210c2-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="210c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="210c2-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="210c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="210c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="210c2-107">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="210c2-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="210c2-108">Der Gerätekontext, auf dem gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="210c2-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="210c2-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="210c2-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="210c2-110">Das Rechteck, das neu gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="210c2-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="210c2-111">*Zulassen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="210c2-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="210c2-112">Gibt an, ob der Repaint-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="210c2-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="210c2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="210c2-113">Return value</span></span>

<span data-ttu-id="210c2-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="210c2-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="210c2-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="210c2-115">Remarks</span></span>

<span data-ttu-id="210c2-116">Diese Ereignismethode wird in den \_ Dispatch-only-Schnittstellen iinkoverlayevents und \_ iinkpictureevents (Dispinterfaces) mit der ID DISPID \_ ioepaint definiert.</span><span class="sxs-lookup"><span data-stu-id="210c2-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="210c2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="210c2-117">Requirements</span></span>



| <span data-ttu-id="210c2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="210c2-118">Requirement</span></span> | <span data-ttu-id="210c2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="210c2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="210c2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="210c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="210c2-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="210c2-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="210c2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="210c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="210c2-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="210c2-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="210c2-124">Header</span><span class="sxs-lookup"><span data-stu-id="210c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="210c2-125"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="210c2-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="210c2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="210c2-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="210c2-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="210c2-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="210c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="210c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="210c2-129">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="210c2-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




