---
title: DRV_FREE Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird. Der Treiber sollte jeglichen Arbeitsspeicher und andere Systemressourcen freigeben, die er zugewiesen hat.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957167"
---
# <a name="drv_free-message"></a><span data-ttu-id="710ea-105">Freie drv- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="710ea-105">DRV\_FREE message</span></span>

<span data-ttu-id="710ea-106">Benachrichtigt den Treiber, dass er aus dem Arbeitsspeicher entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="710ea-106">Notifies the driver that it is being removed from memory.</span></span> <span data-ttu-id="710ea-107">Der Treiber sollte jeglichen Arbeitsspeicher und andere Systemressourcen freigeben, die er zugewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="710ea-107">The driver should free any memory and other system resources that it has allocated.</span></span>

## <a name="parameters"></a><span data-ttu-id="710ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="710ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="710ea-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="710ea-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="710ea-110">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="710ea-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="710ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="710ea-111">Return Value</span></span>

<span data-ttu-id="710ea-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="710ea-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="710ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="710ea-113">Remarks</span></span>

<span data-ttu-id="710ea-114">Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="710ea-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="710ea-115">Die **\_ freie drv** -Nachricht ist immer die letzte Nachricht, die ein Gerätetreiber erhält.</span><span class="sxs-lookup"><span data-stu-id="710ea-115">The **DRV\_FREE** message is always the last message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="710ea-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="710ea-116">Requirements</span></span>



| <span data-ttu-id="710ea-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="710ea-117">Requirement</span></span> | <span data-ttu-id="710ea-118">Wert</span><span class="sxs-lookup"><span data-stu-id="710ea-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="710ea-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="710ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="710ea-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710ea-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="710ea-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="710ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="710ea-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="710ea-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="710ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="710ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="710ea-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="710ea-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710ea-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="710ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="710ea-126">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="710ea-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="710ea-127">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="710ea-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





