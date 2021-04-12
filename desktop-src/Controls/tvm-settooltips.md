---
title: TVM_SETTOOLTIPS Meldung (kommstrg. h)
description: Legt das untergeordnete ToolTip-Steuerelement eines Strukturansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros SetToolTips senden.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Windows-Steuerelemente für TVM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103623"
---
# <a name="tvm_settooltips-message"></a><span data-ttu-id="7a76b-105">TVM- \_ SetToolTips-Meldung</span><span class="sxs-lookup"><span data-stu-id="7a76b-105">TVM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="7a76b-106">Legt das untergeordnete ToolTip-Steuerelement eines Strukturansicht-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="7a76b-106">Sets a tree-view control's child tooltip control.</span></span> <span data-ttu-id="7a76b-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) senden.</span><span class="sxs-lookup"><span data-stu-id="7a76b-107">You can send this message explicitly or by using the [**TreeView\_SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a76b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a76b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a76b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a76b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a76b-110">Handle für ein QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7a76b-110">Handle to a tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="7a76b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a76b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7a76b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7a76b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a76b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a76b-113">Return value</span></span>

<span data-ttu-id="7a76b-114">Gibt das Handle für das QuickInfo-Steuerelement zurück, das zuvor für das Strukturansicht-Steuerelement festgelegt wurde, oder **null** , wenn keine Quick Infos verwendet wurden</span><span class="sxs-lookup"><span data-stu-id="7a76b-114">Returns the handle to tooltip control previously set for the tree-view control, or **NULL** if tooltips were not previously used.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a76b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a76b-115">Remarks</span></span>

<span data-ttu-id="7a76b-116">Beim Erstellen wird von Strukturansicht-Steuerelementen automatisch ein untergeordnetes QuickInfo-Steuerelement erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a76b-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="7a76b-117">Um zu verhindern, dass ein Strukturansicht-Steuerelement Quick Infos verwendet, erstellen Sie das Steuerelement mit dem [**\_ witooltips**](tree-view-control-window-styles.md) -Stil "TVs".</span><span class="sxs-lookup"><span data-stu-id="7a76b-117">To prevent a tree-view control from using tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a76b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a76b-118">Requirements</span></span>



| <span data-ttu-id="7a76b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a76b-119">Requirement</span></span> | <span data-ttu-id="7a76b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7a76b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a76b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a76b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a76b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a76b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a76b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a76b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a76b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7a76b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a76b-125">Header</span><span class="sxs-lookup"><span data-stu-id="7a76b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a76b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a76b-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a76b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a76b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a76b-128">**TVM \_ gettooltips**</span><span class="sxs-lookup"><span data-stu-id="7a76b-128">**TVM\_GETTOOLTIPS**</span></span>](tvm-gettooltips.md)
</dt> </dl>

 

 





