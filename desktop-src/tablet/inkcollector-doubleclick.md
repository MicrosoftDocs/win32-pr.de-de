---
description: Tritt auf, wenn auf das InkCollector-oder InkOverlay-Objekt Doppel geklickt wird.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: InkCollector. DoubleClick-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862095"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="fd471-103">InkCollector. DoubleClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fd471-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="fd471-104">Tritt auf, wenn auf das [**InkCollector**](inkcollector-class.md) -oder [**InkOverlay**](inkoverlay-class.md) -Objekt Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="fd471-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd471-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd471-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="fd471-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd471-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd471-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd471-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd471-108">**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="fd471-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd471-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd471-109">Return value</span></span>

<span data-ttu-id="fd471-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fd471-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd471-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd471-111">Remarks</span></span>

<span data-ttu-id="fd471-112">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ ipedblclick definiert.</span><span class="sxs-lookup"><span data-stu-id="fd471-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd471-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd471-113">Requirements</span></span>



| <span data-ttu-id="fd471-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd471-114">Requirement</span></span> | <span data-ttu-id="fd471-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fd471-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd471-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd471-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd471-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd471-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd471-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd471-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd471-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fd471-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fd471-120">Header</span><span class="sxs-lookup"><span data-stu-id="fd471-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd471-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fd471-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fd471-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fd471-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd471-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd471-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fd471-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd471-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd471-125">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fd471-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




