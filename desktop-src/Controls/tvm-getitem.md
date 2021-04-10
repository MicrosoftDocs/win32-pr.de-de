---
title: TVM_GETITEM Meldung (kommstrg. h)
description: Ruft einige oder alle der Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "GetItem" senden.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Windows-Steuerelemente für TVM_GETITEM Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106574"
---
# <a name="tvm_getitem-message"></a><span data-ttu-id="e2f90-105">TVM- \_ GetItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="e2f90-105">TVM\_GETITEM message</span></span>

<span data-ttu-id="e2f90-106">Ruft einige oder alle der Attribute eines Struktur Ansichts Elements ab.</span><span class="sxs-lookup"><span data-stu-id="e2f90-106">Retrieves some or all of a tree-view item's attributes.</span></span> <span data-ttu-id="e2f90-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) " senden.</span><span class="sxs-lookup"><span data-stu-id="e2f90-107">You can send this message explicitly or by using the [**TreeView\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2f90-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2f90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f90-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2f90-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2f90-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e2f90-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2f90-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2f90-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f90-112">Ein Zeiger auf eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und Informationen über das Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="e2f90-112">Pointer to a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that specifies the information to retrieve and receives information about the item.</span></span> <span data-ttu-id="e2f90-113">Mit [Version 4,71](common-control-versions.md) und höher können Sie stattdessen eine [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2f90-113">With [version 4.71](common-control-versions.md) and later, you can use a [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure instead.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f90-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2f90-114">Return value</span></span>

<span data-ttu-id="e2f90-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e2f90-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f90-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2f90-116">Remarks</span></span>

<span data-ttu-id="e2f90-117">Wenn die Nachricht gesendet wird, identifiziert das **Hitem** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur das Element, über das Informationen abgerufen werden sollen, und der **Mask** -Member gibt die abzurufenden Attribute an.</span><span class="sxs-lookup"><span data-stu-id="e2f90-117">When the message is sent, the **hItem** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure identifies the item to retrieve information about, and the **mask** member specifies the attributes to retrieve.</span></span>

<span data-ttu-id="e2f90-118">Wenn das tvif- \_ textflag im **Mask** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur festgelegt ist, muss der **pszText** -Member auf einen gültigen Puffer zeigen, und das **cchtextmax** -Element muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e2f90-118">If the TVIF\_TEXT flag is set in the **mask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) or [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) structure, the **pszText** member must point to a valid buffer and the **cchTextMax** member must be set to the number of characters in that buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f90-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2f90-119">Requirements</span></span>



| <span data-ttu-id="e2f90-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2f90-120">Requirement</span></span> | <span data-ttu-id="e2f90-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e2f90-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f90-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2f90-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f90-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2f90-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2f90-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2f90-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f90-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2f90-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2f90-126">Header</span><span class="sxs-lookup"><span data-stu-id="e2f90-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f90-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f90-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e2f90-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="e2f90-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e2f90-129">**TVM \_ Getitemw** (Unicode) und **TVM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e2f90-129">**TVM\_GETITEMW** (Unicode) and **TVM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





