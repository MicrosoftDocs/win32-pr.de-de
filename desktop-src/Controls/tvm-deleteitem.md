---
title: TVM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ DeleteItem-Makros senden.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Windows-Steuerelemente für TVM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476953"
---
# <a name="tvm_deleteitem-message"></a><span data-ttu-id="0983f-105">TVM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="0983f-105">TVM\_DELETEITEM message</span></span>

<span data-ttu-id="0983f-106">Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0983f-106">Removes an item and all its children from a tree-view control.</span></span> <span data-ttu-id="0983f-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="0983f-107">You can send this message explicitly or by using the [**TreeView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0983f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0983f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0983f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0983f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0983f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0983f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0983f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0983f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0983f-112">**HTREEITEM** -Handle für das Element, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="0983f-112">**HTREEITEM** handle to the item to delete.</span></span> <span data-ttu-id="0983f-113">Wenn *LPARAM* auf TVI \_ root oder auf **null** festgelegt ist, werden alle Elemente gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0983f-113">If *lParam* is set to TVI\_ROOT or to **NULL**, all items are deleted.</span></span> <span data-ttu-id="0983f-114">Sie können auch das [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) -Makro verwenden, um alle Elemente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0983f-114">You can also use the [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) macro to delete all items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0983f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0983f-115">Return value</span></span>

<span data-ttu-id="0983f-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0983f-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0983f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0983f-117">Remarks</span></span>

<span data-ttu-id="0983f-118">Es ist nicht sicher, Elemente als Reaktion auf eine Benachrichtigung zu löschen, wie z. [b. TVN \_ selchanging](tvn-selchanging.md).</span><span class="sxs-lookup"><span data-stu-id="0983f-118">It is not safe to delete items in response to a notification such as [TVN\_SELCHANGING](tvn-selchanging.md).</span></span>

<span data-ttu-id="0983f-119">Wenn ein Element gelöscht wird, ist das zugehörige Handle ungültig und kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0983f-119">Once an item is deleted, its handle is invalid and cannot be used.</span></span>

<span data-ttu-id="0983f-120">Das übergeordnete Fenster empfängt einen [TVN \_ DeleteItem](tvn-deleteitem.md) -Benachrichtigungs Code, wenn jedes Element entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0983f-120">The parent window receives a [TVN\_DELETEITEM](tvn-deleteitem.md) notification code when each item is removed.</span></span>

<span data-ttu-id="0983f-121">Wenn die Element Bezeichnung bearbeitet wird, wird der Bearbeitungsvorgang abgebrochen, und das übergeordnete Fenster empfängt den [TVN \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="0983f-121">If the item label is being edited, the edit operation is canceled and the parent window receives the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

<span data-ttu-id="0983f-122">Wenn Sie alle Elemente in einem Strukturansicht-Steuerelement mit dem " [**TVs"- \_ NoScroll**](tree-view-control-window-styles.md) -Stil löschen, werden die Elemente, die später hinzugefügt werden, möglicherweise nicht</span><span class="sxs-lookup"><span data-stu-id="0983f-122">If you delete all items in a tree-view control that has the [**TVS\_NOSCROLL**](tree-view-control-window-styles.md) style, items subsequently added may not display properly.</span></span> <span data-ttu-id="0983f-123">Weitere Informationen finden Sie unter [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span><span class="sxs-lookup"><span data-stu-id="0983f-123">For more information, see [**TreeView\_DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).</span></span>

## <a name="requirements"></a><span data-ttu-id="0983f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0983f-124">Requirements</span></span>



| <span data-ttu-id="0983f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0983f-125">Requirement</span></span> | <span data-ttu-id="0983f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0983f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0983f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0983f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0983f-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0983f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0983f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0983f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0983f-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0983f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0983f-131">Header</span><span class="sxs-lookup"><span data-stu-id="0983f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0983f-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0983f-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





