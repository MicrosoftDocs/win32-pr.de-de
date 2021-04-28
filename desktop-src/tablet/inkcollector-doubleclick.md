---
description: 'InkCollector.DoubleClick-Ereignis: Tritt auf, wenn auf das InkCollector- oder InkOverlay-Objekt doppelklickt.'
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: InkCollector.DoubleClick-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51c3fef9ee999bbe2701da64e09a360f07db345
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110208"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="faa79-103">InkCollector.DoubleClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="faa79-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="faa79-104">Tritt ein, wenn auf [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) doppelklickt wird.</span><span class="sxs-lookup"><span data-stu-id="faa79-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="faa79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="faa79-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="faa79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="faa79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa79-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="faa79-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="faa79-108">**VARIANT \_ TRUE,** um das Ereignis für das übergeordnete Steuerelement abzubricht; andernfalls **VARIANT \_ FALSE**.</span><span class="sxs-lookup"><span data-stu-id="faa79-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa79-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="faa79-109">Return value</span></span>

<span data-ttu-id="faa79-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="faa79-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa79-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faa79-111">Remarks</span></span>

<span data-ttu-id="faa79-112">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEDblClick definiert.</span><span class="sxs-lookup"><span data-stu-id="faa79-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="faa79-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa79-113">Requirements</span></span>



| <span data-ttu-id="faa79-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faa79-114">Requirement</span></span> | <span data-ttu-id="faa79-115">Wert</span><span class="sxs-lookup"><span data-stu-id="faa79-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faa79-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faa79-116">Minimum supported client</span></span><br/> | <span data-ttu-id="faa79-117">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="faa79-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="faa79-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faa79-118">Minimum supported server</span></span><br/> | <span data-ttu-id="faa79-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="faa79-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="faa79-120">Header</span><span class="sxs-lookup"><span data-stu-id="faa79-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa79-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="faa79-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="faa79-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="faa79-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="faa79-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faa79-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="faa79-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="faa79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faa79-125">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="faa79-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




