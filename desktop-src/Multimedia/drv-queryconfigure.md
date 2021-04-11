---
title: DRV_QUERYCONFIGURE Meldung (MMSYSTEM. h)
description: Weist den Treiber an, anzugeben, ob die benutzerdefinierte Konfiguration unterstützt wird.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66780106fdd42364d247db534a838842f25dc16a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213738"
---
# <a name="drv_queryconfigure-message"></a><span data-ttu-id="12ad2-104">DRV- \_ queryconfigure-Meldung</span><span class="sxs-lookup"><span data-stu-id="12ad2-104">DRV\_QUERYCONFIGURE message</span></span>

<span data-ttu-id="12ad2-105">Weist den Treiber an, anzugeben, ob die benutzerdefinierte Konfiguration unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="12ad2-105">Directs the driver to specify whether it supports custom configuration.</span></span>

## <a name="parameters"></a><span data-ttu-id="12ad2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ad2-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="12ad2-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="12ad2-108">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="12ad2-108">Identifier of the installable driver.</span></span> <span data-ttu-id="12ad2-109">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="12ad2-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="12ad2-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="12ad2-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="12ad2-111">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="12ad2-111">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ad2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12ad2-112">Return Value</span></span>

<span data-ttu-id="12ad2-113">Gibt einen Wert ungleich 0 (null) zurück, wenn der Treiber ein Konfigurations Dialogfeld anzeigen kann, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="12ad2-113">Returns a nonzero value if the driver can display a configuration dialog box or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12ad2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12ad2-114">Remarks</span></span>

<span data-ttu-id="12ad2-115">Die Parameter *lParam1* und *lParam2* werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="12ad2-115">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="12ad2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12ad2-116">Requirements</span></span>



| <span data-ttu-id="12ad2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12ad2-117">Requirement</span></span> | <span data-ttu-id="12ad2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="12ad2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12ad2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12ad2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="12ad2-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ad2-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="12ad2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12ad2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="12ad2-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ad2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="12ad2-123">Header</span><span class="sxs-lookup"><span data-stu-id="12ad2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ad2-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12ad2-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ad2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12ad2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ad2-126">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="12ad2-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="12ad2-127">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="12ad2-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





