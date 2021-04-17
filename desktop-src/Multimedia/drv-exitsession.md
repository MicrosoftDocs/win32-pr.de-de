---
title: DRV_EXITSESSION Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass die Beendigung von Windows vorbereitet wird. Der Treiber sollte sich auf die Beendigung vorbereiten.
ms.assetid: 8d200d64-b89b-47f1-ad21-ab86987efa4b
keywords:
- DRV_EXITSESSION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_EXITSESSION
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236da457541af2d594bc708caf5b5ed07e58cc04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479149"
---
# <a name="drv_exitsession-message"></a><span data-ttu-id="cdcaa-105">DRV- \_ exitsession-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cdcaa-105">DRV\_EXITSESSION message</span></span>

<span data-ttu-id="cdcaa-106">Benachrichtigt den Treiber, dass die Beendigung von Windows vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-106">Notifies the driver that Windows is preparing to exit.</span></span> <span data-ttu-id="cdcaa-107">Der Treiber sollte sich auf die Beendigung vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-107">The driver should prepare for termination.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdcaa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdcaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdcaa-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="cdcaa-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="cdcaa-110">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-110">Identifier of the installable driver.</span></span> <span data-ttu-id="cdcaa-111">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="cdcaa-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="cdcaa-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="cdcaa-113">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdcaa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdcaa-114">Return Value</span></span>

<span data-ttu-id="cdcaa-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdcaa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cdcaa-116">Remarks</span></span>

<span data-ttu-id="cdcaa-117">Die Parameter *lParam1* und *lParam2* werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdcaa-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcaa-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdcaa-118">Requirements</span></span>



| <span data-ttu-id="cdcaa-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdcaa-119">Requirement</span></span> | <span data-ttu-id="cdcaa-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cdcaa-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcaa-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdcaa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcaa-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdcaa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cdcaa-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdcaa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcaa-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdcaa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cdcaa-125">Header</span><span class="sxs-lookup"><span data-stu-id="cdcaa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdcaa-126"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdcaa-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcaa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdcaa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcaa-128">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="cdcaa-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="cdcaa-129">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="cdcaa-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





