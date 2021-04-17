---
title: HDM_GETFOCUSEDITEM Meldung (kommstrg. h)
description: Ruft das Element in einem Header Steuerelement ab, das über den Fokus verfügt. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ getfocuseditem-Makro.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Windows-Steuerelemente für HDM_GETFOCUSEDITEM Meldung
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477586"
---
# <a name="hdm_getfocuseditem-message"></a><span data-ttu-id="2e0d6-105">HDM \_ getfocuseditem-Meldung</span><span class="sxs-lookup"><span data-stu-id="2e0d6-105">HDM\_GETFOCUSEDITEM message</span></span>

<span data-ttu-id="2e0d6-106">Ruft das Element in einem Header Steuerelement ab, das über den Fokus verfügt.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-106">Gets the item in a header control that has the focus.</span></span> <span data-ttu-id="2e0d6-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ getfocuseditem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) -Makro.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-107">Send this message explicitly or by using the [**Header\_GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e0d6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e0d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0d6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e0d6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e0d6-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-110">Not used.</span></span> <span data-ttu-id="2e0d6-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e0d6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e0d6-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e0d6-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-113">Not used.</span></span> <span data-ttu-id="2e0d6-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e0d6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e0d6-115">Return value</span></span>

<span data-ttu-id="2e0d6-116">Gibt den Index des Elements zurück, das den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="2e0d6-116">Returns the index of the item in focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0d6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e0d6-117">Requirements</span></span>



| <span data-ttu-id="2e0d6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e0d6-118">Requirement</span></span> | <span data-ttu-id="2e0d6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2e0d6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0d6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e0d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0d6-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e0d6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e0d6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e0d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0d6-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e0d6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e0d6-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e0d6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e0d6-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e0d6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0d6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e0d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0d6-127">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="2e0d6-127">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





