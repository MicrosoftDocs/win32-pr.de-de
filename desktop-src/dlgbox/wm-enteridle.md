---
title: WM_ENTERIDLE Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines modalen Dialog Felds oder Menüs gesendet, das in den Leerlaufzustand wechselt. Ein modales Dialogfeld oder Menü wechselt in den Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem mindestens eine vorherige Nachricht verarbeitet wurde.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Dialog Felder WM_ENTERIDLE Meldung
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392101"
---
# <a name="wm_enteridle-message"></a><span data-ttu-id="9fc00-105">WM-Enterprise- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="9fc00-105">WM\_ENTERIDLE message</span></span>

<span data-ttu-id="9fc00-106">Wird an das Besitzer Fenster eines modalen Dialog Felds oder Menüs gesendet, das in den Leerlaufzustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="9fc00-106">Sent to the owner window of a modal dialog box or menu that is entering an idle state.</span></span> <span data-ttu-id="9fc00-107">Ein modales Dialogfeld oder Menü wechselt in den Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem mindestens eine vorherige Nachricht verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="9fc00-107">A modal dialog box or menu enters an idle state when no messages are waiting in its queue after it has processed one or more previous messages.</span></span>


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a><span data-ttu-id="9fc00-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fc00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc00-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9fc00-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc00-110">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="9fc00-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9fc00-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9fc00-111">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="9fc00-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9fc00-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <span data-ttu-id="9fc00-113"><dt>**MSGF \_ Dialogbox**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9fc00-113"><dt>**MSGF\_DIALOGBOX**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="9fc00-114">Das System befindet sich im Leerlauf, weil ein Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fc00-114">The system is idle because a dialog box is displayed.</span></span><br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <span data-ttu-id="9fc00-115"><dt>**MSGF \_ Menü**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9fc00-115"><dt>**MSGF\_MENU**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="9fc00-116">Das System befindet sich im Leerlauf, weil ein Menü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fc00-116">The system is idle because a menu is displayed.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="9fc00-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9fc00-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc00-118">Ein Handle für das Dialogfeld (wenn *wParam* das **MSGF- \_ Dialogfeld** ist) oder ein Fenster mit dem angezeigten Menü (wenn *wParam* das **MSGF- \_ Menü** ist).</span><span class="sxs-lookup"><span data-stu-id="9fc00-118">A handle to the dialog box (if *wParam* is **MSGF\_DIALOGBOX**) or window containing the displayed menu (if *wParam* is **MSGF\_MENU**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fc00-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fc00-119">Return value</span></span>

<span data-ttu-id="9fc00-120">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9fc00-120">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc00-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fc00-121">Remarks</span></span>

<span data-ttu-id="9fc00-122">Wenn Sie das Dialogfeld mit dem Format " **DS \_ noidlemsg** " erstellen, können Sie die " **WM \_ Enter inidle** "-Meldung für ein Dialogfeld unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="9fc00-122">You can suppress the **WM\_ENTERIDLE** message for a dialog box by creating the dialog box with the **DS\_NOIDLEMSG** style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc00-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fc00-123">Requirements</span></span>



| <span data-ttu-id="9fc00-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fc00-124">Requirement</span></span> | <span data-ttu-id="9fc00-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9fc00-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc00-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fc00-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc00-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fc00-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9fc00-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fc00-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc00-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fc00-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9fc00-130">Header</span><span class="sxs-lookup"><span data-stu-id="9fc00-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc00-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc00-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc00-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fc00-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="9fc00-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9fc00-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc00-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9fc00-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="9fc00-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9fc00-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fc00-136">Dialog Felder</span><span class="sxs-lookup"><span data-stu-id="9fc00-136">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

