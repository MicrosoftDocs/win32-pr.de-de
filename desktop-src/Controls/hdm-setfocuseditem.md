---
title: HDM_SETFOCUSEDITEM Meldung (kommstrg. h)
description: Legt den Fokus auf ein angegebenes Element in einem Header Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ setfocuseditem-Makro.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- Windows-Steuerelemente für HDM_SETFOCUSEDITEM Meldung
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105291"
---
# <a name="hdm_setfocuseditem-message"></a><span data-ttu-id="aab4c-105">HDM- \_ setfocuseditem-Meldung</span><span class="sxs-lookup"><span data-stu-id="aab4c-105">HDM\_SETFOCUSEDITEM message</span></span>

<span data-ttu-id="aab4c-106">Legt den Fokus auf ein angegebenes Element in einem Header Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="aab4c-106">Sets the focus to a specified item in a header control.</span></span> <span data-ttu-id="aab4c-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ setfocuseditem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) -Makro.</span><span class="sxs-lookup"><span data-stu-id="aab4c-107">Send this message explicitly or by using the [**Header\_SetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="aab4c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="aab4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab4c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aab4c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aab4c-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="aab4c-110">Not used.</span></span> <span data-ttu-id="aab4c-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="aab4c-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aab4c-112">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aab4c-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab4c-113">Der Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="aab4c-113">The index of item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab4c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aab4c-114">Return value</span></span>

<span data-ttu-id="aab4c-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="aab4c-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab4c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aab4c-116">Requirements</span></span>



| <span data-ttu-id="aab4c-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aab4c-117">Requirement</span></span> | <span data-ttu-id="aab4c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="aab4c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aab4c-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aab4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aab4c-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aab4c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aab4c-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aab4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aab4c-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aab4c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aab4c-123">Header</span><span class="sxs-lookup"><span data-stu-id="aab4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab4c-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab4c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aab4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab4c-126">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="aab4c-126">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





