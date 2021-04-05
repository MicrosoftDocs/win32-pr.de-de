---
title: TVM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetBkColor-Makros senden.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Windows-Steuerelemente für TVM_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858999"
---
# <a name="tvm_setbkcolor-message"></a><span data-ttu-id="2e25f-105">TVM- \_ SetBkColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="2e25f-105">TVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="2e25f-106">Legt die Hintergrundfarbe des-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="2e25f-106">Sets the background color of the control.</span></span> <span data-ttu-id="2e25f-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2e25f-107">You can send this message explicitly or by using the [**TreeView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e25f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e25f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e25f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e25f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e25f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e25f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e25f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e25f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e25f-112">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Hintergrundfarbe enthält.</span><span class="sxs-lookup"><span data-stu-id="2e25f-112">[**COLORREF**](/windows/desktop/gdi/colorref) value that contains the new background color.</span></span> <span data-ttu-id="2e25f-113">Wenn dieser Wert-1 ist, wird das Steuerelement wieder auf die System Farbe für die Hintergrundfarbe zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-113">If this value is -1, the control will revert to using the system color for the background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e25f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e25f-114">Return value</span></span>

<span data-ttu-id="2e25f-115">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Hintergrundfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e25f-115">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous background color.</span></span> <span data-ttu-id="2e25f-116">Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="2e25f-116">If this value is -1, the control was using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e25f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e25f-117">Requirements</span></span>



| <span data-ttu-id="2e25f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e25f-118">Requirement</span></span> | <span data-ttu-id="2e25f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2e25f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e25f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e25f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2e25f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e25f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e25f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e25f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2e25f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e25f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e25f-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e25f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e25f-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e25f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e25f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e25f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e25f-127">**TVM \_ GetBkColor**</span><span class="sxs-lookup"><span data-stu-id="2e25f-127">**TVM\_GETBKCOLOR**</span></span>](tvm-getbkcolor.md)
</dt> </dl>

 

