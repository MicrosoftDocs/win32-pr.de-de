---
title: TVM_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Textfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetTextColor-Makros senden.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Windows-Steuerelemente für TVM_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742000"
---
# <a name="tvm_settextcolor-message"></a><span data-ttu-id="a36f1-105">TVM- \_ SetTextColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="a36f1-105">TVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="a36f1-106">Legt die Textfarbe des-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="a36f1-106">Sets the text color of the control.</span></span> <span data-ttu-id="a36f1-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a36f1-107">You can send this message explicitly or by using the [**TreeView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a36f1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a36f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a36f1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a36f1-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a36f1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a36f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a36f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a36f1-112">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Textfarbe enthält.</span><span class="sxs-lookup"><span data-stu-id="a36f1-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new text color.</span></span> <span data-ttu-id="a36f1-113">Wenn dieses Argument-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="a36f1-113">If this argument is -1, the control will revert to using the system color for the text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36f1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a36f1-114">Return value</span></span>

<span data-ttu-id="a36f1-115">Gibt einen **COLORREF** -Wert zurück, der die vorherige Textfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="a36f1-115">Returns a **COLORREF** value that represents the previous text color.</span></span> <span data-ttu-id="a36f1-116">Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="a36f1-116">If this value is -1, the control was using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="a36f1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a36f1-117">Requirements</span></span>



| <span data-ttu-id="a36f1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a36f1-118">Requirement</span></span> | <span data-ttu-id="a36f1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a36f1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a36f1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a36f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a36f1-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36f1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a36f1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a36f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a36f1-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36f1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a36f1-124">Header</span><span class="sxs-lookup"><span data-stu-id="a36f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a36f1-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a36f1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a36f1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a36f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36f1-127">**TVM \_ gettextcolor**</span><span class="sxs-lookup"><span data-stu-id="a36f1-127">**TVM\_GETTEXTCOLOR**</span></span>](tvm-gettextcolor.md)
</dt> </dl>

 

