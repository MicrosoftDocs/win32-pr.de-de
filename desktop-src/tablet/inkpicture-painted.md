---
description: Tritt auf, wenn das InkPicture-Steuerelement das erneute zeichnen selbst abgeschlossen hat.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: InkPicture. gezeichnet-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348687"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="d2e20-103">InkPicture. gezeichnet-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d2e20-103">InkPicture.Painted event</span></span>

<span data-ttu-id="d2e20-104">Tritt auf, wenn das [InkPicture](inkpicture-control-reference.md) -Steuerelement das erneute zeichnen selbst abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="d2e20-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e20-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2e20-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="d2e20-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2e20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e20-107">*hdc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2e20-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e20-108">Der Gerätekontext, in dem das Ereignis aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d2e20-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d2e20-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2e20-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e20-110">Das [**inkrechteck**](inkrectangle-class.md) , das neu gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2e20-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e20-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2e20-111">Return value</span></span>

<span data-ttu-id="d2e20-112">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2e20-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e20-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2e20-113">Remarks</span></span>

<span data-ttu-id="d2e20-114">Diese Ereignismethode wird in den **\_ iinkoverlayevents** -und **\_ iinkpictureevents** -DISP mit der ID DISPID \_ ioegezeichnet definiert.</span><span class="sxs-lookup"><span data-stu-id="d2e20-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e20-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2e20-115">Requirements</span></span>



| <span data-ttu-id="d2e20-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2e20-116">Requirement</span></span> | <span data-ttu-id="d2e20-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d2e20-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e20-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2e20-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e20-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2e20-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d2e20-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2e20-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e20-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d2e20-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d2e20-122">Header</span><span class="sxs-lookup"><span data-stu-id="d2e20-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e20-123"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d2e20-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2e20-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2e20-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2e20-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2e20-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d2e20-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2e20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e20-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d2e20-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




