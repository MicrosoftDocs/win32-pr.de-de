---
description: Wird von IME an eine Anwendung gesendet, um die Anwendung über einen Tastendruck zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: db7075fb-b3d4-4d32-a0db-096d17d67c72
title: WM_IME_KEYDOWN Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3089af3c839f70e7f55895ae13158e7b2240605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214637"
---
# <a name="wm_ime_keydown-message"></a><span data-ttu-id="6cef9-104">WM- \_ IME- \_ KeyDown-Meldung</span><span class="sxs-lookup"><span data-stu-id="6cef9-104">WM\_IME\_KEYDOWN message</span></span>

<span data-ttu-id="6cef9-105">Wird von IME an eine Anwendung gesendet, um die Anwendung über einen Tastendruck zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6cef9-105">Sent to an application by the IME to notify the application of a key press and to keep message order.</span></span> <span data-ttu-id="6cef9-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6cef9-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,        
  WM_IME_KEYDOWN,  
  WPARAM wParam, 
  LPARAM lParam      
);
```



## <a name="parameters"></a><span data-ttu-id="6cef9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cef9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cef9-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="6cef9-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="6cef9-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="6cef9-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="6cef9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cef9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cef9-111">Der virtuelle Schlüsselcode des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="6cef9-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="6cef9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cef9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cef9-113">Wiederholungs Anzahl, Überprüfungs Code, erweitertes schlüsselflag, Kontext Code, Vorheriges schlüsselstatusflag und Übergangs Zustands Kennzeichen, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6cef9-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown in the following table.</span></span>



| <span data-ttu-id="6cef9-114">bit</span><span class="sxs-lookup"><span data-stu-id="6cef9-114">Bit</span></span>   | <span data-ttu-id="6cef9-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6cef9-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="6cef9-116">0-15</span><span class="sxs-lookup"><span data-stu-id="6cef9-116">0-15</span></span>  | <span data-ttu-id="6cef9-117">Wiederholungs Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6cef9-117">Repeat count.</span></span>                                                               |
| <span data-ttu-id="6cef9-118">16-23</span><span class="sxs-lookup"><span data-stu-id="6cef9-118">16-23</span></span> | <span data-ttu-id="6cef9-119">Scannen Sie den Code.</span><span class="sxs-lookup"><span data-stu-id="6cef9-119">Scan code.</span></span>                                                                  |
| <span data-ttu-id="6cef9-120">24</span><span class="sxs-lookup"><span data-stu-id="6cef9-120">24</span></span>    | <span data-ttu-id="6cef9-121">Erweiterter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="6cef9-121">Extended key.</span></span> <span data-ttu-id="6cef9-122">Dieser Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="6cef9-122">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="6cef9-123">Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="6cef9-123">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="6cef9-124">25-28</span><span class="sxs-lookup"><span data-stu-id="6cef9-124">25-28</span></span> | <span data-ttu-id="6cef9-125">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6cef9-125">Not used.</span></span>                                                                   |
| <span data-ttu-id="6cef9-126">29</span><span class="sxs-lookup"><span data-stu-id="6cef9-126">29</span></span>    | <span data-ttu-id="6cef9-127">Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="6cef9-127">Context code.</span></span> <span data-ttu-id="6cef9-128">Dieser Wert ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="6cef9-128">This value is always 0.</span></span>                                       |
| <span data-ttu-id="6cef9-129">30</span><span class="sxs-lookup"><span data-stu-id="6cef9-129">30</span></span>    | <span data-ttu-id="6cef9-130">Vorheriger Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="6cef9-130">Previous key state.</span></span> <span data-ttu-id="6cef9-131">Dieser Wert ist 1, wenn der Schlüssel nicht aktiv ist, oder 0, wenn er aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="6cef9-131">This value is 1 if the key is down or 0 if it is up.</span></span>    |
| <span data-ttu-id="6cef9-132">31</span><span class="sxs-lookup"><span data-stu-id="6cef9-132">31</span></span>    | <span data-ttu-id="6cef9-133">Übergangsstatus.</span><span class="sxs-lookup"><span data-stu-id="6cef9-133">Transition state.</span></span> <span data-ttu-id="6cef9-134">Dieser Wert ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="6cef9-134">This value is always 0.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cef9-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6cef9-135">Return value</span></span>

<span data-ttu-id="6cef9-136">Eine Anwendung sollte 0 zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6cef9-136">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cef9-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6cef9-137">Remarks</span></span>

<span data-ttu-id="6cef9-138">Eine Anwendung kann diese Nachricht verarbeiten oder an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion übergeben, um eine übereinstimmende [**WM- \_ keydownnachricht**](../inputdev/wm-keydown.md) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="6cef9-138">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cef9-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cef9-139">Requirements</span></span>



| <span data-ttu-id="6cef9-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cef9-140">Requirement</span></span> | <span data-ttu-id="6cef9-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6cef9-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cef9-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cef9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6cef9-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cef9-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6cef9-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cef9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6cef9-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cef9-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6cef9-146">Header</span><span class="sxs-lookup"><span data-stu-id="6cef9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cef9-147"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6cef9-147"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cef9-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cef9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cef9-149">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="6cef9-149">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="6cef9-150">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="6cef9-150">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
