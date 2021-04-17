---
title: TVM_EXPAND Meldung (kommstrg. h)
description: Die TVM \_ Expand Message erweitert oder reduziert die Liste der untergeordneten Elemente, die dem angegebenen übergeordneten Element zugeordnet sind, sofern vorhanden. Sie können diese Nachricht explizit oder mithilfe des TreeView Expand- \_ Makros senden.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Windows-Steuerelemente für TVM_EXPAND Meldung
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478486"
---
# <a name="tvm_expand-message"></a><span data-ttu-id="5c28a-105">TVM \_ Expand Message</span><span class="sxs-lookup"><span data-stu-id="5c28a-105">TVM\_EXPAND message</span></span>

<span data-ttu-id="5c28a-106">Die **TVM \_ Expand** Message erweitert oder reduziert die Liste der untergeordneten Elemente, die dem angegebenen übergeordneten Element zugeordnet sind, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5c28a-106">The **TVM\_EXPAND** message expands or collapses the list of child items associated with the specified parent item, if any.</span></span> <span data-ttu-id="5c28a-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5c28a-107">You can send this message explicitly or by using the [**TreeView\_Expand**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c28a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c28a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c28a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c28a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c28a-110">Aktionsflag.</span><span class="sxs-lookup"><span data-stu-id="5c28a-110">Action flag.</span></span> <span data-ttu-id="5c28a-111">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="5c28a-111">This parameter can be one or more of the following values:</span></span>



| <span data-ttu-id="5c28a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5c28a-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="5c28a-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5c28a-113">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <span data-ttu-id="5c28a-114"><dt>**TVE \_ zuklappen**</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-114"><dt>**TVE\_COLLAPSE**</dt></span></span> </dl>                | <span data-ttu-id="5c28a-115">Reduziert die Liste.</span><span class="sxs-lookup"><span data-stu-id="5c28a-115">Collapses the list.</span></span> <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <span data-ttu-id="5c28a-116"><dt>**TVE- \_ redusereset**</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-116"><dt>**TVE\_COLLAPSERESET**</dt></span></span> </dl> | <span data-ttu-id="5c28a-117">Reduziert die Liste und entfernt die untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="5c28a-117">Collapses the list and removes the child items.</span></span> <span data-ttu-id="5c28a-118">Das [**Tvis \_ expandebug**](tree-view-control-item-states.md) State-Flag wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5c28a-118">The [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is reset.</span></span> <span data-ttu-id="5c28a-119">Dieses Flag muss mit dem "TVE Collapse"-Flag verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="5c28a-119">This flag must be used with the TVE\_COLLAPSE flag.</span></span><br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <span data-ttu-id="5c28a-120"><dt>**TVE \_ erweitern**</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-120"><dt>**TVE\_EXPAND**</dt></span></span> </dl>                      | <span data-ttu-id="5c28a-121">Erweitert die Liste.</span><span class="sxs-lookup"><span data-stu-id="5c28a-121">Expands the list.</span></span><br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <span data-ttu-id="5c28a-122"><dt>**TVE \_ expandpartial**</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-122"><dt>**TVE\_EXPANDPARTIAL**</dt></span></span> </dl> | <span data-ttu-id="5c28a-123">[Version 4,70](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5c28a-123">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="5c28a-124">Erweitert die Liste teilweise.</span><span class="sxs-lookup"><span data-stu-id="5c28a-124">Partially expands the list.</span></span> <span data-ttu-id="5c28a-125">In diesem Zustand werden die untergeordneten Elemente sichtbar, und das Pluszeichen (+) des übergeordneten Elements, das angibt, dass es erweitert werden kann, wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c28a-125">In this state the child items are visible and the parent item's plus sign (+), indicating that it can be expanded, is displayed.</span></span> <span data-ttu-id="5c28a-126">Dieses Flag muss in Kombination mit dem "TVE expand"-Flag verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="5c28a-126">This flag must be used in combination with the TVE\_EXPAND flag.</span></span><br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <span data-ttu-id="5c28a-127"><dt>**TVE \_ Umschalten**</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-127"><dt>**TVE\_TOGGLE**</dt></span></span> </dl>                      | <span data-ttu-id="5c28a-128">Reduziert die Liste, wenn Sie erweitert wird, oder erweitert Sie, wenn Sie reduziert ist.</span><span class="sxs-lookup"><span data-stu-id="5c28a-128">Collapses the list if it is expanded or expands it if it is collapsed.</span></span><br/>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="5c28a-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c28a-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c28a-130">Handle für das übergeordnete Element, das erweitert oder reduziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c28a-130">Handle to the parent item to expand or collapse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c28a-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c28a-131">Return value</span></span>

<span data-ttu-id="5c28a-132">Gibt einen Wert ungleich 0 (null) zurück, wenn der Vorgang erfolgreich war, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="5c28a-132">Returns nonzero if the operation was successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c28a-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c28a-133">Remarks</span></span>

<span data-ttu-id="5c28a-134">Das Erweitern eines Knotens, der bereits erweitert ist, gilt als erfolgreicher Vorgang, und [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) gibt einen Wert ungleich 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5c28a-134">Expanding a node that is already expanded is considered a successful operation and [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns a nonzero value.</span></span> <span data-ttu-id="5c28a-135">Beim Reduzieren eines Knotens wird 0 zurückgegeben, wenn der Knoten bereits reduziert ist. Andernfalls wird ein Wert ungleich NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5c28a-135">Collapsing a node returns zero if the node is already collapsed; otherwise it returns nonzero.</span></span> <span data-ttu-id="5c28a-136">Der Versuch, einen Knoten zu erweitern oder zu reduzieren, der keine untergeordneten Elemente hat, wird als Fehler betrachtet, und **SendMessage** gibt NULL zurück</span><span class="sxs-lookup"><span data-stu-id="5c28a-136">Attempting to expand or collapse a node that has no children is considered a failure and **SendMessage** returns zero.</span></span>

<span data-ttu-id="5c28a-137">Wenn ein Element erstmalig durch eine **TVM \_** -Erweiterungs Meldung erweitert wird, generiert die Aktion [TVN \_ itemexpandeing](tvn-itemexpanding.md) und [TVN \_ itemexpanded](tvn-itemexpanded.md) -Benachrichtigungs Codes, und das [**Tvis \_**](tree-view-control-item-states.md) -Statusflag des Elements wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c28a-137">When an item is first expanded by a **TVM\_EXPAND** message, the action generates [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes and the item's [**TVIS\_EXPANDEDONCE**](tree-view-control-item-states.md) state flag is set.</span></span> <span data-ttu-id="5c28a-138">Solange dieses Statusflag festgelegt bleibt, generieren nachfolgende **TVM \_ Expand** Messages keine TVN \_ itemexpandor-und TVN \_ itemexpanded-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="5c28a-138">As long as this state flag remains set, subsequent **TVM\_EXPAND** messages do not generate TVN\_ITEMEXPANDING or TVN\_ITEMEXPANDED notifications.</span></span> <span data-ttu-id="5c28a-139">Um das **Tvis \_ expandedonce** State-Flag zurückzusetzen, müssen Sie eine **TVM- \_** Erweiterungs Meldung mit den \_ festgelegten Flags "TVE Collapse" und "TVE \_ redusereset" senden.</span><span class="sxs-lookup"><span data-stu-id="5c28a-139">To reset the **TVIS\_EXPANDEDONCE** state flag, you must send a **TVM\_EXPAND** message with the TVE\_COLLAPSE and TVE\_COLLAPSERESET flags set.</span></span> <span data-ttu-id="5c28a-140">Der Versuch, **Tvis \_ expandedonce** explizit festzulegen, führt zu unvorhersehbarem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="5c28a-140">Attempting to explicitly set **TVIS\_EXPANDEDONCE** will result in unpredictable behavior.</span></span>

<span data-ttu-id="5c28a-141">Der Erweiterungs Vorgang kann fehlschlagen, wenn der Besitzer des TreeView-Steuer Elements den Vorgang als Reaktion auf eine [TVN \_ itemexpandeing](tvn-itemexpanding.md) -Benachrichtigung ablehnt.</span><span class="sxs-lookup"><span data-stu-id="5c28a-141">The expand operation may fail if the owner of the treeview control denies the operation in response to a [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c28a-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c28a-142">Requirements</span></span>



| <span data-ttu-id="5c28a-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c28a-143">Requirement</span></span> | <span data-ttu-id="5c28a-144">Wert</span><span class="sxs-lookup"><span data-stu-id="5c28a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c28a-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c28a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5c28a-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c28a-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c28a-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c28a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5c28a-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c28a-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c28a-149">Header</span><span class="sxs-lookup"><span data-stu-id="5c28a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c28a-150"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c28a-150"><dt>Commctrl.h</dt></span></span> </dl> |



 

