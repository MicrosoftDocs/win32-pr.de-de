---
title: TVM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Strukturansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ InsertItem-Makros senden.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Windows-Steuerelemente für TVM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858752"
---
# <a name="tvm_insertitem-message"></a><span data-ttu-id="20cb8-105">TVM \_ InsertItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="20cb8-105">TVM\_INSERTITEM message</span></span>

<span data-ttu-id="20cb8-106">Fügt ein neues Element in ein Strukturansicht-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="20cb8-106">Inserts a new item in a tree-view control.</span></span> <span data-ttu-id="20cb8-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="20cb8-107">You can send this message explicitly or by using the [**TreeView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="20cb8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="20cb8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20cb8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="20cb8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="20cb8-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="20cb8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="20cb8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="20cb8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="20cb8-112">Ein Zeiger auf eine [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur, die die Attribute des Struktur Ansichts Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="20cb8-112">Pointer to a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure that specifies the attributes of the tree-view item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20cb8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20cb8-113">Return value</span></span>

<span data-ttu-id="20cb8-114">Gibt das **HTREEITEM** -Handle für das neue Element zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="20cb8-114">Returns the **HTREEITEM** handle to the new item if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="20cb8-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20cb8-115">Requirements</span></span>



| <span data-ttu-id="20cb8-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20cb8-116">Requirement</span></span> | <span data-ttu-id="20cb8-117">Wert</span><span class="sxs-lookup"><span data-stu-id="20cb8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20cb8-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20cb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20cb8-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20cb8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="20cb8-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20cb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20cb8-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20cb8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="20cb8-122">Header</span><span class="sxs-lookup"><span data-stu-id="20cb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20cb8-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="20cb8-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="20cb8-124">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="20cb8-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20cb8-125">**TVM \_ Insertitemw** (Unicode) und **TVM \_ insertitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20cb8-125">**TVM\_INSERTITEMW** (Unicode) and **TVM\_INSERTITEMA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="20cb8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20cb8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cb8-127">TVN \_ endlabeledit</span><span class="sxs-lookup"><span data-stu-id="20cb8-127">TVN\_ENDLABELEDIT</span></span>](tvn-endlabeledit.md)
</dt> </dl>

 

 





