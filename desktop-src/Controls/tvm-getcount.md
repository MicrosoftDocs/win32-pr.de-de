---
title: TVM_GETCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetCount-Makros senden.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Windows-Steuerelemente für TVM_GETCOUNT Meldung
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478480"
---
# <a name="tvm_getcount-message"></a><span data-ttu-id="2bb1f-105">TVM \_ GetCount-Meldung</span><span class="sxs-lookup"><span data-stu-id="2bb1f-105">TVM\_GETCOUNT message</span></span>

<span data-ttu-id="2bb1f-106">Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-106">Retrieves a count of the items in a tree-view control.</span></span> <span data-ttu-id="2bb1f-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-107">You can send this message explicitly or by using the [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2bb1f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bb1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bb1f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bb1f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2bb1f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2bb1f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bb1f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2bb1f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bb1f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bb1f-113">Return value</span></span>

<span data-ttu-id="2bb1f-114">Gibt die Anzahl der Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-114">Returns the count of items.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb1f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bb1f-115">Remarks</span></span>

<span data-ttu-id="2bb1f-116">Die von [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) zurückgegebene Knoten Anzahl ist auf ganzzahlige Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-116">The node count returned by [**TreeView\_GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) is limited to integer values.</span></span> <span data-ttu-id="2bb1f-117">Wenn Sie einen Knoten außer 32767 hinzufügen, gibt das Makro einen negativen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-117">If you add a node beyond 32767 the macro returns a negative value.</span></span> <span data-ttu-id="2bb1f-118">Nach dem Hinzufügen von 65536 Knoten wird die Anzahl auf 0 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-118">After adding 65536 nodes the count returns to zero.</span></span> <span data-ttu-id="2bb1f-119">Wenn dies auftritt, wird das Strukturansicht-Steuerelement ohne Scrollleisten leer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2bb1f-119">When this occurs, the tree-view control appears empty with no scrollbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb1f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bb1f-120">Requirements</span></span>



| <span data-ttu-id="2bb1f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bb1f-121">Requirement</span></span> | <span data-ttu-id="2bb1f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2bb1f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb1f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2bb1f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb1f-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb1f-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bb1f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2bb1f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb1f-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2bb1f-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bb1f-127">Header</span><span class="sxs-lookup"><span data-stu-id="2bb1f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bb1f-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb1f-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





