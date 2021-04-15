---
title: WM_UNDO Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM- \_ Rückgängig Meldung an ein Bearbeitungs Steuerelement, um den letzten Vorgang rückgängig zu machen. Wenn diese Nachricht an ein Bearbeitungs Steuerelement gesendet wird, wird der zuvor gelöschte Text wieder hergestellt oder der zuvor hinzugefügte Text gelöscht.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Windows-Steuerelemente für WM_UNDO Meldung
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477526"
---
# <a name="wm_undo-message"></a><span data-ttu-id="5e754-105">WM- \_ Rückgängig Meldung</span><span class="sxs-lookup"><span data-stu-id="5e754-105">WM\_UNDO message</span></span>

<span data-ttu-id="5e754-106">Eine Anwendung sendet eine **WM- \_ Rückgängig** Meldung an ein Bearbeitungs Steuerelement, um den letzten Vorgang rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="5e754-106">An application sends a **WM\_UNDO** message to an edit control to undo the last operation.</span></span> <span data-ttu-id="5e754-107">Wenn diese Nachricht an ein Bearbeitungs Steuerelement gesendet wird, wird der zuvor gelöschte Text wieder hergestellt oder der zuvor hinzugefügte Text gelöscht.</span><span class="sxs-lookup"><span data-stu-id="5e754-107">When this message is sent to an edit control, the previously deleted text is restored or the previously added text is deleted.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e754-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e754-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e754-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e754-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e754-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5e754-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e754-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e754-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e754-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5e754-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e754-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e754-113">Return value</span></span>

<span data-ttu-id="5e754-114">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="5e754-114">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="5e754-115">Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="5e754-115">If the message fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e754-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e754-116">Remarks</span></span>

<span data-ttu-id="5e754-117">Umfassende **Bearbeitung:** Es wird empfohlen, [**EM \_ Undo**](em-undo.md) anstelle von **WM \_ Undo** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e754-117">**Rich Edit:** It is recommended that [**EM\_UNDO**](em-undo.md) be used instead of **WM\_UNDO**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e754-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e754-118">Requirements</span></span>



| <span data-ttu-id="5e754-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e754-119">Requirement</span></span> | <span data-ttu-id="5e754-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5e754-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e754-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e754-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5e754-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e754-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e754-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e754-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5e754-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e754-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e754-125">Header</span><span class="sxs-lookup"><span data-stu-id="5e754-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e754-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5e754-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e754-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e754-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e754-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5e754-128">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5e754-129">**WM \_ Clear**</span><span class="sxs-lookup"><span data-stu-id="5e754-129">**WM\_CLEAR**</span></span>](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[<span data-ttu-id="5e754-130">**WM- \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="5e754-130">**WM\_COPY**</span></span>](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[<span data-ttu-id="5e754-131">**WM \_ Ausschneiden**</span><span class="sxs-lookup"><span data-stu-id="5e754-131">**WM\_CUT**</span></span>](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[<span data-ttu-id="5e754-132">**WM \_ Einfügen**</span><span class="sxs-lookup"><span data-stu-id="5e754-132">**WM\_PASTE**</span></span>](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

