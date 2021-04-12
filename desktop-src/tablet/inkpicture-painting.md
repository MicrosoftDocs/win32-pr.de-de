---
description: Tritt ein, bevor das InkPicture-Steuerelement sich selbst neu zeichnet.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: InkPicture. Paint-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216588"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="fa463-103">InkPicture. Paint-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fa463-103">InkPicture.Painting event</span></span>

<span data-ttu-id="fa463-104">Tritt ein, bevor das [InkPicture](inkpicture-control-reference.md) -Steuerelement sich selbst neu zeichnet.</span><span class="sxs-lookup"><span data-stu-id="fa463-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa463-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa463-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="fa463-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa463-107">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa463-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa463-108">Der Gerätekontext, auf dem gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa463-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="fa463-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa463-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa463-110">Das frei zuzeichnende frei Hand Rechteck.</span><span class="sxs-lookup"><span data-stu-id="fa463-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="fa463-111">*Zulassen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa463-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa463-112">Gibt an, ob der Repaint-Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa463-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa463-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa463-113">Return value</span></span>

<span data-ttu-id="fa463-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fa463-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa463-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa463-115">Remarks</span></span>

<span data-ttu-id="fa463-116">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID DISPID \_ ioepaint definiert.</span><span class="sxs-lookup"><span data-stu-id="fa463-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa463-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa463-117">Requirements</span></span>



| <span data-ttu-id="fa463-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa463-118">Requirement</span></span> | <span data-ttu-id="fa463-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fa463-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa463-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa463-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fa463-121">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa463-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fa463-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa463-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fa463-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fa463-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fa463-124">Header</span><span class="sxs-lookup"><span data-stu-id="fa463-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa463-125"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa463-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa463-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fa463-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa463-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa463-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fa463-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa463-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa463-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="fa463-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




