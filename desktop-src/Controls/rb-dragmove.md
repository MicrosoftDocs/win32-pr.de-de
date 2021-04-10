---
title: RB_DRAGMOVE Meldung (kommstrg. h)
description: Aktualisiert die Zieh Position im Grund leisten-Steuerelement nach einer vorherigen RB \_ BeginDrag-Nachricht.
ms.assetid: 0d2ce7fe-4172-45d9-932b-50f3e4cf2d8e
keywords:
- Windows-Steuerelemente für RB_DRAGMOVE Meldung
topic_type:
- apiref
api_name:
- RB_DRAGMOVE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8657d8f8f73c798f934262804dda83b359b0c0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956803"
---
# <a name="rb_dragmove-message"></a><span data-ttu-id="6834b-104">RB \_ DragMove-Meldung</span><span class="sxs-lookup"><span data-stu-id="6834b-104">RB\_DRAGMOVE message</span></span>

<span data-ttu-id="6834b-105">Aktualisiert die Zieh Position im Grund leisten-Steuerelement nach einer vorherigen [**RB \_ BeginDrag**](rb-begindrag.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6834b-105">Updates the drag position in the rebar control after a previous [**RB\_BEGINDRAG**](rb-begindrag.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="6834b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6834b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6834b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6834b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6834b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6834b-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6834b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6834b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6834b-110">**DWORD** -Wert, der die neuen Maus Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="6834b-110">**DWORD** value that contains the new mouse coordinates.</span></span> <span data-ttu-id="6834b-111">Die horizontale Koordinate ist im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthalten, und die vertikale Koordinate ist im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthalten.</span><span class="sxs-lookup"><span data-stu-id="6834b-111">The horizontal coordinate is contained in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the vertical coordinate is contained in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="6834b-112">Wenn Sie (DWORD)-1 übergeben, verwendet das Grund leisten-Steuerelement die Position des Mauszeigers, wenn der Thread des Steuer Elements das letzte Mal den Thread [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**Peer-Message**](/windows/desktop/DevNotes/-peekmessage)aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="6834b-112">If you pass (DWORD)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/DevNotes/-peekmessage).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6834b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6834b-113">Return value</span></span>

<span data-ttu-id="6834b-114">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6834b-114">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6834b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6834b-115">Requirements</span></span>



| <span data-ttu-id="6834b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6834b-116">Requirement</span></span> | <span data-ttu-id="6834b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6834b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6834b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6834b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6834b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6834b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6834b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6834b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6834b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6834b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6834b-122">Header</span><span class="sxs-lookup"><span data-stu-id="6834b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6834b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6834b-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6834b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6834b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="6834b-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6834b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6834b-126">**RB- \_ EndDrag**</span><span class="sxs-lookup"><span data-stu-id="6834b-126">**RB\_ENDDRAG**</span></span>](rb-enddrag.md)
</dt> </dl>

 

