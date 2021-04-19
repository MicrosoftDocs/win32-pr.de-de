---
description: Wird von IME an eine Anwendung gesendet, um die Anwendung über eine schlüsselfreigabe zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 652f951f-4e9f-407c-844c-b250b6a9e6f5
title: WM_IME_KEYUP Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0eb6c6701510a373573ff6d85d5b50a8541b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347775"
---
# <a name="wm_ime_keyup-message"></a><span data-ttu-id="06fcc-104">WM- \_ IME- \_ KeyUp-Meldung</span><span class="sxs-lookup"><span data-stu-id="06fcc-104">WM\_IME\_KEYUP message</span></span>

<span data-ttu-id="06fcc-105">Wird von IME an eine Anwendung gesendet, um die Anwendung über eine schlüsselfreigabe zu benachrichtigen und die Reihenfolge der Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="06fcc-105">Sent to an application by the IME to notify the application of a key release and to keep message order.</span></span> <span data-ttu-id="06fcc-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="06fcc-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_KEYUP,    
  WPARAM wParam,   
  LPARAM lParam    
);
```



## <a name="parameters"></a><span data-ttu-id="06fcc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="06fcc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fcc-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="06fcc-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="06fcc-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="06fcc-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="06fcc-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06fcc-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06fcc-111">Der virtuelle Schlüsselcode des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="06fcc-111">Virtual key code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="06fcc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06fcc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="06fcc-113">Wiederholungs Anzahl, Überprüfungs Code, erweitertes schlüsselflag, Kontext Code, Vorheriges schlüsselstatusflag und Übergangs Zustands Kennzeichen, wie unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="06fcc-113">Repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, as shown below.</span></span>



| <span data-ttu-id="06fcc-114">bit</span><span class="sxs-lookup"><span data-stu-id="06fcc-114">Bit</span></span>   | <span data-ttu-id="06fcc-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="06fcc-115">Meaning</span></span>                                                                     |
|-------|-----------------------------------------------------------------------------|
| <span data-ttu-id="06fcc-116">0-15</span><span class="sxs-lookup"><span data-stu-id="06fcc-116">0-15</span></span>  | <span data-ttu-id="06fcc-117">Wiederholungs Anzahl.</span><span class="sxs-lookup"><span data-stu-id="06fcc-117">Repeat count.</span></span> <span data-ttu-id="06fcc-118">Dieser Wert ist immer 1.</span><span class="sxs-lookup"><span data-stu-id="06fcc-118">This value is always 1.</span></span>                                       |
| <span data-ttu-id="06fcc-119">16-23</span><span class="sxs-lookup"><span data-stu-id="06fcc-119">16-23</span></span> | <span data-ttu-id="06fcc-120">Scannen Sie den Code.</span><span class="sxs-lookup"><span data-stu-id="06fcc-120">Scan code.</span></span>                                                                  |
| <span data-ttu-id="06fcc-121">24</span><span class="sxs-lookup"><span data-stu-id="06fcc-121">24</span></span>    | <span data-ttu-id="06fcc-122">Erweiterter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="06fcc-122">Extended key.</span></span> <span data-ttu-id="06fcc-123">Dieser Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="06fcc-123">This value is 1 if it is an extended key.</span></span> <span data-ttu-id="06fcc-124">Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="06fcc-124">Otherwise, it is 0.</span></span> |
| <span data-ttu-id="06fcc-125">25-28</span><span class="sxs-lookup"><span data-stu-id="06fcc-125">25-28</span></span> | <span data-ttu-id="06fcc-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="06fcc-126">Not used.</span></span>                                                                   |
| <span data-ttu-id="06fcc-127">29</span><span class="sxs-lookup"><span data-stu-id="06fcc-127">29</span></span>    | <span data-ttu-id="06fcc-128">Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="06fcc-128">Context code.</span></span> <span data-ttu-id="06fcc-129">Dieser Wert ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="06fcc-129">This value is always 0.</span></span>                                       |
| <span data-ttu-id="06fcc-130">30</span><span class="sxs-lookup"><span data-stu-id="06fcc-130">30</span></span>    | <span data-ttu-id="06fcc-131">Vorheriger Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="06fcc-131">Previous key state.</span></span> <span data-ttu-id="06fcc-132">Dieser Wert ist immer 1.</span><span class="sxs-lookup"><span data-stu-id="06fcc-132">This value is always 1.</span></span>                                 |
| <span data-ttu-id="06fcc-133">31</span><span class="sxs-lookup"><span data-stu-id="06fcc-133">31</span></span>    | <span data-ttu-id="06fcc-134">Übergangsstatus.</span><span class="sxs-lookup"><span data-stu-id="06fcc-134">Transition state.</span></span> <span data-ttu-id="06fcc-135">Dieser Wert ist immer 1.</span><span class="sxs-lookup"><span data-stu-id="06fcc-135">This value is always 1.</span></span>                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06fcc-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06fcc-136">Return value</span></span>

<span data-ttu-id="06fcc-137">Eine Anwendung sollte 0 zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="06fcc-137">An application should return 0 if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="06fcc-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06fcc-138">Remarks</span></span>

<span data-ttu-id="06fcc-139">Eine Anwendung kann diese Nachricht verarbeiten oder an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion übergeben, um eine übereinstimmende [**WM- \_ KeyUp**](../inputdev/wm-keyup.md) -Nachricht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="06fcc-139">An application can process this message or pass it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function to generate a matching [**WM\_KEYUP**](../inputdev/wm-keyup.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="06fcc-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06fcc-140">Requirements</span></span>



| <span data-ttu-id="06fcc-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06fcc-141">Requirement</span></span> | <span data-ttu-id="06fcc-142">Wert</span><span class="sxs-lookup"><span data-stu-id="06fcc-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fcc-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06fcc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06fcc-144">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06fcc-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="06fcc-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06fcc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06fcc-146">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06fcc-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06fcc-147">Header</span><span class="sxs-lookup"><span data-stu-id="06fcc-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="06fcc-148"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="06fcc-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fcc-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06fcc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fcc-150">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="06fcc-150">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="06fcc-151">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="06fcc-151">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
