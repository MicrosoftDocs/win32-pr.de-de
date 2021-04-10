---
title: UDM_SETPOS32 Meldung (kommstrg. h)
description: Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- Windows-Steuerelemente für UDM_SETPOS32 Meldung
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0153305bb535a79dbed59e8d42a7c25157c30cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956791"
---
# <a name="udm_setpos32-message"></a><span data-ttu-id="f8f02-104">UDM \_ SETPOS32 Meldung</span><span class="sxs-lookup"><span data-stu-id="f8f02-104">UDM\_SETPOS32 message</span></span>

<span data-ttu-id="f8f02-105">Legt die Position eines auf-ab-Steuer Elements mit 32-Bit-Genauigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="f8f02-105">Sets the position of an up-down control with 32-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8f02-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8f02-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f8f02-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f8f02-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f8f02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8f02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f02-110">Eine Variable vom Typ Integer, die die neue Position für das auf-ab-Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="f8f02-110">Variable of type integer that specifies the new position for the up-down control.</span></span> <span data-ttu-id="f8f02-111">Wenn der-Parameter außerhalb des angegebenen Bereichs des Steuer Elements liegt, wird *LPARAM* auf den nächstgelegenen gültigen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8f02-111">If the parameter is outside the control's specified range, *lParam* is set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f02-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8f02-112">Return value</span></span>

<span data-ttu-id="f8f02-113">Gibt die vorherige Position zurück.</span><span class="sxs-lookup"><span data-stu-id="f8f02-113">Returns the previous position.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f02-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8f02-114">Requirements</span></span>



| <span data-ttu-id="f8f02-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8f02-115">Requirement</span></span> | <span data-ttu-id="f8f02-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f8f02-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f02-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8f02-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f02-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8f02-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8f02-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8f02-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f02-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8f02-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8f02-121">Header</span><span class="sxs-lookup"><span data-stu-id="f8f02-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8f02-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f02-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f02-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8f02-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8f02-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f8f02-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8f02-125">**UDM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="f8f02-125">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> <dt>

[<span data-ttu-id="f8f02-126">**UDM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="f8f02-126">**UDM\_SETPOS**</span></span>](udm-setpos.md)
</dt> <dt>

[<span data-ttu-id="f8f02-127">**UDM \_ GETPOS32**</span><span class="sxs-lookup"><span data-stu-id="f8f02-127">**UDM\_GETPOS32**</span></span>](udm-getpos32.md)
</dt> </dl>

 

 





