---
title: EM_CANUNDO Meldung (Winuser. h)
description: Bestimmt, ob in der Rückgängig-Warteschlange eines Bearbeitungs Steuer Elements Aktionen vorhanden sind. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Windows-Steuerelemente für EM_CANUNDO Meldung
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104504"
---
# <a name="em_canundo-message"></a><span data-ttu-id="6d815-105">EM \_ CanUndo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="6d815-105">EM\_CANUNDO message</span></span>

<span data-ttu-id="6d815-106">Bestimmt, ob in der Rückgängig-Warteschlange eines Bearbeitungs Steuer Elements Aktionen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6d815-106">Determines whether there are any actions in an edit control's undo queue.</span></span> <span data-ttu-id="6d815-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="6d815-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d815-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d815-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d815-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d815-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d815-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6d815-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6d815-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d815-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6d815-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="6d815-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d815-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d815-113">Return value</span></span>

<span data-ttu-id="6d815-114">Wenn Aktionen in der Rückgängig-Warteschlange des Steuer Elements vorhanden sind, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6d815-114">If there are actions in the control's undo queue, the return value is nonzero.</span></span>

<span data-ttu-id="6d815-115">Wenn die Rückgängig-Warteschlange leer ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6d815-115">If the undo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d815-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d815-116">Remarks</span></span>

<span data-ttu-id="6d815-117">Wenn die Rückgängig-Warteschlange nicht leer ist, können Sie die [**EM- \_ Rückgängig**](em-undo.md) Meldung an das Steuerelement senden, um den letzten Vorgang rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="6d815-117">If the undo queue is not empty, you can send the [**EM\_UNDO**](em-undo.md) message to the control to undo the most recent operation.</span></span>

<span data-ttu-id="6d815-118">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Die Rückgängig-Warteschlange enthält nur den letzten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6d815-118">**Edit controls and Rich Edit 1.0:** The undo queue contains only the most recent operation.</span></span>

<span data-ttu-id="6d815-119">**Rich Edit 2,0 und höher:** Die Rückgängig-Warteschlange kann mehrere Vorgänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="6d815-119">**Rich Edit 2.0 and later:** The undo queue can contain multiple operations.</span></span>

<span data-ttu-id="6d815-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d815-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6d815-121">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="6d815-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d815-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d815-122">Requirements</span></span>



| <span data-ttu-id="6d815-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d815-123">Requirement</span></span> | <span data-ttu-id="6d815-124">Wert</span><span class="sxs-lookup"><span data-stu-id="6d815-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d815-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d815-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6d815-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d815-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d815-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d815-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6d815-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d815-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6d815-129">Header</span><span class="sxs-lookup"><span data-stu-id="6d815-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d815-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6d815-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d815-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d815-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d815-132">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="6d815-132">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





