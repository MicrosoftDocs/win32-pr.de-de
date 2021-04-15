---
title: UDM_GETACCEL Meldung (kommstrg. h)
description: Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- Windows-Steuerelemente für UDM_GETACCEL Meldung
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475735"
---
# <a name="udm_getaccel-message"></a><span data-ttu-id="218e2-104">UDM \_ GetAccel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="218e2-104">UDM\_GETACCEL message</span></span>

<span data-ttu-id="218e2-105">Ruft Beschleunigungs Informationen für ein auf-ab-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="218e2-105">Retrieves acceleration information for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="218e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="218e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="218e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="218e2-108">Anzahl von Elementen im Array, die von *LPARAM* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="218e2-108">Number of elements in the array specified by *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="218e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="218e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="218e2-110">Zeiger auf ein Array von [**udaccel**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) -Strukturen, die Beschleunigungs Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="218e2-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that receive acceleration information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218e2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="218e2-111">Return value</span></span>

<span data-ttu-id="218e2-112">Der Rückgabewert ist die Anzahl von Accelerators, die derzeit für das Steuerelement festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="218e2-112">The return value is the number of accelerators currently set for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="218e2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="218e2-113">Requirements</span></span>



| <span data-ttu-id="218e2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="218e2-114">Requirement</span></span> | <span data-ttu-id="218e2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="218e2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="218e2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="218e2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="218e2-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="218e2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="218e2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="218e2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="218e2-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="218e2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="218e2-120">Header</span><span class="sxs-lookup"><span data-stu-id="218e2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="218e2-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="218e2-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="218e2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="218e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218e2-123">**UDM- \_ SetAccel**</span><span class="sxs-lookup"><span data-stu-id="218e2-123">**UDM\_SETACCEL**</span></span>](udm-setaccel.md)
</dt> </dl>

 

 





