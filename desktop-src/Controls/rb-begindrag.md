---
title: RB_BEGINDRAG Meldung (kommstrg. h)
description: Versetzt das Grund leisten-Steuerelement in den Drag & Drop-Modus. Diese Meldung bewirkt nicht, dass eine RBN- \_ BeginDrag-Benachrichtigung gesendet wird.
ms.assetid: 1e3e4928-cb84-4fd4-8056-84de1f791d1c
keywords:
- Windows-Steuerelemente für RB_BEGINDRAG Meldung
topic_type:
- apiref
api_name:
- RB_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41865baa2bf6c640595296be9c157201d0cc16d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477889"
---
# <a name="rb_begindrag-message"></a><span data-ttu-id="e6894-105">RB \_ BeginDrag-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e6894-105">RB\_BEGINDRAG message</span></span>

<span data-ttu-id="e6894-106">Versetzt das Grund leisten-Steuerelement in den Drag & Drop-Modus.</span><span class="sxs-lookup"><span data-stu-id="e6894-106">Puts the rebar control in drag-and-drop mode.</span></span> <span data-ttu-id="e6894-107">Diese Meldung bewirkt nicht, dass eine [RBN- \_ BeginDrag](rbn-begindrag.md) -Benachrichtigung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6894-107">This message does not cause a [RBN\_BEGINDRAG](rbn-begindrag.md) notification to be sent.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6894-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6894-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6894-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6894-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6894-110">Der null basierte Index des Bands, auf den sich der Drag & Drop-Vorgang auswirkt.</span><span class="sxs-lookup"><span data-stu-id="e6894-110">Zero-based index of the band that the drag-and-drop operation will affect.</span></span>

</dd> <dt>

<span data-ttu-id="e6894-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6894-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6894-112">**DWORD** -Wert, der die Start Maus Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="e6894-112">**DWORD** value that contains the starting mouse coordinates.</span></span> <span data-ttu-id="e6894-113">Die horizontale Koordinate ist im LoWord enthalten, und die vertikale Koordinate ist im HIWORD enthalten.</span><span class="sxs-lookup"><span data-stu-id="e6894-113">The horizontal coordinate is contained in the LOWORD and the vertical coordinate is contained in the HIWORD.</span></span> <span data-ttu-id="e6894-114">Wenn Sie (**DWORD**)-1 übergeben, verwendet das Grund leisten-Steuerelement die Position des Mauszeigers, wenn der Thread des Steuer Elements das letzte Mal den Thread [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) oder [**Peer-Message**](/windows/desktop/api/winuser/nf-winuser-peekmessagea)aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="e6894-114">If you pass (**DWORD**)-1, the rebar control will use the position of the mouse the last time the control's thread called [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6894-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6894-115">Return value</span></span>

<span data-ttu-id="e6894-116">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6894-116">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6894-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6894-117">Remarks</span></span>

<span data-ttu-id="e6894-118">Mit den [**\_ EndDrag**](rb-enddrag.md) -Meldungen " **RB \_ BeginDrag**", "RB [**\_ DragMove**](rb-dragmove.md)" und "RB" können Sie eine [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle für ein Grund leisten-Steuerelement implementieren.</span><span class="sxs-lookup"><span data-stu-id="e6894-118">The **RB\_BEGINDRAG**, [**RB\_DRAGMOVE**](rb-dragmove.md), and [**RB\_ENDDRAG**](rb-enddrag.md) messages allow you to implement an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface for a rebar control.</span></span> <span data-ttu-id="e6894-119">Sie senden die **RB \_ BeginDrag** -Nachricht als Antwort [**auf IDropTarget::D ragenter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), senden **die \_ RB DragMove** -Nachricht als Antwort auf [**IDropTarget::D ragover**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover)und die **RB- \_ EndDrag** -Nachricht als Antwort auf [**IDropTarget::D ROP**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) und [**IDropTarget::D ragleave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span><span class="sxs-lookup"><span data-stu-id="e6894-119">You send the **RB\_BEGINDRAG** message in response to [**IDropTarget::DragEnter**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragenter), send the **RB\_DRAGMOVE** message in response to [**IDropTarget::DragOver**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragover), and the **RB\_ENDDRAG** message in response to [**IDropTarget::Drop**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop) and [**IDropTarget::DragLeave**](/windows/desktop/api/oleidl/nf-oleidl-idroptarget-dragleave).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6894-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6894-120">Requirements</span></span>



| <span data-ttu-id="e6894-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6894-121">Requirement</span></span> | <span data-ttu-id="e6894-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e6894-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6894-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6894-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6894-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6894-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6894-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6894-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6894-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6894-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6894-127">Header</span><span class="sxs-lookup"><span data-stu-id="e6894-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6894-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6894-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

