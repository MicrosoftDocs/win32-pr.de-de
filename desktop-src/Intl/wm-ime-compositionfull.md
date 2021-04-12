---
description: Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz zum Erweitern des Bereichs für das Kompositionsfenster findet. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: WM_IME_COMPOSITIONFULL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218683"
---
# <a name="wm_ime_compositionfull-message"></a><span data-ttu-id="e7a3c-104">"WM \_ IME \_ compositionfull"-Meldung</span><span class="sxs-lookup"><span data-stu-id="e7a3c-104">WM\_IME\_COMPOSITIONFULL message</span></span>

<span data-ttu-id="e7a3c-105">Wird an eine Anwendung gesendet, wenn das IME-Fenster keinen Platz zum Erweitern des Bereichs für das Kompositionsfenster findet.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-105">Sent to an application when the IME window finds no space to extend the area for the composition window.</span></span> <span data-ttu-id="e7a3c-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a><span data-ttu-id="e7a3c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a3c-107">Parameters</span></span>

<span data-ttu-id="e7a3c-108">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-108">This message has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="e7a3c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7a3c-109">Return value</span></span>

<span data-ttu-id="e7a3c-110">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-110">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7a3c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7a3c-111">Remarks</span></span>

<span data-ttu-id="e7a3c-112">Die Anwendung sollte mithilfe des Befehls [IMC \_ setcompositionwindow](imc-setcompositionwindow.md) angeben, wie das Fenster angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-112">The application should use the [IMC\_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) command to specify how the window should be displayed.</span></span>

<span data-ttu-id="e7a3c-113">Das IME-Fenster sendet diese Benachrichtigungs Meldung nicht in den IME, sondern von der [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e7a3c-113">The IME window, instead of the IME, sends this notification message by the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a3c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7a3c-114">Requirements</span></span>



| <span data-ttu-id="e7a3c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7a3c-115">Requirement</span></span> | <span data-ttu-id="e7a3c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e7a3c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a3c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7a3c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a3c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a3c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7a3c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7a3c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a3c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7a3c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7a3c-121">Header</span><span class="sxs-lookup"><span data-stu-id="e7a3c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a3c-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e7a3c-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a3c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7a3c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a3c-124">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="e7a3c-124">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="e7a3c-125">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="e7a3c-125">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> <dt>

[<span data-ttu-id="e7a3c-126">IMC \_ setcompositionwindow</span><span class="sxs-lookup"><span data-stu-id="e7a3c-126">IMC\_SETCOMPOSITIONWINDOW</span></span>](imc-setcompositionwindow.md)
</dt> </dl>

 

 
