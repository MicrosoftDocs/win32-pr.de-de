---
title: EM_UNDO Meldung (Winuser. h)
description: Diese Nachricht macht den letzten Bearbeitungs Steuerungs Vorgang in der Rückgängig-Warteschlange des-Steuer Elements rückgängig. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Windows-Steuerelemente für EM_UNDO Meldung
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741577"
---
# <a name="em_undo-message"></a><span data-ttu-id="50780-105">EM- \_ Rückgängig Meldung</span><span class="sxs-lookup"><span data-stu-id="50780-105">EM\_UNDO message</span></span>

<span data-ttu-id="50780-106">Diese Nachricht macht den letzten Bearbeitungs Steuerungs Vorgang in der Rückgängig-Warteschlange des-Steuer Elements rückgängig.</span><span class="sxs-lookup"><span data-stu-id="50780-106">This message undoes the last edit control operation in the control's undo queue.</span></span> <span data-ttu-id="50780-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="50780-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="50780-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50780-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50780-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50780-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50780-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="50780-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="50780-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50780-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50780-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="50780-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50780-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50780-113">Return value</span></span>

<span data-ttu-id="50780-114">Bei einem einzeiligen Bearbeitungs Steuerelement ist der Rückgabewert immer " **true**".</span><span class="sxs-lookup"><span data-stu-id="50780-114">For a single-line edit control, the return value is always **TRUE**.</span></span>

<span data-ttu-id="50780-115">Bei einem mehrzeiligen Bearbeitungs Steuerelement ist der Rückgabewert **true** , wenn der Rückgängig-Vorgang erfolgreich ist, oder **false** , wenn der Rückgängig-Vorgang fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="50780-115">For a multiline edit control, the return value is **TRUE** if the undo operation is successful, or **FALSE** if the undo operation fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="50780-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50780-116">Remarks</span></span>

<span data-ttu-id="50780-117">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Ein Rückgängig-Vorgang kann auch rückgängig gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="50780-117">**Edit controls and Rich Edit 1.0:** An undo operation can also be undone.</span></span> <span data-ttu-id="50780-118">Beispielsweise können Sie gelöschten Text mit der ersten **EM- \_ Rückgängig** -Nachricht wiederherstellen und den Text erneut mit einer zweiten **EM- \_ Rückgängig** -Meldung entfernen, solange es keinen dazwischen liegenden Bearbeitungsvorgang gibt.</span><span class="sxs-lookup"><span data-stu-id="50780-118">For example, you can restore deleted text with the first **EM\_UNDO** message, and remove the text again with a second **EM\_UNDO** message as long as there is no intervening edit operation.</span></span>

<span data-ttu-id="50780-119">**Rich Edit 2,0 und höher:** Die Rückgängig-Funktion ist eine mehrstufige Funktion, sodass das Senden von zwei **EM- \_ Rückgängig** -Nachrichten die letzten beiden Vorgänge in der rückgängig-</span><span class="sxs-lookup"><span data-stu-id="50780-119">**Rich Edit 2.0 and later:** The undo feature is multilevel so sending two **EM\_UNDO** messages will undo the last two operations in the undo queue.</span></span> <span data-ttu-id="50780-120">Um einen Vorgang wiederholen, senden Sie die EM-Wiederholungs Nachricht. [**\_**](em-redo.md)</span><span class="sxs-lookup"><span data-stu-id="50780-120">To redo an operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

<span data-ttu-id="50780-121">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="50780-121">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="50780-122">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="50780-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50780-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50780-123">Requirements</span></span>



| <span data-ttu-id="50780-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50780-124">Requirement</span></span> | <span data-ttu-id="50780-125">Wert</span><span class="sxs-lookup"><span data-stu-id="50780-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50780-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50780-126">Minimum supported client</span></span><br/> | <span data-ttu-id="50780-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50780-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50780-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50780-128">Minimum supported server</span></span><br/> | <span data-ttu-id="50780-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50780-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50780-130">Header</span><span class="sxs-lookup"><span data-stu-id="50780-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="50780-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="50780-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50780-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50780-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50780-133">**EM \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="50780-133">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> </dl>

 

 





