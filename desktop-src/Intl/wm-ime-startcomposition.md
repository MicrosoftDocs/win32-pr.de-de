---
description: Wird unmittelbar vor dem Generieren der Kompositions Zeichenfolge als Ergebnis eines Tastatur Schlags gesendet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: WM_IME_STARTCOMPOSITION Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862647"
---
# <a name="wm_ime_startcomposition-message"></a><span data-ttu-id="dcbe9-104">WM \_ IME \_ StartComposition-Nachricht</span><span class="sxs-lookup"><span data-stu-id="dcbe9-104">WM\_IME\_STARTCOMPOSITION message</span></span>

<span data-ttu-id="dcbe9-105">Wird unmittelbar vor dem Generieren der Kompositions Zeichenfolge als Ergebnis eines Tastatur Schlags gesendet.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-105">Sent immediately before the IME generates the composition string as a result of a keystroke.</span></span> <span data-ttu-id="dcbe9-106">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
  WPARAM wParam,            
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="dcbe9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcbe9-107">Parameters</span></span>

<span data-ttu-id="dcbe9-108">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="dcbe9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcbe9-109">Return value</span></span>

<span data-ttu-id="dcbe9-110">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcbe9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcbe9-111">Remarks</span></span>

<span data-ttu-id="dcbe9-112">Diese Meldung ist eine Benachrichtigung an ein IME-Fenster, um das Kompositionsfenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-112">This message is a notification to an IME window to open its composition window.</span></span> <span data-ttu-id="dcbe9-113">Eine Anwendung sollte diese Nachricht verarbeiten, wenn Sie selbst Kompositions Zeichen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-113">An application should process this message if it displays composition characters itself.</span></span>

<span data-ttu-id="dcbe9-114">Wenn eine Anwendung ein IME-Fenster erstellt hat, sollte diese Meldung an dieses Fenster übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-114">If an application has created an IME window, it should pass this message to that window.</span></span> <span data-ttu-id="dcbe9-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion verarbeitet die Nachricht, indem Sie Sie an das IME-Standardfenster übergibt.</span><span class="sxs-lookup"><span data-stu-id="dcbe9-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function processes the message by passing it to the default IME window.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcbe9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcbe9-116">Requirements</span></span>



| <span data-ttu-id="dcbe9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcbe9-117">Requirement</span></span> | <span data-ttu-id="dcbe9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="dcbe9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbe9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcbe9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcbe9-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcbe9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dcbe9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcbe9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcbe9-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcbe9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dcbe9-123">Header</span><span class="sxs-lookup"><span data-stu-id="dcbe9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcbe9-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="dcbe9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcbe9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcbe9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcbe9-126">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="dcbe9-126">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="dcbe9-127">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="dcbe9-127">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
