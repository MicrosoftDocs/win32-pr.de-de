---
title: DRV_LOAD Meldung (MMSYSTEM. h)
description: Benachrichtigt den Treiber, dass er geladen wurde. Der Treiber sollte sicherstellen, dass Hardware und unterstützende Treiber, die für die ordnungsgemäße Funktion erforderlich sind, vorhanden sind.
ms.assetid: f3642d91-cea8-499d-8d2e-bf01a59a7d72
keywords:
- DRV_LOAD-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- DRV_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dda950eaa84f924f4845d99d5740e37d6b354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957165"
---
# <a name="drv_load-message"></a><span data-ttu-id="b143c-105">DRV- \_ Lade Nachricht</span><span class="sxs-lookup"><span data-stu-id="b143c-105">DRV\_LOAD message</span></span>

<span data-ttu-id="b143c-106">Benachrichtigt den Treiber, dass er geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b143c-106">Notifies the driver that it has been loaded.</span></span> <span data-ttu-id="b143c-107">Der Treiber sollte sicherstellen, dass Hardware und unterstützende Treiber, die für die ordnungsgemäße Funktion erforderlich sind, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b143c-107">The driver should make sure that any hardware and supporting drivers it needs to function properly are present.</span></span>

## <a name="parameters"></a><span data-ttu-id="b143c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b143c-108">Parameters</span></span>

<span data-ttu-id="b143c-109">Der *hdrvr* -Parameter ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b143c-109">The *hdrvr* parameter is always zero.</span></span> <span data-ttu-id="b143c-110">Die Parameter " *dwdriverid*", " *lParam1*" und " *lParam2* " werden nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b143c-110">The *dwDriverId*, *lParam1*, and *lParam2* parameters are not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b143c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b143c-111">Return Value</span></span>

<span data-ttu-id="b143c-112">Gibt einen Wert ungleich 0 (null) zurück, wenn erfolgreich, andernfalls</span><span class="sxs-lookup"><span data-stu-id="b143c-112">Returns nonzero if successful or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b143c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b143c-113">Remarks</span></span>

<span data-ttu-id="b143c-114">Die **drv- \_ Lade** Nachricht ist immer die erste Meldung, die ein Gerätetreiber erhält.</span><span class="sxs-lookup"><span data-stu-id="b143c-114">The **DRV\_LOAD** message is always the first message that a device driver receives.</span></span>

## <a name="requirements"></a><span data-ttu-id="b143c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b143c-115">Requirements</span></span>



| <span data-ttu-id="b143c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b143c-116">Requirement</span></span> | <span data-ttu-id="b143c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b143c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b143c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b143c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b143c-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b143c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b143c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b143c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b143c-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b143c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b143c-122">Header</span><span class="sxs-lookup"><span data-stu-id="b143c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b143c-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b143c-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b143c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b143c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b143c-125">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="b143c-125">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="b143c-126">Installierbare Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="b143c-126">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

 





