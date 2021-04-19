---
title: TVM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Hintergrundfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetBkColor-Makros senden.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Windows-Steuerelemente für TVM_GETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345324"
---
# <a name="tvm_getbkcolor-message"></a><span data-ttu-id="311ca-105">TVM \_ GetBkColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="311ca-105">TVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="311ca-106">Ruft die aktuelle Hintergrundfarbe des-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="311ca-106">Retrieves the current background color of the control.</span></span> <span data-ttu-id="311ca-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="311ca-107">You can send this message explicitly or by using the [**TreeView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="311ca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="311ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="311ca-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="311ca-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="311ca-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="311ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="311ca-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="311ca-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="311ca-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311ca-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="311ca-113">Return value</span></span>

<span data-ttu-id="311ca-114">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die aktuelle Hintergrundfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="311ca-114">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the current background color.</span></span> <span data-ttu-id="311ca-115">Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="311ca-115">If this value is -1, the control is using the system color for the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="311ca-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="311ca-116">Requirements</span></span>



| <span data-ttu-id="311ca-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="311ca-117">Requirement</span></span> | <span data-ttu-id="311ca-118">Wert</span><span class="sxs-lookup"><span data-stu-id="311ca-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="311ca-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="311ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="311ca-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="311ca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="311ca-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="311ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="311ca-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="311ca-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="311ca-123">Header</span><span class="sxs-lookup"><span data-stu-id="311ca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="311ca-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="311ca-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="311ca-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="311ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311ca-126">**TVM \_ SetBkColor**</span><span class="sxs-lookup"><span data-stu-id="311ca-126">**TVM\_SETBKCOLOR**</span></span>](tvm-setbkcolor.md)
</dt> </dl>

 

