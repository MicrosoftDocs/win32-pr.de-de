---
title: EM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft den erweiterten Stil für ein Bearbeitungs Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ Makros GetExtendedStyle bearbeiten.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Windows-Steuerelemente für EM_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477922"
---
# <a name="em_getextendedstyle-message-commctrlh"></a><span data-ttu-id="d7dd8-105">EM_GETEXTENDEDSTYLE Meldung (kommstrg. h)</span><span class="sxs-lookup"><span data-stu-id="d7dd8-105">EM_GETEXTENDEDSTYLE message (Commctrl.h)</span></span>

<span data-ttu-id="d7dd8-106">Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d7dd8-106">Retrieves the extended style for a tree-view control.</span></span> <span data-ttu-id="d7dd8-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Makros \_ GetExtendedStyle bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="d7dd8-107">Send this message explicitly or by using the [**Edit\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7dd8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7dd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7dd8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7dd8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d7dd8-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d7dd8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d7dd8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7dd8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d7dd8-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d7dd8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7dd8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7dd8-113">Return value</span></span>

<span data-ttu-id="d7dd8-114">Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="d7dd8-114">Returns the value of extended style.For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7dd8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7dd8-115">Remarks</span></span>

<span data-ttu-id="d7dd8-116">Die erweiterten Stile für ein Bearbeitungs Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder der Funktion " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7dd8-116">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7dd8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7dd8-117">Requirements</span></span>



| <span data-ttu-id="d7dd8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7dd8-118">Requirement</span></span> | <span data-ttu-id="d7dd8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d7dd8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7dd8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7dd8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7dd8-121">Windows 10, Version 1809, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7dd8-121">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7dd8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7dd8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7dd8-123">Nur Windows Server 2019 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7dd8-123">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7dd8-124">Header</span><span class="sxs-lookup"><span data-stu-id="d7dd8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7dd8-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7dd8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

