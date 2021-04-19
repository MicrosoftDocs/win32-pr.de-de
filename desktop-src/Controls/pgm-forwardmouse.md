---
title: PGM_FORWARDMOUSE Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement. Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement WM- \_ MouseMove-Nachrichten an das enthaltene Fenster weiter. Sie können diese Nachricht explizit senden oder das Pager- \_ forwardmouse-Makro verwenden.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Windows-Steuerelemente für PGM_FORWARDMOUSE Meldung
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345312"
---
# <a name="pgm_forwardmouse-message"></a><span data-ttu-id="4ddcb-106">PGM \_ forwardmouse-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4ddcb-106">PGM\_FORWARDMOUSE message</span></span>

<span data-ttu-id="4ddcb-107">Aktiviert oder deaktiviert die Maus Weiterleitung für das Pager-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-107">Enables or disables mouse forwarding for the pager control.</span></span> <span data-ttu-id="4ddcb-108">Wenn die Maus Weiterleitung aktiviert ist, leitet das Pager-Steuerelement [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten an das enthaltene Fenster weiter.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-108">When mouse forwarding is enabled, the pager control forwards [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to the contained window.</span></span> <span data-ttu-id="4ddcb-109">Sie können diese Nachricht explizit senden oder das [**Pager- \_ forwardmouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-109">You can send this message explicitly or use the [**Pager\_ForwardMouse**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ddcb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ddcb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ddcb-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ddcb-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ddcb-112">**Boolescher** Wert, der bestimmt, ob die Maus Weiterleitung aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-112">**BOOL** value that determines if mouse forwarding is enabled or disabled.</span></span> <span data-ttu-id="4ddcb-113">Wenn dieser Wert ungleich 0 (null) ist, wird die Maus Weiterleitung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-113">If this value is nonzero, mouse forwarding is enabled.</span></span> <span data-ttu-id="4ddcb-114">Wenn dieser Wert 0 (null) ist, wird die Maus Weiterleitung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-114">If this value is zero, mouse forwarding is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="4ddcb-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ddcb-115">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4ddcb-116">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-116">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ddcb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ddcb-117">Return value</span></span>

<span data-ttu-id="4ddcb-118">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ddcb-118">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ddcb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ddcb-119">Requirements</span></span>



| <span data-ttu-id="4ddcb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ddcb-120">Requirement</span></span> | <span data-ttu-id="4ddcb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4ddcb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ddcb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ddcb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4ddcb-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ddcb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4ddcb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ddcb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4ddcb-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ddcb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ddcb-126">Header</span><span class="sxs-lookup"><span data-stu-id="4ddcb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ddcb-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ddcb-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

