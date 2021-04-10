---
title: DRV_REMOVE Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll. Wenn ein Treiber diese Nachricht empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfc94d648f83e618a20323ed7bbe3694616bc06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040989"
---
# <a name="drv_remove-message"></a><span data-ttu-id="b4bef-105">DRV- \_ Entfernungs Meldung</span><span class="sxs-lookup"><span data-stu-id="b4bef-105">DRV\_REMOVE message</span></span>

<span data-ttu-id="b4bef-106">Benachrichtigt den Treiber, dass er aus dem System entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4bef-106">Notifies the driver that it is about to be removed from the system.</span></span> <span data-ttu-id="b4bef-107">Wenn ein Treiber diese Nachricht empfängt, sollte er alle Abschnitte entfernen, die er in der Registrierung erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="b4bef-107">When a driver receives this message, it should remove any sections it created in the registry.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4bef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4bef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4bef-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwdriverid*</span><span class="sxs-lookup"><span data-stu-id="b4bef-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="b4bef-110">Der Bezeichner des installierbaren Treibers.</span><span class="sxs-lookup"><span data-stu-id="b4bef-110">Identifier of the installable driver.</span></span> <span data-ttu-id="b4bef-111">Dabei handelt es sich um den gleichen Wert, der zuvor vom Treiber aus der von [**drv \_ geöffneten**](drv-open.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b4bef-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="b4bef-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="b4bef-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="b4bef-113">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="b4bef-113">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4bef-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4bef-114">Return Value</span></span>

<span data-ttu-id="b4bef-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="b4bef-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4bef-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4bef-116">Remarks</span></span>

<span data-ttu-id="b4bef-117">Die Parameter *lParam1* und *lParam2* werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4bef-117">The *lParam1* and *lParam2* parameters are not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4bef-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4bef-118">Requirements</span></span>



| <span data-ttu-id="b4bef-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4bef-119">Requirement</span></span> | <span data-ttu-id="b4bef-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b4bef-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4bef-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4bef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b4bef-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4bef-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b4bef-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4bef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b4bef-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4bef-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b4bef-125">Header</span><span class="sxs-lookup"><span data-stu-id="b4bef-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4bef-126"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4bef-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4bef-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4bef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4bef-128">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="b4bef-128">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="b4bef-129">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="b4bef-129">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





