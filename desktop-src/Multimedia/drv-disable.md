---
title: DRV_DISABLE Meldung (MMSYSTEM. h)
description: Deaktiviert den Treiber. Der Treiber sollte das entsprechende Gerät (sofern vorhanden) in einen inaktiven Zustand versetzen und alle Rückruf Funktionen oder Threads beenden.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957168"
---
# <a name="drv_disable-message"></a><span data-ttu-id="d3b2c-105">DRV-Deaktivierungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="d3b2c-105">DRV\_DISABLE message</span></span>

<span data-ttu-id="d3b2c-106">Deaktiviert den Treiber.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-106">Disables the driver.</span></span> <span data-ttu-id="d3b2c-107">Der Treiber sollte das entsprechende Gerät (sofern vorhanden) in einen inaktiven Zustand versetzen und alle Rückruf Funktionen oder Threads beenden.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-107">The driver should place the corresponding device, if any, in an inactive state and terminate any callback functions or threads.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3b2c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3b2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b2c-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="d3b2c-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="d3b2c-110">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b2c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3b2c-111">Return Value</span></span>

<span data-ttu-id="d3b2c-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b2c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3b2c-113">Remarks</span></span>

<span data-ttu-id="d3b2c-114">Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="d3b2c-115">Nach der Deaktivierung des Treibers sendet das System in der Regel eine [**drv- \_ freie drv**](drv-free.md) -Nachricht, bevor der Treiber aus dem Arbeitsspeicher entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d3b2c-115">After disabling the driver, the system typically sends the driver a [**DRV\_FREE**](drv-free.md) message before removing the driver from memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b2c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3b2c-116">Requirements</span></span>



| <span data-ttu-id="d3b2c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3b2c-117">Requirement</span></span> | <span data-ttu-id="d3b2c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d3b2c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b2c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3b2c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b2c-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3b2c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3b2c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3b2c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b2c-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3b2c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d3b2c-123">Header</span><span class="sxs-lookup"><span data-stu-id="d3b2c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b2c-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b2c-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b2c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3b2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b2c-126">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="d3b2c-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="d3b2c-127">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="d3b2c-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





