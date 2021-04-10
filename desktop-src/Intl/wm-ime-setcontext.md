---
description: Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214635"
---
# <a name="wm_ime_setcontext-message"></a><span data-ttu-id="b9388-104">WM \_ IME- \_ SetContext-Meldung</span><span class="sxs-lookup"><span data-stu-id="b9388-104">WM\_IME\_SETCONTEXT message</span></span>

<span data-ttu-id="b9388-105">Wird an eine Anwendung gesendet, wenn ein Fenster aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="b9388-105">Sent to an application when a window is activated.</span></span> <span data-ttu-id="b9388-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b9388-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="b9388-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9388-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9388-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b9388-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b9388-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="b9388-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="b9388-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9388-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9388-111">**True** , wenn das Fenster aktiv ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b9388-111">**TRUE** if the window is active, and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="b9388-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b9388-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9388-113">Anzeigeoptionen</span><span class="sxs-lookup"><span data-stu-id="b9388-113">Display options.</span></span> <span data-ttu-id="b9388-114">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b9388-114">This parameter can have one or more of the following values.</span></span>



| <span data-ttu-id="b9388-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b9388-115">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="b9388-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b9388-116">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <span data-ttu-id="b9388-117"><dt>**ISC \_ showuicompositionwindow**</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-117"><dt>**ISC\_SHOWUICOMPOSITIONWINDOW**</dt></span></span> </dl> | <span data-ttu-id="b9388-118">Fenster "Komposition" nach Benutzeroberflächen Fenster anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9388-118">Show the composition window by user interface window.</span></span><br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <span data-ttu-id="b9388-119"><dt>**ISC \_ showuiguidwindow**</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-119"><dt>**ISC\_SHOWUIGUIDWINDOW**</dt></span></span> </dl>                      | <span data-ttu-id="b9388-120">Zeigen Sie das Fenster "Guide" nach Benutzeroberflächen Fenster an.</span><span class="sxs-lookup"><span data-stu-id="b9388-120">Show the guide window by user interface window.</span></span><br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <span data-ttu-id="b9388-121"><dt>**ISC \_ showuisoft kbd**</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-121"><dt>**ISC\_SHOWUISOFTKBD**</dt></span></span> </dl>                               | <span data-ttu-id="b9388-122">Zeigt das Fenster "weiche Tastatur nach Benutzeroberfläche" an.</span><span class="sxs-lookup"><span data-stu-id="b9388-122">Show the soft keyboard by user interface window.</span></span><br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <span data-ttu-id="b9388-123"><dt>**ISC \_ showuicandidatewindow**</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-123"><dt>**ISC\_SHOWUICANDIDATEWINDOW**</dt></span></span> </dl>       | <span data-ttu-id="b9388-124">Anzeigen des Kandidaten Fensters von Index 0 nach Fenster der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="b9388-124">Show the candidate window of index 0 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b9388-125"><dt>ISC \_ showuicandidatewindow << 1</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-125"><dt>ISC\_SHOWUICANDIDATEWINDOW << 1</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b9388-126">Anzeigen des Kandidaten Fensters von Index 1 nach Benutzeroberflächen Fenster.</span><span class="sxs-lookup"><span data-stu-id="b9388-126">Show the candidate window of index 1 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b9388-127"><dt>ISC \_ showuicandidatewindow << 2</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-127"><dt>ISC\_SHOWUICANDIDATEWINDOW << 2</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b9388-128">Anzeigen des Kandidaten Fensters von Index 2 nach Benutzeroberflächen Fenster.</span><span class="sxs-lookup"><span data-stu-id="b9388-128">Show the candidate window of index 2 by user interface window.</span></span><br/> |
| <dl> <span data-ttu-id="b9388-129"><dt>ISC \_ showuicandidatewindow << 3</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-129"><dt>ISC\_SHOWUICANDIDATEWINDOW << 3</dt></span></span> </dl>                                                                                        | <span data-ttu-id="b9388-130">Anzeigen des Kandidaten Fensters von Index 3 nach Benutzeroberflächen Fenster.</span><span class="sxs-lookup"><span data-stu-id="b9388-130">Show the candidate window of index 3 by user interface window.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9388-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9388-131">Return value</span></span>

<span data-ttu-id="b9388-132">Gibt den von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)zurückgegebenen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b9388-132">Returns the value returned by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9388-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9388-133">Remarks</span></span>

<span data-ttu-id="b9388-134">Wenn die Anwendung ein IME-Fenster erstellt hat, sollte Sie " [**immisuimess Age**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b9388-134">If the application has created an IME window, it should call [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="b9388-135">Andernfalls sollte diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b9388-135">Otherwise, it should pass this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="b9388-136">Wenn die Anwendung das Kompositionsfenster zeichnet, muss das Fenster für die Zusammensetzung des standardmäßigen IME-Fensters nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b9388-136">If the application draws the composition window, the default IME window does not have to show its composition window.</span></span> <span data-ttu-id="b9388-137">In diesem Fall muss die Anwendung den Wert von **ISC \_ showuicompositionwindow** aus dem *LPARAM* -Parameter löschen, bevor Sie die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)übergibt.</span><span class="sxs-lookup"><span data-stu-id="b9388-137">In this case, the application must clear the **ISC\_SHOWUICOMPOSITIONWINDOW** value from the *lParam* parameter before passing the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) or [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).</span></span> <span data-ttu-id="b9388-138">Wenn Sie ein bestimmtes Fenster für die Benutzeroberfläche anzeigen möchten, sollte eine Anwendung den entsprechenden Wert entfernen, damit Sie vom IME nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9388-138">To display a certain user interface window, an application should remove the corresponding value so that the IME will not display it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9388-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9388-139">Requirements</span></span>



| <span data-ttu-id="b9388-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9388-140">Requirement</span></span> | <span data-ttu-id="b9388-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b9388-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9388-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9388-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b9388-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9388-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b9388-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9388-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b9388-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9388-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b9388-146">Header</span><span class="sxs-lookup"><span data-stu-id="b9388-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9388-147"><dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9388-147"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9388-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9388-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9388-149">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="b9388-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="b9388-150">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="b9388-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="b9388-151">**Immisuimess Age**</span><span class="sxs-lookup"><span data-stu-id="b9388-151">**ImmIsUIMessage**</span></span>](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
