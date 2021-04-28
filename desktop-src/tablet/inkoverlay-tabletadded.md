---
description: 'InkOverlay.TabletAdded-Ereignis: Tritt auf, wenn dem System eine IInkTablet hinzugefügt wird.'
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: InkOverlay.TabletAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c22630430622c98026c81adb1c6a131a53277a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116788"
---
# <a name="inkoverlaytabletadded-event"></a><span data-ttu-id="3b060-103">InkOverlay.TabletAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3b060-103">InkOverlay.TabletAdded event</span></span>

<span data-ttu-id="3b060-104">Tritt ein, wenn dem System eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3b060-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b060-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b060-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="3b060-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b060-107">*Tablet* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3b060-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b060-108">Das [**IInkTablet-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) das dem System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="3b060-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b060-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b060-109">Return value</span></span>

<span data-ttu-id="3b060-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3b060-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b060-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b060-111">Remarks</span></span>

<span data-ttu-id="3b060-112">Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICETabletAdded definiert.</span><span class="sxs-lookup"><span data-stu-id="3b060-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b060-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b060-113">Requirements</span></span>



| <span data-ttu-id="3b060-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b060-114">Requirement</span></span> | <span data-ttu-id="3b060-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3b060-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b060-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b060-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b060-117">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b060-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3b060-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b060-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b060-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3b060-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3b060-120">Header</span><span class="sxs-lookup"><span data-stu-id="3b060-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b060-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="3b060-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3b060-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3b060-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b060-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b060-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3b060-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3b060-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b060-125">**InkOverlay-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3b060-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="3b060-126">**IInkTablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3b060-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




