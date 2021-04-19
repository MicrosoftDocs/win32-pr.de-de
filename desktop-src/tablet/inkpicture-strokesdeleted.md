---
description: Tritt auf, nachdem IInkStrokeDisp-Objekte aus der Ink-Eigenschaft gelöscht wurden.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: InkPicture. StrokesDeleted-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355376"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="67486-103">InkPicture. StrokesDeleted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="67486-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="67486-104">Tritt auf, nachdem [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) -Objekte aus der [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) -Eigenschaft gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="67486-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="67486-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67486-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="67486-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67486-106">Parameters</span></span>

<span data-ttu-id="67486-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="67486-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67486-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67486-108">Return value</span></span>

<span data-ttu-id="67486-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="67486-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67486-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67486-110">Remarks</span></span>

<span data-ttu-id="67486-111">Es sind keine Ereignisdaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="67486-111">There is no event data.</span></span>

<span data-ttu-id="67486-112">Diese Ereignismethode wird in den Dispatch-only-Schnittstellen **\_ iinkoverlayevents** und **\_ iinkpictureevents** (Dispinterfaces) mit der ID "DISPID \_ ioestrokesdeleted" definiert.</span><span class="sxs-lookup"><span data-stu-id="67486-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="67486-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67486-113">Requirements</span></span>



| <span data-ttu-id="67486-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67486-114">Requirement</span></span> | <span data-ttu-id="67486-115">Wert</span><span class="sxs-lookup"><span data-stu-id="67486-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67486-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67486-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67486-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67486-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="67486-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67486-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67486-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="67486-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="67486-120">Header</span><span class="sxs-lookup"><span data-stu-id="67486-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67486-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="67486-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="67486-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67486-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="67486-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67486-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="67486-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67486-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67486-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="67486-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




