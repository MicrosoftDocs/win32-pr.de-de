---
description: Tritt auf, wenn ein iinktablet aus dem System entfernt wird.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: InkCollector. tabletreverschober Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec723a6752f79a1a1d56d318d49ec3d025919d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345090"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="3df77-103">InkCollector. tabletreverschogereignis</span><span class="sxs-lookup"><span data-stu-id="3df77-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="3df77-104">Tritt auf, wenn ein [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aus dem System entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3df77-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df77-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="3df77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3df77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df77-107">*Tabletid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3df77-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3df77-108">Der Long-Wert, der als ID für das [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt verwendet wurde, das entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="3df77-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3df77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3df77-109">Return value</span></span>

<span data-ttu-id="3df77-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3df77-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3df77-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3df77-111">Remarks</span></span>

<span data-ttu-id="3df77-112">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icetabletreverschot definiert.</span><span class="sxs-lookup"><span data-stu-id="3df77-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="3df77-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3df77-113">Requirements</span></span>



| <span data-ttu-id="3df77-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3df77-114">Requirement</span></span> | <span data-ttu-id="3df77-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3df77-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df77-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3df77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3df77-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3df77-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3df77-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3df77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3df77-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3df77-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3df77-120">Header</span><span class="sxs-lookup"><span data-stu-id="3df77-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3df77-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3df77-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3df77-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3df77-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="3df77-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3df77-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3df77-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3df77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df77-125">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3df77-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="3df77-126">**Iinktablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3df77-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




