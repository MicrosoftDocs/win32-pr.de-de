---
title: TVM_SETINSERTMARK Meldung (kommstrg. h)
description: Legt die Einfügemarke in einem Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ mapresertmark-Makros senden.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Windows-Steuerelemente für TVM_SETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858998"
---
# <a name="tvm_setinsertmark-message"></a><span data-ttu-id="65433-105">TVM- \_ Nachricht "tmark"</span><span class="sxs-lookup"><span data-stu-id="65433-105">TVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="65433-106">Legt die Einfügemarke in einem Strukturansicht-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="65433-106">Sets the insertion mark in a tree-view control.</span></span> <span data-ttu-id="65433-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ mapresertmark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="65433-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="65433-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="65433-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65433-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65433-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65433-110">**Boolescher** Wert, der angibt, ob die Einfügemarke vor oder nach dem angegebenen Element eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="65433-110">**BOOL** value that specifies if the insertion mark is placed before or after the specified item.</span></span> <span data-ttu-id="65433-111">Wenn dieses Argument ungleich 0 (null) ist, wird die Einfügemarke hinter dem Element platziert.</span><span class="sxs-lookup"><span data-stu-id="65433-111">If this argument is nonzero, the insertion mark will be placed after the item.</span></span> <span data-ttu-id="65433-112">Wenn dieses Argument 0 (null) ist, wird die Einfügemarke vor dem Element platziert.</span><span class="sxs-lookup"><span data-stu-id="65433-112">If this argument is zero, the insertion mark will be placed before the item.</span></span>

</dd> <dt>

<span data-ttu-id="65433-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65433-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65433-114">**HTREEITEM** , das angibt, an welchem Punkt die Einfügemarke platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="65433-114">**HTREEITEM** that specifies at which item the insertion mark will be placed.</span></span> <span data-ttu-id="65433-115">Wenn dieses Argument **null** ist, wird die Einfügemarke entfernt.</span><span class="sxs-lookup"><span data-stu-id="65433-115">If this argument is **NULL**, the insertion mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65433-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65433-116">Return value</span></span>

<span data-ttu-id="65433-117">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="65433-117">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65433-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65433-118">Remarks</span></span>

<span data-ttu-id="65433-119">In einigen Fällen kann die Einfügemarke an zwei Stellen angezeigt werden, nachdem ein Knoten erweitert wurde.</span><span class="sxs-lookup"><span data-stu-id="65433-119">In some circumstances, the insert mark can appear in two places after a node is expanded.</span></span> <span data-ttu-id="65433-120">Wenn Sie Einfügezeichen verwenden, wird empfohlen, nach dem Erweitern eines Knotens eine Aktualisierung des Steuer Elements zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="65433-120">If you are using insertion marks, it is recommended that you force a refresh of the control after expanding a node.</span></span>

## <a name="requirements"></a><span data-ttu-id="65433-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65433-121">Requirements</span></span>



| <span data-ttu-id="65433-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65433-122">Requirement</span></span> | <span data-ttu-id="65433-123">Wert</span><span class="sxs-lookup"><span data-stu-id="65433-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65433-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65433-124">Minimum supported client</span></span><br/> | <span data-ttu-id="65433-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65433-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65433-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65433-126">Minimum supported server</span></span><br/> | <span data-ttu-id="65433-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65433-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65433-128">Header</span><span class="sxs-lookup"><span data-stu-id="65433-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="65433-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="65433-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





