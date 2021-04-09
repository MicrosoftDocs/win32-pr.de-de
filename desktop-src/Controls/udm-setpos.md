---
title: UDM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest.
ms.assetid: e7c8b55f-3a4f-47e7-8c7d-e47509f27f1d
keywords:
- Windows-Steuerelemente für UDM_SETPOS Meldung
topic_type:
- apiref
api_name:
- UDM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b409f9e7468e3add89248b61b7b563ac592f0dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104762"
---
# <a name="udm_setpos-message"></a><span data-ttu-id="6b509-104">UDM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6b509-104">UDM\_SETPOS message</span></span>

<span data-ttu-id="6b509-105">Legt die aktuelle Position für ein auf-ab-Steuerelement mit 16-Bit-Genauigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="6b509-105">Sets the current position for an up-down control with 16-bit precision.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b509-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b509-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b509-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b509-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6b509-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6b509-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6b509-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b509-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b509-110">Neue Position für das auf-ab-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6b509-110">New position for the up-down control.</span></span> <span data-ttu-id="6b509-111">Wenn der Parameter außerhalb des angegebenen Bereichs des Steuer Elements liegt, wird *LPARAM* auf den nächstgelegenen gültigen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b509-111">If the parameter is outside the control's specified range, *lParam* will be set to the nearest valid value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b509-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b509-112">Return value</span></span>

<span data-ttu-id="6b509-113">Der Rückgabewert ist die vorherige Position.</span><span class="sxs-lookup"><span data-stu-id="6b509-113">The return value is the previous position.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b509-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b509-114">Remarks</span></span>

<span data-ttu-id="6b509-115">Diese Meldung unterstützt nur 16-Bit-Positionen.</span><span class="sxs-lookup"><span data-stu-id="6b509-115">This message only supports 16-bit positions.</span></span> <span data-ttu-id="6b509-116">Wenn 32-Bit-Werte für ein auf-ab-Steuerelement mit [**UDM- \_ SETRANGE32**](udm-setrange32.md)aktiviert wurden, verwenden Sie [**UDM \_ SETPOS32**](udm-setpos32.md).</span><span class="sxs-lookup"><span data-stu-id="6b509-116">If 32-bit values have been enabled for an up-down control with [**UDM\_SETRANGE32**](udm-setrange32.md), use [**UDM\_SETPOS32**](udm-setpos32.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b509-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b509-117">Requirements</span></span>



| <span data-ttu-id="6b509-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b509-118">Requirement</span></span> | <span data-ttu-id="6b509-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6b509-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b509-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b509-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b509-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b509-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b509-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b509-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b509-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b509-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b509-124">Header</span><span class="sxs-lookup"><span data-stu-id="6b509-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b509-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b509-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b509-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b509-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b509-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6b509-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b509-128">**UDM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="6b509-128">**UDM\_GETRANGE**</span></span>](udm-getrange.md)
</dt> <dt>

[<span data-ttu-id="6b509-129">**UDM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="6b509-129">**UDM\_GETPOS**</span></span>](udm-getpos.md)
</dt> </dl>

 

 





