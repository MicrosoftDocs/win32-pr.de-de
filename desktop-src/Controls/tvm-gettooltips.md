---
title: TVM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das untergeordnete ToolTip-Steuerelement ab, das von einem Strukturansicht-Steuerelement verwendet wird. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ gettooltips-Makros senden.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Windows-Steuerelemente für TVM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475897"
---
# <a name="tvm_gettooltips-message"></a><span data-ttu-id="67e3b-105">TVM \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="67e3b-105">TVM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="67e3b-106">Ruft das Handle für das untergeordnete ToolTip-Steuerelement ab, das von einem Strukturansicht-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="67e3b-106">Retrieves the handle to the child tooltip control used by a tree-view control.</span></span> <span data-ttu-id="67e3b-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="67e3b-107">You can send this message explicitly or by using the [**TreeView\_GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="67e3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="67e3b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="67e3b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="67e3b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="67e3b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="67e3b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="67e3b-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="67e3b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e3b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67e3b-113">Return value</span></span>

<span data-ttu-id="67e3b-114">Gibt das Handle für das untergeordnete QuickInfo-Steuerelement zurück, oder **null** , wenn das Steuerelement keine Quick Infos verwendet.</span><span class="sxs-lookup"><span data-stu-id="67e3b-114">Returns the handle to the child tooltip control, or **NULL** if the control is not using tooltips.</span></span>

## <a name="remarks"></a><span data-ttu-id="67e3b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67e3b-115">Remarks</span></span>

<span data-ttu-id="67e3b-116">Beim Erstellen wird von Strukturansicht-Steuerelementen automatisch ein untergeordnetes QuickInfo-Steuerelement erstellt.</span><span class="sxs-lookup"><span data-stu-id="67e3b-116">When created, tree-view controls automatically create a child tooltip control.</span></span> <span data-ttu-id="67e3b-117">Damit ein Strukturansicht-Steuerelement keine Quick Infos verwendet, erstellen Sie das Steuerelement mit [**dem \_ witooltips**](tree-view-control-window-styles.md) -Stil "TVs".</span><span class="sxs-lookup"><span data-stu-id="67e3b-117">To cause a tree-view control not to use tooltips, create the control with the [**TVS\_NOTOOLTIPS**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="67e3b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67e3b-118">Requirements</span></span>



| <span data-ttu-id="67e3b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67e3b-119">Requirement</span></span> | <span data-ttu-id="67e3b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="67e3b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67e3b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67e3b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="67e3b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e3b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="67e3b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67e3b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="67e3b-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e3b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="67e3b-125">Header</span><span class="sxs-lookup"><span data-stu-id="67e3b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="67e3b-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="67e3b-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e3b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67e3b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e3b-128">**TVM- \_ SetToolTips**</span><span class="sxs-lookup"><span data-stu-id="67e3b-128">**TVM\_SETTOOLTIPS**</span></span>](tvm-settooltips.md)
</dt> </dl>

 

 





