---
description: Wird an eine Anwendung gesendet, um Befehle und Anforderungs Informationen bereitzustellen. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: WM_IME_REQUEST Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353091"
---
# <a name="wm_ime_request-message"></a><span data-ttu-id="4139e-104">WM_IME_REQUEST Meldung</span><span class="sxs-lookup"><span data-stu-id="4139e-104">WM_IME_REQUEST message</span></span>

<span data-ttu-id="4139e-105">Wird an eine Anwendung gesendet, um Befehle und Anforderungs Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4139e-105">Sent to an application to provide commands and request information.</span></span> <span data-ttu-id="4139e-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4139e-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="4139e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4139e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4139e-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="4139e-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4139e-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="4139e-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="4139e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4139e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4139e-111">Befehl.</span><span class="sxs-lookup"><span data-stu-id="4139e-111">Command.</span></span> <span data-ttu-id="4139e-112">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="4139e-112">This parameter can have one of the following values:</span></span>

<dl> 
<dd><span data-ttu-id="4139e-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4139e-113"><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4139e-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span><span class="sxs-lookup"><span data-stu-id="4139e-114"><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></span></span></dd> 
<dd><span data-ttu-id="4139e-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="4139e-115"><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></span></span></dd> 
<dd><span data-ttu-id="4139e-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="4139e-116"><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></span></span></dd> 
<dd><span data-ttu-id="4139e-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span><span class="sxs-lookup"><span data-stu-id="4139e-117"><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></span></span></dd> 
<dd><span data-ttu-id="4139e-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span><span class="sxs-lookup"><span data-stu-id="4139e-118"><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></span></span></dd> 
<dd><span data-ttu-id="4139e-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span><span class="sxs-lookup"><span data-stu-id="4139e-119"><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></span></span></dd> 
</dl> 
</dd> 
<dt>

<span data-ttu-id="4139e-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4139e-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4139e-121">Befehls spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="4139e-121">Command-specific data.</span></span> <span data-ttu-id="4139e-122">Weitere Informationen finden Sie in der Beschreibung der einzelnen Befehle.</span><span class="sxs-lookup"><span data-stu-id="4139e-122">For more information, see the description for each command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4139e-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4139e-123">Return value</span></span>

<span data-ttu-id="4139e-124">Gibt einen Befehls spezifischen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4139e-124">Returns a command-specific value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4139e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4139e-125">Requirements</span></span>



| <span data-ttu-id="4139e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4139e-126">Requirement</span></span> | <span data-ttu-id="4139e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4139e-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4139e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4139e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4139e-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4139e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4139e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4139e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4139e-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4139e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4139e-132">Header</span><span class="sxs-lookup"><span data-stu-id="4139e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4139e-133"><dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4139e-133"><dt>Winuser.h (include Windows.h); </dt> <dt>Imm.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4139e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4139e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4139e-135">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="4139e-135">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="4139e-136">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="4139e-136">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="4139e-137">IMR_CANDIDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="4139e-137">IMR_CANDIDATEWINDOW</span></span>](imr-candidatewindow.md)
</dt> <dt>

[<span data-ttu-id="4139e-138">IMR_COMPOSITIONFONT</span><span class="sxs-lookup"><span data-stu-id="4139e-138">IMR_COMPOSITIONFONT</span></span>](imr-compositionfont.md)
</dt> <dt>

[<span data-ttu-id="4139e-139">IMR_COMPOSITIONWINDOW</span><span class="sxs-lookup"><span data-stu-id="4139e-139">IMR_COMPOSITIONWINDOW</span></span>](imr-compositionwindow.md)
</dt> <dt>

[<span data-ttu-id="4139e-140">IMR_CONFIRMRECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="4139e-140">IMR_CONFIRMRECONVERTSTRING</span></span>](imr-confirmreconvertstring.md)
</dt> <dt>

[<span data-ttu-id="4139e-141">IMR_DOCUMENTFEED</span><span class="sxs-lookup"><span data-stu-id="4139e-141">IMR_DOCUMENTFEED</span></span>](imr-documentfeed.md)
</dt> <dt>

[<span data-ttu-id="4139e-142">IMR_QUERYCHARPOSITION</span><span class="sxs-lookup"><span data-stu-id="4139e-142">IMR_QUERYCHARPOSITION</span></span>](imr-querycharposition.md)
</dt> <dt>

[<span data-ttu-id="4139e-143">IMR_RECONVERTSTRING</span><span class="sxs-lookup"><span data-stu-id="4139e-143">IMR_RECONVERTSTRING</span></span>](imr-reconvertstring.md)
</dt> </dl>

 

 
