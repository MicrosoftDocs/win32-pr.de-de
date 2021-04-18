---
description: Wird an eine Anwendung gesendet, um Sie über Änderungen am IME-Fenster zu benachrichtigen. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: WM_IME_NOTIFY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343311"
---
# <a name="wm_ime_notify-message"></a><span data-ttu-id="31a49-104">WM_IME_NOTIFY Meldung</span><span class="sxs-lookup"><span data-stu-id="31a49-104">WM_IME_NOTIFY message</span></span>

<span data-ttu-id="31a49-105">Wird an eine Anwendung gesendet, um Sie über Änderungen am IME-Fenster zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="31a49-105">Sent to an application to notify it of changes to the IME window.</span></span> <span data-ttu-id="31a49-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="31a49-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="31a49-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="31a49-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a49-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="31a49-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="31a49-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="31a49-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="31a49-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31a49-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31a49-111">Der Befehl.</span><span class="sxs-lookup"><span data-stu-id="31a49-111">The command.</span></span> <span data-ttu-id="31a49-112">Dieser Parameter kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="31a49-112">This parameter can have one of the following values.</span></span>

<dl>
<dd><span data-ttu-id="31a49-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-113"><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-114"><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="31a49-115"><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="31a49-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-116"><a href="imn-guideline.md">IMN_GUIDELINE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-117"><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="31a49-118"><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="31a49-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="31a49-119"><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="31a49-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="31a49-120"><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="31a49-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="31a49-121"><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="31a49-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-122"><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="31a49-123"><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></span></span></dd> 
<dd><span data-ttu-id="31a49-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span><span class="sxs-lookup"><span data-stu-id="31a49-124"><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></span></span></dd> 
<dd><span data-ttu-id="31a49-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="31a49-125"><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="31a49-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31a49-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31a49-127">Befehls spezifische Daten, wobei das Format vom Wert des Parameters " *wParam* " abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="31a49-127">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="31a49-128">Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Befehlen.</span><span class="sxs-lookup"><span data-stu-id="31a49-128">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a49-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31a49-129">Return value</span></span>

<span data-ttu-id="31a49-130">Der Rückgabewert hängt vom gesendeten Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="31a49-130">The return value depends on the command sent.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a49-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31a49-131">Remarks</span></span>

<span data-ttu-id="31a49-132">Eine Anwendung verarbeitet diese Nachricht, wenn Sie für die Verwaltung des IME-Fensters zuständig ist.</span><span class="sxs-lookup"><span data-stu-id="31a49-132">An application processes this message if it is responsible for managing the IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a49-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a49-133">Requirements</span></span>



| <span data-ttu-id="31a49-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a49-134">Requirement</span></span> | <span data-ttu-id="31a49-135">Wert</span><span class="sxs-lookup"><span data-stu-id="31a49-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a49-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31a49-136">Minimum supported client</span></span><br/> | <span data-ttu-id="31a49-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31a49-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="31a49-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31a49-138">Minimum supported server</span></span><br/> | <span data-ttu-id="31a49-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31a49-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="31a49-140">Header</span><span class="sxs-lookup"><span data-stu-id="31a49-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a49-141"><dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31a49-141"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a49-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31a49-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a49-143">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="31a49-143">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="31a49-144">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="31a49-144">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="31a49-145">IMN_CHANGECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="31a49-145">IMN_CHANGECANDIDATE</span></span>](imn-changecandidate.md)
</dt> <dt>

[<span data-ttu-id="31a49-146">IMN_CLOSECANDIDATE</span><span class="sxs-lookup"><span data-stu-id="31a49-146">IMN_CLOSECANDIDATE</span></span>](imn-closecandidate.md)
</dt> <dt>

[<span data-ttu-id="31a49-147">IMN_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="31a49-147">IMN_CLOSESTATUSWINDOW</span></span>](imn-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="31a49-148">IMN_GUIDELINE</span><span class="sxs-lookup"><span data-stu-id="31a49-148">IMN_GUIDELINE</span></span>](imn-guideline.md)
</dt> <dt>

[<span data-ttu-id="31a49-149">IMN_OPENCANDIDATE</span><span class="sxs-lookup"><span data-stu-id="31a49-149">IMN_OPENCANDIDATE</span></span>](imn-opencandidate.md)
</dt> <dt>

[<span data-ttu-id="31a49-150">IMN_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="31a49-150">IMN_OPENSTATUSWINDOW</span></span>](imn-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="31a49-151">IMN_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="31a49-151">IMN_SETCANDIDATEPOS</span></span>](imn-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="31a49-152">IMN_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="31a49-152">IMN_SETCOMPOSITIONFONT</span></span>](imn-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="31a49-153">IMN_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="31a49-153">IMN_SETCOMPOSITIONWINDOW</span></span>](imn-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="31a49-154">IMN_SETCONVERSIONMODE</span><span class="sxs-lookup"><span data-stu-id="31a49-154">IMN_SETCONVERSIONMODE</span></span>](imn-setconversionmode.md)
</dt> <dt>

[<span data-ttu-id="31a49-155">IMN_SETOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="31a49-155">IMN_SETOPENSTATUS</span></span>](imn-setopenstatus.md)
</dt> <dt>

[<span data-ttu-id="31a49-156">IMN_SETSENTENCEMODE</span><span class="sxs-lookup"><span data-stu-id="31a49-156">IMN_SETSENTENCEMODE</span></span>](imn-setsentencemode.md)
</dt> <dt>

[<span data-ttu-id="31a49-157">IMN_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="31a49-157">IMN_SETSTATUSWINDOWPOS</span></span>](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
