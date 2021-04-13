---
description: Wird an eine Anwendung gesendet, wenn das IME die Komposition beendet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343629"
---
# <a name="wm_ime_endcomposition-message"></a><span data-ttu-id="171dc-104">WM- \_ IME- \_ endkompositions Nachricht</span><span class="sxs-lookup"><span data-stu-id="171dc-104">WM\_IME\_ENDCOMPOSITION message</span></span>

<span data-ttu-id="171dc-105">Wird an eine Anwendung gesendet, wenn das IME die Komposition beendet.</span><span class="sxs-lookup"><span data-stu-id="171dc-105">Sent to an application when the IME ends composition.</span></span> <span data-ttu-id="171dc-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="171dc-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
  WPARAM wParam,      
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="171dc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="171dc-107">Parameters</span></span>

<span data-ttu-id="171dc-108">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="171dc-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="171dc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="171dc-109">Return value</span></span>

<span data-ttu-id="171dc-110">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="171dc-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="171dc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="171dc-111">Remarks</span></span>

<span data-ttu-id="171dc-112">Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="171dc-112">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="171dc-113">Wenn die Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="171dc-113">If the application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="171dc-114">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  -Funktion verarbeitet diese Nachricht, indem Sie Sie an das IME-Standardfenster übergibt.</span><span class="sxs-lookup"><span data-stu-id="171dc-114">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  function processes this message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="171dc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="171dc-115">Requirements</span></span>



| <span data-ttu-id="171dc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="171dc-116">Requirement</span></span> | <span data-ttu-id="171dc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="171dc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171dc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="171dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="171dc-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="171dc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="171dc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="171dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="171dc-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="171dc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="171dc-122">Header</span><span class="sxs-lookup"><span data-stu-id="171dc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="171dc-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="171dc-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="171dc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="171dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="171dc-125">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="171dc-125">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="171dc-126">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="171dc-126">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
