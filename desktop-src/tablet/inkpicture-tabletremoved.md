---
description: 'InkPicture.TabletRemoved-Ereignis: Tritt auf, wenn eine IInkTablet aus dem System entfernt wird.'
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: InkPicture.TabletRemoved-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929458c6b972143852b5921a8c8364a54a4b6f41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113648"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="53424-103">InkPicture.TabletRemoved-Ereignis</span><span class="sxs-lookup"><span data-stu-id="53424-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="53424-104">Tritt ein, wenn eine [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="53424-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="53424-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53424-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="53424-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53424-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53424-107">*TabletId* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="53424-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53424-108">Der long-Wert, der als ID für das [**entfernte IInkTablet-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="53424-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53424-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53424-109">Return value</span></span>

<span data-ttu-id="53424-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="53424-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53424-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53424-111">Remarks</span></span>

<span data-ttu-id="53424-112">Diese Ereignismethode wird in den Dispatch-Only-Schnittstellen **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** und **\_ IInkPictureEvents** (dispinterfaces) mit der ID DISPID \_ ICETabletRemoved definiert.</span><span class="sxs-lookup"><span data-stu-id="53424-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="53424-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53424-113">Requirements</span></span>



| <span data-ttu-id="53424-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53424-114">Requirement</span></span> | <span data-ttu-id="53424-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53424-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53424-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53424-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53424-117">Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="53424-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="53424-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53424-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53424-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="53424-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="53424-120">Header</span><span class="sxs-lookup"><span data-stu-id="53424-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53424-121"><dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="53424-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="53424-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53424-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="53424-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53424-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="53424-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="53424-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53424-125">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="53424-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="53424-126">**IInkTablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="53424-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




