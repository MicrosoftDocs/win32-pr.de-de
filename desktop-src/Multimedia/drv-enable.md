---
title: DRV_ENABLE Meldung (MMSYSTEM. h)
description: Aktiviert den Treiber. Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe-und Ausgabeschnittstelle (e/a) suchen.
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957170"
---
# <a name="drv_enable-message"></a><span data-ttu-id="53ed3-105">DRV- \_ Aktivierungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="53ed3-105">DRV\_ENABLE message</span></span>

<span data-ttu-id="53ed3-106">Aktiviert den Treiber.</span><span class="sxs-lookup"><span data-stu-id="53ed3-106">Enables the driver.</span></span> <span data-ttu-id="53ed3-107">Der Treiber sollte alle Variablen initialisieren und Geräte mit der Eingabe-und Ausgabeschnittstelle (e/a) suchen.</span><span class="sxs-lookup"><span data-stu-id="53ed3-107">The driver should initialize any variables and locate devices with the input and output (I/O) interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="53ed3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="53ed3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ed3-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="53ed3-109"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="53ed3-110">Handle der installierbaren Treiber Instanz.</span><span class="sxs-lookup"><span data-stu-id="53ed3-110">Handle of the installable driver instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ed3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53ed3-111">Return Value</span></span>

<span data-ttu-id="53ed3-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="53ed3-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53ed3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53ed3-113">Remarks</span></span>

<span data-ttu-id="53ed3-114">Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="53ed3-114">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

<span data-ttu-id="53ed3-115">Treiber werden ab dem Zeitpunkt, an dem Sie diese Nachricht empfangen, als aktiviert eingestuft, bis Sie mithilfe der [**drv- \_**](drv-disable.md) Deaktivierungs Nachricht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="53ed3-115">Drivers are considered enabled from the time they receive this message until they are disabled by using the [**DRV\_DISABLE**](drv-disable.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="53ed3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53ed3-116">Requirements</span></span>



| <span data-ttu-id="53ed3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53ed3-117">Requirement</span></span> | <span data-ttu-id="53ed3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="53ed3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53ed3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53ed3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53ed3-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53ed3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53ed3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53ed3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53ed3-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53ed3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53ed3-123">Header</span><span class="sxs-lookup"><span data-stu-id="53ed3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53ed3-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53ed3-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53ed3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53ed3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ed3-126">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="53ed3-126">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="53ed3-127">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="53ed3-127">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





