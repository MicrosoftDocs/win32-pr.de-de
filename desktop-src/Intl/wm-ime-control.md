---
description: Wird von einer Anwendung gesendet, um das IME-Fenster an den angeforderten Befehl weiterzuleiten.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: WM_IME_CONTROL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862651"
---
# <a name="wm_ime_control-message"></a><span data-ttu-id="cb8c8-103">WM_IME_CONTROL Meldung</span><span class="sxs-lookup"><span data-stu-id="cb8c8-103">WM_IME_CONTROL message</span></span>

<span data-ttu-id="cb8c8-104">Wird von einer Anwendung gesendet, um das IME-Fenster an den angeforderten Befehl weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-104">Sent by an application to direct the IME window to carry out the requested command.</span></span> <span data-ttu-id="cb8c8-105">Die Anwendung verwendet diese Nachricht, um das von ihr erstellte IME-Fenster zu steuern.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-105">The application uses this message to control the IME window that it has created.</span></span> <span data-ttu-id="cb8c8-106">Um diese Nachricht zu senden, ruft die Anwendung die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern auf.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-106">To send this message, the application calls the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the following parameters.</span></span>


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="cb8c8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb8c8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb8c8-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="cb8c8-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="cb8c8-109">Handle für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="cb8c8-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb8c8-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb8c8-111">Der Befehl.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-111">The command.</span></span> <span data-ttu-id="cb8c8-112">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="cb8c8-112">This parameter can have one of the following values:</span></span>

<dl>
<dd><span data-ttu-id="cb8c8-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-113"><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-114"><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-115"><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-116"><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-117"><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-118"><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-119"><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span><span class="sxs-lookup"><span data-stu-id="cb8c8-120"><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></span></span></dd> 
<dd><span data-ttu-id="cb8c8-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-121"><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="cb8c8-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span><span class="sxs-lookup"><span data-stu-id="cb8c8-122"><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></span></span></dd> 
</dl>
</dd>

<dt>

<span data-ttu-id="cb8c8-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb8c8-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb8c8-124">Befehls spezifische Daten, wobei das Format vom Wert des Parameters " *wParam* " abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-124">Command-specific data, with format dependent on the value of the *wParam* parameter.</span></span> <span data-ttu-id="cb8c8-125">Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Befehlen.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-125">For more information, refer to the documentation for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb8c8-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb8c8-126">Return value</span></span>

<span data-ttu-id="cb8c8-127">Die Meldung gibt einen Befehls spezifischen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="cb8c8-127">The message returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb8c8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb8c8-128">Requirements</span></span>



| <span data-ttu-id="cb8c8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb8c8-129">Requirement</span></span> | <span data-ttu-id="cb8c8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="cb8c8-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb8c8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb8c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cb8c8-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb8c8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="cb8c8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb8c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cb8c8-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb8c8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="cb8c8-135">Header</span><span class="sxs-lookup"><span data-stu-id="cb8c8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb8c8-136"><dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb8c8-136"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb8c8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb8c8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb8c8-138">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="cb8c8-138">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-139">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="cb8c8-139">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-140">IMC_CLOSESTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="cb8c8-140">IMC_CLOSESTATUSWINDOW</span></span>](imc-closestatuswindow.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-141">IMC_GETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="cb8c8-141">IMC_GETCANDIDATEPOS</span></span>](imc-getcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-142">IMC_GETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="cb8c8-142">IMC_GETCOMPOSITIONFONT</span></span>](imc-getcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-143">IMC_GETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="cb8c8-143">IMC_GETCOMPOSITIONWINDOW</span></span>](imc-getcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-144">IMC_GETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="cb8c8-144">IMC_GETSTATUSWINDOWPOS</span></span>](imc-getstatuswindowpos.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-145">IMC_OPENSTATUSWINDOW</span><span class="sxs-lookup"><span data-stu-id="cb8c8-145">IMC_OPENSTATUSWINDOW</span></span>](imc-openstatuswindow.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-146">IMC_SETCANDIDATEPOS</span><span class="sxs-lookup"><span data-stu-id="cb8c8-146">IMC_SETCANDIDATEPOS</span></span>](imc-setcandidatepos.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-147">IMC_SETCOMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="cb8c8-147">IMC_SETCOMPOSITIONFONT</span></span>](imc-setcompositionfont.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-148">IMC_SETCOMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="cb8c8-148">IMC_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> <dt>

[<span data-ttu-id="cb8c8-149">IMC_SETSTATUSWINDOWPOS</span><span class="sxs-lookup"><span data-stu-id="cb8c8-149">IMC_SETSTATUSWINDOWPOS</span></span>](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
