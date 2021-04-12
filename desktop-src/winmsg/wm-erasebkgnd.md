---
description: Wird gesendet, wenn der Fenster Hintergrund gelöscht werden muss (z. b. wenn die Größe eines Fensters geändert wird). Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters zum Zeichnen vorzubereiten.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: WM_ERASEBKGND Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216959"
---
# <a name="wm_erasebkgnd-message"></a><span data-ttu-id="9ed82-104">WM \_ erasebkgnd-Meldung</span><span class="sxs-lookup"><span data-stu-id="9ed82-104">WM\_ERASEBKGND message</span></span>

<span data-ttu-id="9ed82-105">Wird gesendet, wenn der Fenster Hintergrund gelöscht werden muss (z. b. wenn die Größe eines Fensters geändert wird).</span><span class="sxs-lookup"><span data-stu-id="9ed82-105">Sent when the window background must be erased (for example, when a window is resized).</span></span> <span data-ttu-id="9ed82-106">Die Nachricht wird gesendet, um einen ungültigen Teil eines Fensters zum Zeichnen vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="9ed82-106">The message is sent to prepare an invalidated portion of a window for painting.</span></span>


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a><span data-ttu-id="9ed82-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ed82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed82-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ed82-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed82-109">Ein Handle für den Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="9ed82-109">A handle to the device context.</span></span>

</dd> <dt>

<span data-ttu-id="9ed82-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ed82-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ed82-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ed82-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed82-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ed82-112">Return value</span></span>

<span data-ttu-id="9ed82-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ed82-113">Type: **LRESULT**</span></span>

<span data-ttu-id="9ed82-114">Eine Anwendung sollte einen Wert ungleich 0 (null) zurückgeben, wenn Sie den Hintergrund löscht. Andernfalls sollte NULL zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9ed82-114">An application should return nonzero if it erases the background; otherwise, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed82-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ed82-115">Remarks</span></span>

<span data-ttu-id="9ed82-116">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion löscht den Hintergrund mithilfe des klassenhintergrund Pinsels, der durch den **hbrbackground** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9ed82-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function erases the background by using the class background brush specified by the **hbrBackground** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure.</span></span> <span data-ttu-id="9ed82-117">Wenn **hbrbackground** **null** ist, muss die Anwendung die **WM- \_ erasebkgnd** -Nachricht verarbeiten und den Hintergrund löschen.</span><span class="sxs-lookup"><span data-stu-id="9ed82-117">If **hbrBackground** is **NULL**, the application should process the **WM\_ERASEBKGND** message and erase the background.</span></span>

<span data-ttu-id="9ed82-118">Eine Anwendung sollte als Antwort auf **WM \_ erasebkgnd** einen Wert ungleich 0 (null) zurückgeben, wenn Sie die Nachricht verarbeitet und den Hintergrund löscht. Dies weist darauf hin, dass kein weiterer Löschvorgang erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9ed82-118">An application should return nonzero in response to **WM\_ERASEBKGND** if it processes the message and erases the background; this indicates that no further erasing is required.</span></span> <span data-ttu-id="9ed82-119">Wenn die Anwendung 0 (null) zurückgibt, bleibt das Fenster zum Löschen markiert.</span><span class="sxs-lookup"><span data-stu-id="9ed82-119">If the application returns zero, the window will remain marked for erasing.</span></span> <span data-ttu-id="9ed82-120">(In der Regel bedeutet dies, dass der **ferase** -Member der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur " **true**" ist.)</span><span class="sxs-lookup"><span data-stu-id="9ed82-120">(Typically, this indicates that the **fErase** member of the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure will be **TRUE**.)</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed82-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ed82-121">Requirements</span></span>



| <span data-ttu-id="9ed82-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ed82-122">Requirement</span></span> | <span data-ttu-id="9ed82-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9ed82-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed82-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ed82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed82-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ed82-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ed82-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ed82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed82-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ed82-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ed82-128">Header</span><span class="sxs-lookup"><span data-stu-id="9ed82-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed82-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed82-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ed82-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ed82-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ed82-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9ed82-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ed82-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9ed82-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9ed82-133">**WNDCLASS**</span><span class="sxs-lookup"><span data-stu-id="9ed82-133">**WNDCLASS**</span></span>](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

<span data-ttu-id="9ed82-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9ed82-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ed82-135">Symbole</span><span class="sxs-lookup"><span data-stu-id="9ed82-135">Icons</span></span>](../menurc/icons.md)
</dt> <dt>

<span data-ttu-id="9ed82-136">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="9ed82-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9ed82-137">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="9ed82-137">**BeginPaint**</span></span>](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="9ed82-138">**PAINTSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="9ed82-138">**PAINTSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
