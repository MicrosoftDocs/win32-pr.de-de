---
description: 'InkPicture.TabletAdded-Ereignis: Tritt auf, wenn dem System eine IInkTablet hinzugefügt wird.'
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: InkPicture.TabletAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c5121b668f27034a04230311ee88ebb7564802
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113658"
---
# <a name="inkpicturetabletadded-event"></a><span data-ttu-id="a868b-103">InkPicture.TabletAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a868b-103">InkPicture.TabletAdded event</span></span>

<span data-ttu-id="a868b-104">Tritt ein, wenn dem System eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a868b-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a868b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a868b-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="a868b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a868b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a868b-107">*Tablet* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a868b-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a868b-108">Das [**IInkTablet-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) das dem System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a868b-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a868b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a868b-109">Return value</span></span>

<span data-ttu-id="a868b-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a868b-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a868b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a868b-111">Remarks</span></span>

<span data-ttu-id="a868b-112">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICETabletAdded definiert.</span><span class="sxs-lookup"><span data-stu-id="a868b-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a868b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a868b-113">Requirements</span></span>



| <span data-ttu-id="a868b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a868b-114">Requirement</span></span> | <span data-ttu-id="a868b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a868b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a868b-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a868b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a868b-117">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a868b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a868b-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a868b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a868b-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a868b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a868b-120">Header</span><span class="sxs-lookup"><span data-stu-id="a868b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a868b-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="a868b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a868b-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a868b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a868b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a868b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a868b-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a868b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a868b-125">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="a868b-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a868b-126">**IInkTablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a868b-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




