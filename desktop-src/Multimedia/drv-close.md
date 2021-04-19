---
title: DRV_CLOSE Meldung (MMSYSTEM. h)
description: Weist den Treiber an, die angegebene-Instanz zu schließen. Wenn keine anderen Instanzen geöffnet sind, sollte der Treiber für die nachfolgende Freigabe aus dem Arbeitsspeicher vorbereitet werden.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343063"
---
# <a name="drv_close-message"></a><span data-ttu-id="98c88-105">DRV- \_ Schließen-Meldung</span><span class="sxs-lookup"><span data-stu-id="98c88-105">DRV\_CLOSE message</span></span>

<span data-ttu-id="98c88-106">Weist den Treiber an, die angegebene-Instanz zu schließen.</span><span class="sxs-lookup"><span data-stu-id="98c88-106">Directs the driver to close the given instance.</span></span> <span data-ttu-id="98c88-107">Wenn keine anderen Instanzen geöffnet sind, sollte der Treiber für die nachfolgende Freigabe aus dem Arbeitsspeicher vorbereitet werden.</span><span class="sxs-lookup"><span data-stu-id="98c88-107">If no other instances are open, the driver should prepare for subsequent release from memory.</span></span>

## <a name="parameters"></a><span data-ttu-id="98c88-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="98c88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c88-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="98c88-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="98c88-110">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="98c88-110">Identifier of the installable driver.</span></span> <span data-ttu-id="98c88-111">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="98c88-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="98c88-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="98c88-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="98c88-113">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="98c88-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="98c88-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="98c88-114"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="98c88-115">32-Bit-Wert, der in einem Aufrufen der **driverclose** -Funktion als *lParam1* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98c88-115">32-bit value specified as the *lParam1* parameter in a call to the **DriverClose** function.</span></span>

</dd> <dt>

<span data-ttu-id="98c88-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="98c88-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="98c88-117">32-Bit-Wert, der in einem Aufrufen der **driverclose** -Funktion als *lParam2* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="98c88-117">32-bit value specified as the *lParam2* parameter in a call to the **DriverClose** function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c88-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98c88-118">Return Value</span></span>

<span data-ttu-id="98c88-119">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls</span><span class="sxs-lookup"><span data-stu-id="98c88-119">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c88-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98c88-120">Requirements</span></span>



| <span data-ttu-id="98c88-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98c88-121">Requirement</span></span> | <span data-ttu-id="98c88-122">Wert</span><span class="sxs-lookup"><span data-stu-id="98c88-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c88-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98c88-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98c88-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98c88-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="98c88-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98c88-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98c88-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98c88-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="98c88-127">Header</span><span class="sxs-lookup"><span data-stu-id="98c88-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c88-128"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c88-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c88-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98c88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c88-130">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="98c88-130">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="98c88-131">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="98c88-131">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





