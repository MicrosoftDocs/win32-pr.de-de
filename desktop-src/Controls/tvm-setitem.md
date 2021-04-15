---
title: TVM_SETITEM Meldung (kommstrg. h)
description: Mit der TVM \_ SetItem-Meldung werden einige oder alle der Attribute eines Struktur Ansichts Elements festgelegt. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros (TreeView) senden \_ .
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Windows-Steuerelemente für TVM_SETITEM Meldung
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476950"
---
# <a name="tvm_setitem-message"></a><span data-ttu-id="c0d42-105">TVM-nach \_ richten-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c0d42-105">TVM\_SETITEM message</span></span>

<span data-ttu-id="c0d42-106">Mit der **TVM \_ SetItem** -Meldung werden einige oder alle der Attribute eines Struktur Ansichts Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c0d42-106">The **TVM\_SETITEM** message sets some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="c0d42-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ -Makros (TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) ) senden.</span><span class="sxs-lookup"><span data-stu-id="c0d42-107">You can send this message explicitly or by using the [**TreeView\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0d42-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0d42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0d42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d42-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c0d42-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c0d42-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0d42-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d42-112">Zeiger auf eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die neuen Element Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="c0d42-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="c0d42-113">Mit [Version 4,71](common-control-versions.md) und höher können Sie stattdessen eine [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="c0d42-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0d42-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0d42-114">Return value</span></span>

<span data-ttu-id="c0d42-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c0d42-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0d42-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0d42-116">Remarks</span></span>

<span data-ttu-id="c0d42-117">Das **Hitem** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur identifiziert das Element, und der **Mask** -Member gibt an, welche Attribute festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c0d42-117">The **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item, and the **mask** member specifies which attributes to set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0d42-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d42-118">Requirements</span></span>



| <span data-ttu-id="c0d42-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d42-119">Requirement</span></span> | <span data-ttu-id="c0d42-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d42-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d42-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0d42-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0d42-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0d42-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0d42-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0d42-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0d42-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0d42-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0d42-125">Header</span><span class="sxs-lookup"><span data-stu-id="c0d42-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0d42-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d42-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c0d42-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="c0d42-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c0d42-128">**TVM \_** "S" (Unicode) und " **TVM \_** " (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c0d42-128">**TVM\_SETITEMW** (Unicode) and **TVM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





