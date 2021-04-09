---
title: TCM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element aus einem Registerkarten-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ DeleteItem-Makros senden.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- Windows-Steuerelemente für TCM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ad4f57b63c154ee98fc48a59ac81bf4fd61ba5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957042"
---
# <a name="tcm_deleteitem-message"></a><span data-ttu-id="de22e-105">TCM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="de22e-105">TCM\_DELETEITEM message</span></span>

<span data-ttu-id="de22e-106">Entfernt ein Element aus einem Registerkarten-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="de22e-106">Removes an item from a tab control.</span></span> <span data-ttu-id="de22e-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="de22e-107">You can send this message explicitly or by using the [**TabCtrl\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="de22e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de22e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de22e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de22e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de22e-110">Der Index des zu löschenden Elements.</span><span class="sxs-lookup"><span data-stu-id="de22e-110">Index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="de22e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de22e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="de22e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="de22e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de22e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de22e-113">Return value</span></span>

<span data-ttu-id="de22e-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="de22e-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de22e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de22e-115">Requirements</span></span>



| <span data-ttu-id="de22e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de22e-116">Requirement</span></span> | <span data-ttu-id="de22e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="de22e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de22e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de22e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de22e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de22e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de22e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de22e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de22e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de22e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de22e-122">Header</span><span class="sxs-lookup"><span data-stu-id="de22e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de22e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de22e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





