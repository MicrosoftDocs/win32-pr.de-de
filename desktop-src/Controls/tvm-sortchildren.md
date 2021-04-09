---
title: TVM_SORTCHILDREN Meldung (kommstrg. h)
description: Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SortChildren-Makros senden.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Windows-Steuerelemente für TVM_SORTCHILDREN Meldung
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040941"
---
# <a name="tvm_sortchildren-message"></a><span data-ttu-id="ed21e-105">TVM \_ SortChildren-Meldung</span><span class="sxs-lookup"><span data-stu-id="ed21e-105">TVM\_SORTCHILDREN message</span></span>

<span data-ttu-id="ed21e-106">Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ed21e-106">Sorts the child items of the specified parent item in a tree-view control.</span></span> <span data-ttu-id="ed21e-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ed21e-107">You can send this message explicitly or by using the [**TreeView\_SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed21e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed21e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed21e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed21e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed21e-110">Ein Wert, der angibt, ob die Sortierung rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="ed21e-110">Value that specifies whether the sorting is recursive.</span></span> <span data-ttu-id="ed21e-111">Legen Sie " *wParam* " auf " **true** " fest, um alle Ebenen von untergeordneten Elementen unterhalb des übergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="ed21e-111">Set *wParam* to **TRUE** to sort all levels of child items below the parent item.</span></span> <span data-ttu-id="ed21e-112">Andernfalls werden nur die unmittelbar untergeordneten Elemente des übergeordneten Elements sortiert.</span><span class="sxs-lookup"><span data-stu-id="ed21e-112">Otherwise, only the parent's immediate children are sorted.</span></span>

</dd> <dt>

<span data-ttu-id="ed21e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed21e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed21e-114">Handle für das übergeordnete Element, dessen untergeordnete Elemente sortiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ed21e-114">Handle to the parent item whose child items are to be sorted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed21e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed21e-115">Return value</span></span>

<span data-ttu-id="ed21e-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ed21e-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed21e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed21e-117">Remarks</span></span>

<span data-ttu-id="ed21e-118">In dieser Meldung werden die Strukturelemente mithilfe von [**lstrincmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) auf dem Elementnamen alphabetisch sortiert.</span><span class="sxs-lookup"><span data-stu-id="ed21e-118">This message alphabetizes the tree items using [**lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) on the item name.</span></span> <span data-ttu-id="ed21e-119">Mit der [**TVM \_ SortChildren**](tvm-sortchildrencb.md) -Nachricht können Sie das Bestellverhalten anpassen.</span><span class="sxs-lookup"><span data-stu-id="ed21e-119">You can use the [**TVM\_SORTCHILDRENCB**](tvm-sortchildrencb.md) message to customize the ordering behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed21e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed21e-120">Requirements</span></span>



| <span data-ttu-id="ed21e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed21e-121">Requirement</span></span> | <span data-ttu-id="ed21e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ed21e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed21e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed21e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed21e-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed21e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed21e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed21e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed21e-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed21e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed21e-127">Header</span><span class="sxs-lookup"><span data-stu-id="ed21e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed21e-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed21e-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

