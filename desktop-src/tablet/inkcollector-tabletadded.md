---
description: 'InkCollector.TabletAdded-Ereignis: Tritt auf, wenn dem System eine IInkTablet hinzugefügt wird.'
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: InkCollector.TabletAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110008"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="aee12-103">InkCollector.TabletAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="aee12-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="aee12-104">Tritt ein, wenn dem System eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="aee12-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aee12-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="aee12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aee12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee12-107">*Tablet* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aee12-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee12-108">Das [**IInkTablet-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) das dem System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="aee12-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee12-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aee12-109">Return value</span></span>

<span data-ttu-id="aee12-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="aee12-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aee12-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aee12-111">Remarks</span></span>

<span data-ttu-id="aee12-112">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICETabletAdded definiert.</span><span class="sxs-lookup"><span data-stu-id="aee12-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee12-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aee12-113">Requirements</span></span>



| <span data-ttu-id="aee12-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aee12-114">Requirement</span></span> | <span data-ttu-id="aee12-115">Wert</span><span class="sxs-lookup"><span data-stu-id="aee12-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee12-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aee12-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aee12-117">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="aee12-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="aee12-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aee12-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aee12-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aee12-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="aee12-120">Header</span><span class="sxs-lookup"><span data-stu-id="aee12-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee12-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="aee12-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="aee12-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aee12-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="aee12-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee12-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="aee12-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aee12-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee12-125">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aee12-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="aee12-126">**IInkTablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="aee12-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




