---
title: TVM_SELECTITEM Meldung (kommstrg. h)
description: Wählt das angegebene Struktur Ansichts Element aus, führt einen Bildlauf durch das Element durch oder zeichnet das Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Windows-Steuerelemente für TVM_SELECTITEM Meldung
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858730"
---
# <a name="tvm_selectitem-message"></a><span data-ttu-id="c3d4f-104">TVM \_ SelectItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="c3d4f-104">TVM\_SELECTITEM message</span></span>

<span data-ttu-id="c3d4f-105">Wählt das angegebene Struktur Ansichts Element aus, führt einen Bildlauf durch das Element durch oder zeichnet das Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-105">Selects the specified tree-view item, scrolls the item into view, or redraws the item in the style used to indicate the target of a drag-and-drop operation.</span></span> <span data-ttu-id="c3d4f-106">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)-, [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)-oder [**TreeView \_ selectdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-106">You can send this message explicitly or by using the [**TreeView\_Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem), or [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3d4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3d4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d4f-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3d4f-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d4f-109">Aktionsflag.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-109">Action flag.</span></span> <span data-ttu-id="c3d4f-110">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c3d4f-110">This parameter can be one of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3d4f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="c3d4f-111">Value</span></span></th>
<th><span data-ttu-id="c3d4f-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c3d4f-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <span data-ttu-id="c3d4f-113"><dt><strong>TVGN_CARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c3d4f-113"><dt><strong>TVGN_CARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c3d4f-114">Legt die Auswahl auf das angegebene Element fest.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-114">Sets the selection to the specified item.</span></span> <span data-ttu-id="c3d4f-115">Das übergeordnete Fenster des Strukturansicht-Steuer Elements empfängt die <a href="tvn-selchanging.md">TVN_SELCHANGING</a> -und <a href="tvn-selchanged.md">TVN_SELCHANGED</a> -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-115">The tree-view control's parent window receives the <a href="tvn-selchanging.md">TVN_SELCHANGING</a> and <a href="tvn-selchanged.md">TVN_SELCHANGED</a> notification codes.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <span data-ttu-id="c3d4f-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c3d4f-116"><dt><strong>TVGN_DROPHILITE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c3d4f-117">Zeichnet das angegebene Element im Stil neu, mit dem das Ziel eines Drag & Drop-Vorgangs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-117">Redraws the specified item in the style used to indicate the target of a drag-and-drop operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <span data-ttu-id="c3d4f-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c3d4f-118"><dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c3d4f-119">Stellt sicher, dass das angegebene Element sichtbar ist, und zeigt es, wenn möglich, oben im Fenster des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-119">Ensures that the specified item is visible, and, if possible, displays it at the top of the control's window.</span></span> <span data-ttu-id="c3d4f-120">Strukturansicht-Steuerelemente zeigen so viele Elemente an, wie Sie in das Fenster passen.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-120">Tree-view controls display as many items as will fit in the window.</span></span> <span data-ttu-id="c3d4f-121">Wenn sich das angegebene Element am unteren Rand der Hierarchie der Elemente des Steuer Elements befindet, wird es möglicherweise nicht zum ersten sichtbaren Element, abhängig von der Anzahl der Elemente, die in das Fenster passen.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-121">If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <span data-ttu-id="c3d4f-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c3d4f-122"><dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c3d4f-123">Wenn ein einzelnes Element ausgewählt ist, wird von sichergestellt, dass die untergeordneten Elemente dieses Elements nicht von der TreeView-Ansicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-123">When a single item is selected, ensures that the treeview does not expand the children of that item.</span></span> <span data-ttu-id="c3d4f-124">Dieser Wert ist nur gültig, wenn er mit dem TVGN_CARET-Flag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-124">This is valid only if used with the TVGN_CARET flag.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c3d4f-125">Um dieses Flag zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-125">To use this flag, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c3d4f-126">Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-126">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="c3d4f-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3d4f-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3d4f-128">Handle für ein Element.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-128">Handle to an item.</span></span> <span data-ttu-id="c3d4f-129">Wenn *LPARAM* den Wert **null** hat, wird für das Steuerelement festgelegt, dass kein Element ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-129">If *lParam* is **NULL**, the control is set to have no selected item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d4f-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3d4f-130">Return value</span></span>

<span data-ttu-id="c3d4f-131">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c3d4f-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d4f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3d4f-132">Remarks</span></span>

<span data-ttu-id="c3d4f-133">Wenn das angegebene Element das untergeordnete Element eines reduzierten übergeordneten Elements ist, wird die Liste der untergeordneten Elemente des übergeordneten Elements erweitert, um das angegebene Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-133">If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item.</span></span> <span data-ttu-id="c3d4f-134">In diesem Fall empfängt das übergeordnete Fenster des Steuer Elements die [TVN \_ itemexpandeing](tvn-itemexpanding.md) -und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="c3d4f-134">In this case, the control's parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

<span data-ttu-id="c3d4f-135">Die Verwendung des [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) -Makros entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* -Wert, der auf den Tvgn-Caretzeichen Wert festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c3d4f-135">Using the [**TreeView\_SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_CARET value.</span></span> <span data-ttu-id="c3d4f-136">Das Verwenden des [**TreeView \_ selectdroptarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) -Makros entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* -Wert, der auf den Wert der Tvgn-drophitefunktion festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c3d4f-136">Using the [**TreeView\_SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) macro is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_DROPHILITE value.</span></span> <span data-ttu-id="c3d4f-137">Die Verwendung von [**TreeView \_ selectsetfirstvisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) entspricht dem Senden der **TVM \_ SelectItem** -Nachricht mit *wParam* , die auf den Wert der Tvgn firstvisible festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="c3d4f-137">Using [**TreeView\_SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) is equivalent to sending the **TVM\_SELECTITEM** message with *wParam* set to the TVGN\_FIRSTVISIBLE value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3d4f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3d4f-138">Requirements</span></span>



| <span data-ttu-id="c3d4f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3d4f-139">Requirement</span></span> | <span data-ttu-id="c3d4f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c3d4f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d4f-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3d4f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d4f-142">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3d4f-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3d4f-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3d4f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d4f-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3d4f-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3d4f-145">Header</span><span class="sxs-lookup"><span data-stu-id="c3d4f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3d4f-146"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d4f-146"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





