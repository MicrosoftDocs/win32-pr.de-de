---
title: TVM_GETTEXTCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Textfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ gettextcolor-Makros senden.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Windows-Steuerelemente für TVM_GETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040351"
---
# <a name="tvm_gettextcolor-message"></a><span data-ttu-id="7b1c0-105">TVM \_ gettextcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="7b1c0-105">TVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="7b1c0-106">Ruft die aktuelle Textfarbe des-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-106">Retrieves the current text color of the control.</span></span> <span data-ttu-id="7b1c0-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ gettextcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-107">You can send this message explicitly or by using the [**TreeView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7b1c0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b1c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b1c0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7b1c0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7b1c0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7b1c0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7b1c0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7b1c0-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b1c0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b1c0-113">Return value</span></span>

<span data-ttu-id="7b1c0-114">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die aktuelle Textfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current text color.</span></span> <span data-ttu-id="7b1c0-115">Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.</span><span class="sxs-lookup"><span data-stu-id="7b1c0-115">If this value is -1, the control is using the system color for the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b1c0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b1c0-116">Requirements</span></span>



| <span data-ttu-id="7b1c0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b1c0-117">Requirement</span></span> | <span data-ttu-id="7b1c0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7b1c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1c0-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b1c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b1c0-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b1c0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7b1c0-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b1c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b1c0-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b1c0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7b1c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="7b1c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b1c0-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b1c0-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b1c0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b1c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1c0-126">**TVM \_ SetTextColor**</span><span class="sxs-lookup"><span data-stu-id="7b1c0-126">**TVM\_SETTEXTCOLOR**</span></span>](tvm-settextcolor.md)
</dt> </dl>

 

