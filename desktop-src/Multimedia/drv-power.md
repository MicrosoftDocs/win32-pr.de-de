---
title: DRV_POWER Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass die Stromversorgung des Geräts aktiviert oder deaktiviert ist.
ms.assetid: b3bbd16a-5b90-4127-a1dd-f2ddfd918f0a
keywords:
- DRV_POWER-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_POWER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8113b7fe544bf36a35b6e516c7a98ae71082577d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957163"
---
# <a name="drv_power-message"></a><span data-ttu-id="4bfb6-104">DRV- \_ Strom Meldung</span><span class="sxs-lookup"><span data-stu-id="4bfb6-104">DRV\_POWER message</span></span>

<span data-ttu-id="4bfb6-105">Benachrichtigt den Treiber, dass die Stromversorgung des Geräts aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4bfb6-105">Notifies the driver that power to the device is being turned on or off.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bfb6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bfb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfb6-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="4bfb6-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="4bfb6-108">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="4bfb6-108">Identifier of the installable driver.</span></span> <span data-ttu-id="4bfb6-109">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="4bfb6-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="4bfb6-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="4bfb6-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="4bfb6-111">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="4bfb6-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfb6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bfb6-112">Return Value</span></span>

<span data-ttu-id="4bfb6-113">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls</span><span class="sxs-lookup"><span data-stu-id="4bfb6-113">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfb6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bfb6-114">Remarks</span></span>

<span data-ttu-id="4bfb6-115">Die Parameter *lParam1* und *lParam2* werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4bfb6-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfb6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bfb6-116">Requirements</span></span>



| <span data-ttu-id="4bfb6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bfb6-117">Requirement</span></span> | <span data-ttu-id="4bfb6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="4bfb6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfb6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bfb6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfb6-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bfb6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4bfb6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bfb6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfb6-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bfb6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4bfb6-123">Header</span><span class="sxs-lookup"><span data-stu-id="4bfb6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bfb6-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bfb6-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfb6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bfb6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfb6-126">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="4bfb6-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="4bfb6-127">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="4bfb6-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





