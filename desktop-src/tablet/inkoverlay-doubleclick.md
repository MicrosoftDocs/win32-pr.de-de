---
description: 'InkOverlay.DoubleClick-Ereignis: Tritt auf, wenn auf das InkCollector- oder InkOverlay-Objekt doppelklickt.'
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: InkOverlay.DoubleClick-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086828"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="6af75-103">InkOverlay.DoubleClick-Ereignis</span><span class="sxs-lookup"><span data-stu-id="6af75-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="6af75-104">Tritt ein, wenn auf [**das InkCollector-**](inkcollector-class.md) oder [**InkOverlay-Objekt**](inkoverlay-class.md) doppelklickt wird.</span><span class="sxs-lookup"><span data-stu-id="6af75-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af75-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6af75-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6af75-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6af75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af75-107">*Abbrechen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6af75-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6af75-108">Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6af75-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af75-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6af75-109">Return value</span></span>

<span data-ttu-id="6af75-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6af75-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af75-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6af75-111">Remarks</span></span>

<span data-ttu-id="6af75-112">Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ IPEDblClick definiert.</span><span class="sxs-lookup"><span data-stu-id="6af75-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af75-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6af75-113">Requirements</span></span>



| <span data-ttu-id="6af75-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6af75-114">Requirement</span></span> | <span data-ttu-id="6af75-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6af75-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af75-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6af75-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6af75-117">Nur Desktop-Apps für Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="6af75-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6af75-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6af75-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6af75-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6af75-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6af75-120">Header</span><span class="sxs-lookup"><span data-stu-id="6af75-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af75-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="6af75-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6af75-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6af75-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6af75-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af75-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6af75-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6af75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6af75-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6af75-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




