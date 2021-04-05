---
title: TVM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des TreeView \_ GetExtendedStyle-Makros.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- Windows-Steuerelemente für TVM_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859234"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a><span data-ttu-id="a1e33-105">TVM_GETEXTENDEDSTYLE Meldung (kommstrg. h)</span><span class="sxs-lookup"><span data-stu-id="a1e33-105">TVM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="a1e33-106">Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a1e33-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="a1e33-107">Senden Sie diese Nachricht explizit oder mithilfe des [**TreeView \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) -Makros.</span><span class="sxs-lookup"><span data-stu-id="a1e33-107">Send this message explicitly or by using the [**TreeView\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1e33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1e33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1e33-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a1e33-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a1e33-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a1e33-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1e33-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a1e33-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a1e33-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e33-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1e33-113">Return value</span></span>

<span data-ttu-id="a1e33-114">Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie Unterstruktur [Ansicht-Steuerelement erweiterte Stile](tree-view-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="a1e33-114">Returns the value of extended style.For more information on styles, see [Tree-View Control Extended Styles](tree-view-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e33-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1e33-115">Remarks</span></span>

<span data-ttu-id="a1e33-116">Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1e33-116">The extended styles for a tree-view control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e33-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1e33-117">Requirements</span></span>



| <span data-ttu-id="a1e33-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1e33-118">Requirement</span></span> | <span data-ttu-id="a1e33-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a1e33-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e33-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1e33-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e33-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e33-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1e33-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1e33-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e33-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1e33-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1e33-124">Header</span><span class="sxs-lookup"><span data-stu-id="a1e33-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e33-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e33-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

