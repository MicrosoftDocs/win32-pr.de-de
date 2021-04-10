---
title: TVM_SETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ mapresertmarkcolor-Makros senden.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Windows-Steuerelemente für TVM_SETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104175"
---
# <a name="tvm_setinsertmarkcolor-message"></a><span data-ttu-id="277e5-105">TVM-Meldung "". \_</span><span class="sxs-lookup"><span data-stu-id="277e5-105">TVM\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="277e5-106">Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="277e5-106">Sets the color used to draw the insertion mark for the tree view.</span></span> <span data-ttu-id="277e5-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ mapresertmarkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="277e5-107">You can send this message explicitly or by using the [**TreeView\_SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="277e5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="277e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="277e5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="277e5-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="277e5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="277e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="277e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="277e5-112">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue einfügemarkierungs Farbe enthält.</span><span class="sxs-lookup"><span data-stu-id="277e5-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277e5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="277e5-113">Return value</span></span>

<span data-ttu-id="277e5-114">Gibt einen **COLORREF** -Wert zurück, der die vorherige Einfügemarke enthält.</span><span class="sxs-lookup"><span data-stu-id="277e5-114">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="277e5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="277e5-115">Requirements</span></span>



| <span data-ttu-id="277e5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="277e5-116">Requirement</span></span> | <span data-ttu-id="277e5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="277e5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="277e5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="277e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="277e5-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="277e5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="277e5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="277e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="277e5-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="277e5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="277e5-122">Header</span><span class="sxs-lookup"><span data-stu-id="277e5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="277e5-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="277e5-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277e5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="277e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277e5-125">**TVM \_ getinsertmarkcolor**</span><span class="sxs-lookup"><span data-stu-id="277e5-125">**TVM\_GETINSERTMARKCOLOR**</span></span>](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

