---
title: WM_NEXTDLGCTL Meldung (Winuser. h)
description: Wird an eine Dialogfeld Prozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld festzulegen.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Dialog Felder WM_NEXTDLGCTL Meldung
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518344"
---
# <a name="wm_nextdlgctl-message"></a><span data-ttu-id="8676f-104">WM- \_ nextdlgctl-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8676f-104">WM\_NEXTDLGCTL message</span></span>

<span data-ttu-id="8676f-105">Wird an eine Dialogfeld Prozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8676f-105">Sent to a dialog box procedure to set the keyboard focus to a different control in the dialog box.</span></span>


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a><span data-ttu-id="8676f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8676f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8676f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8676f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8676f-108">Wenn *LPARAM* den Wert **true** hat, identifiziert dieser Parameter das Steuerelement, das den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="8676f-108">If *lParam* is **TRUE**, this parameter identifies the control that receives the focus.</span></span> <span data-ttu-id="8676f-109">Wenn *LPARAM* auf **false** festgelegt ist, gibt dieser Parameter an, ob das nächste oder vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="8676f-109">If *lParam* is **FALSE**, this parameter indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span> <span data-ttu-id="8676f-110">Wenn *wParam* gleich 0 (null) ist, erhält das nächste Steuerelement den Fokus. Andernfalls erhält das vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus.</span><span class="sxs-lookup"><span data-stu-id="8676f-110">If *wParam* is zero, the next control receives the focus; otherwise, the previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> <dt>

<span data-ttu-id="8676f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8676f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8676f-112">Das nieder wertige Wort gibt an, wie das System *wParam* verwendet.</span><span class="sxs-lookup"><span data-stu-id="8676f-112">The low-order word indicates how the system uses *wParam*.</span></span> <span data-ttu-id="8676f-113">Wenn das nieder wertige Wort **true** ist, ist *wParam* ein Handle, das dem Steuerelement zugeordnet ist, das den Fokus erhält. Andernfalls ist *wParam* ein Flag, das angibt, ob das nächste oder vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="8676f-113">If the low-order word is **TRUE**, *wParam* is a handle associated with the control that receives the focus; otherwise, *wParam* is a flag that indicates whether the next or previous control with the **WS\_TABSTOP** style receives the focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8676f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8676f-114">Return value</span></span>

<span data-ttu-id="8676f-115">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8676f-115">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8676f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8676f-116">Remarks</span></span>

<span data-ttu-id="8676f-117">Diese Meldung führt zusätzliche Dialogfeld-Verwaltungsvorgänge aus, die über diejenigen hinausgehen, die von der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion **WM- \_ nextdlgctl** ausgeführt werden, aktualisiert den standardmäßigen PUSHBUTTON-Rahmen, legt den Standard Steuerelement Bezeichner fest und wählt automatisch den Text eines Bearbeitungs Steuer Elements aus</span><span class="sxs-lookup"><span data-stu-id="8676f-117">This message performs additional dialog box management operations beyond those performed by the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function **WM\_NEXTDLGCTL** updates the default pushbutton border, sets the default control identifier, and automatically selects the text of an edit control (if the target window is an edit control).</span></span>

<span data-ttu-id="8676f-118">Verwenden Sie die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion nicht, um eine **WM- \_ nextdlgctl** -Nachricht zu senden, wenn Ihre Anwendung andere Nachrichten, die den Fokus festlegen, gleichzeitig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8676f-118">Do not use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to send a **WM\_NEXTDLGCTL** message if your application will concurrently process other messages that set the focus.</span></span> <span data-ttu-id="8676f-119">Verwenden Sie stattdessen die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8676f-119">Use the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="8676f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8676f-120">Requirements</span></span>



| <span data-ttu-id="8676f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8676f-121">Requirement</span></span> | <span data-ttu-id="8676f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8676f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8676f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8676f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8676f-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8676f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8676f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8676f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8676f-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8676f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8676f-127">Header</span><span class="sxs-lookup"><span data-stu-id="8676f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8676f-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8676f-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8676f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8676f-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8676f-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8676f-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8676f-131">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="8676f-131">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="8676f-132">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="8676f-132">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="8676f-133">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="8676f-133">**SetFocus**</span></span>](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

<span data-ttu-id="8676f-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8676f-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8676f-135">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="8676f-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

