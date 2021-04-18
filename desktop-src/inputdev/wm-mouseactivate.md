---
title: WM_MOUSEACTIVATE Meldung (Winuser. h)
description: Wird gesendet, wenn sich der Cursor in einem inaktiven Fenster befindet und der Benutzer eine Maustaste drückt. Das übergeordnete Fenster empfängt diese Nachricht nur, wenn das untergeordnete Fenster es an die defwindowproc-Funktion übergibt.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEACTIVATE Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103402"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="cb12e-105">WM- \_ moulogaktivierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="cb12e-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="cb12e-106">Wird gesendet, wenn sich der Cursor in einem inaktiven Fenster befindet und der Benutzer eine Maustaste drückt.</span><span class="sxs-lookup"><span data-stu-id="cb12e-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="cb12e-107">Das übergeordnete Fenster empfängt diese Nachricht nur, wenn das untergeordnete Fenster es an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="cb12e-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="cb12e-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="cb12e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="cb12e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb12e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb12e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb12e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb12e-111">Ein Handle für das übergeordnete Fenster der obersten Ebene des Fensters, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="cb12e-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="cb12e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb12e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb12e-113">Das nieder wertige Wort gibt den von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zurückgegebenen Treffer Testwert als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="cb12e-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="cb12e-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="cb12e-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="cb12e-115">Das höchst wertige Wort gibt den Bezeichner der Maus Meldung an, die generiert wurde, als der Benutzer eine Maustaste gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="cb12e-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="cb12e-116">Abhängig vom Rückgabewert wird die Maus Nachricht entweder verworfen oder im Fenster gepostet.</span><span class="sxs-lookup"><span data-stu-id="cb12e-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb12e-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb12e-117">Return value</span></span>

<span data-ttu-id="cb12e-118">Der Rückgabewert gibt an, ob das Fenster aktiviert werden soll und ob der Bezeichner der Maus Nachricht verworfen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb12e-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="cb12e-119">Es muss sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="cb12e-119">It must be one of the following values.</span></span>



| <span data-ttu-id="cb12e-120">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="cb12e-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="cb12e-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb12e-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb12e-122"><dt>**MA \_**</dt> <dt>1</dt> aktivieren</span><span class="sxs-lookup"><span data-stu-id="cb12e-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="cb12e-123">Aktiviert das Fenster, und die Maus Meldung wird nicht verworfen.</span><span class="sxs-lookup"><span data-stu-id="cb12e-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="cb12e-124"><dt>**MA \_ Activateandeat**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cb12e-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="cb12e-125">Aktiviert das Fenster und verwirft die Maus Meldung.</span><span class="sxs-lookup"><span data-stu-id="cb12e-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="cb12e-126"><dt>**MA \_ Noaktivierung**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cb12e-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="cb12e-127">Das Fenster wird nicht aktiviert, und die Maus Meldung wird nicht verworfen.</span><span class="sxs-lookup"><span data-stu-id="cb12e-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="cb12e-128"><dt>**MA \_ Noactivateandeat**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cb12e-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="cb12e-129">Aktiviert das Fenster nicht, sondern verwirft die Maus Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cb12e-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="cb12e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb12e-130">Remarks</span></span>

<span data-ttu-id="cb12e-131">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt die Nachricht an das übergeordnete Fenster eines untergeordneten Fensters, bevor eine Verarbeitung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cb12e-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="cb12e-132">Das übergeordnete Fenster bestimmt, ob das untergeordnete Fenster aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb12e-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="cb12e-133">Wenn das untergeordnete Fenster aktiviert wird, sollte das übergeordnete Fenster " **MA \_ noaktivierungs** " oder " **MA \_ noactivateandeat** " zurückgeben, um zu verhindern, dass das System die Nachricht weiterverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cb12e-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb12e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb12e-134">Requirements</span></span>



| <span data-ttu-id="cb12e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb12e-135">Requirement</span></span> | <span data-ttu-id="cb12e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="cb12e-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb12e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb12e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cb12e-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb12e-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb12e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb12e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cb12e-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb12e-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb12e-141">Header</span><span class="sxs-lookup"><span data-stu-id="cb12e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb12e-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cb12e-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb12e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb12e-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb12e-144">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cb12e-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb12e-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="cb12e-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="cb12e-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb12e-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cb12e-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb12e-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cb12e-148">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="cb12e-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="cb12e-149">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cb12e-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb12e-150">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="cb12e-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

