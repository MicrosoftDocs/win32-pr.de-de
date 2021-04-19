---
description: Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist. Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d2444e70646d8122a7228094187738811a3f68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350340"
---
# <a name="wm_geticon-message"></a><span data-ttu-id="28497-104">WM- \_ GetIcon-Nachricht</span><span class="sxs-lookup"><span data-stu-id="28497-104">WM\_GETICON message</span></span>

<span data-ttu-id="28497-105">Wird an ein Fenster gesendet, um ein Handle für das große oder kleine Symbol abzurufen, das einem Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="28497-105">Sent to a window to retrieve a handle to the large or small icon associated with a window.</span></span> <span data-ttu-id="28497-106">Das System zeigt das große Symbol im Dialogfeld Alt + Tab und das kleine Symbol in der Fenster Beschriftung an.</span><span class="sxs-lookup"><span data-stu-id="28497-106">The system displays the large icon in the ALT+TAB dialog, and the small icon in the window caption.</span></span>

<span data-ttu-id="28497-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="28497-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a><span data-ttu-id="28497-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="28497-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28497-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28497-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28497-110">Der Typ des abgerufenen Symbols.</span><span class="sxs-lookup"><span data-stu-id="28497-110">The type of icon being retrieved.</span></span> <span data-ttu-id="28497-111">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="28497-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="28497-112">Wert</span><span class="sxs-lookup"><span data-stu-id="28497-112">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="28497-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="28497-113">Meaning</span></span>                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <span data-ttu-id="28497-114"><dt>**Symbol \_ Big**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="28497-114"><dt>**ICON\_BIG**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="28497-115">Rufen Sie das große Symbol für das Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="28497-115">Retrieve the large icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <span data-ttu-id="28497-116"><dt>**Symbol \_ Kleiner**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="28497-116"><dt>**ICON\_SMALL**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="28497-117">Rufen Sie das kleine Symbol für das Fenster ab.</span><span class="sxs-lookup"><span data-stu-id="28497-117">Retrieve the small icon for the window.</span></span><br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <span data-ttu-id="28497-118"><dt>**Symbol \_ SMALL2**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="28497-118"><dt>**ICON\_SMALL2**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="28497-119">Ruft das kleine Symbol ab, das von der Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="28497-119">Retrieves the small icon provided by the application.</span></span> <span data-ttu-id="28497-120">Wenn Sie von der Anwendung nicht bereitgestellt wird, verwendet das System das vom systemgenerierte Symbol für dieses Fenster.</span><span class="sxs-lookup"><span data-stu-id="28497-120">If the application does not provide one, the system uses the system-generated icon for that window.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="28497-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28497-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28497-122">Der dpi-für das Symbol, das abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="28497-122">The DPI of the icon being retrieved.</span></span> <span data-ttu-id="28497-123">Dies kann verwendet werden, um verschiedene Symbole abhängig von der Symbolgröße bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="28497-123">This can be used to provide different icons depending on the icon size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28497-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28497-124">Return value</span></span>

<span data-ttu-id="28497-125">Typ: **HICON**</span><span class="sxs-lookup"><span data-stu-id="28497-125">Type: **HICON**</span></span>

<span data-ttu-id="28497-126">Der Rückgabewert ist ein Handle für das große oder kleine Symbol, abhängig vom Wert von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="28497-126">The return value is a handle to the large or small icon, depending on the value of *wParam*.</span></span> <span data-ttu-id="28497-127">Wenn eine Anwendung diese Nachricht empfängt, kann Sie ein Handle an ein großes oder ein kleines Symbol zurückgeben oder die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="28497-127">When an application receives this message, it can return a handle to a large or small icon, or pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="28497-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28497-128">Remarks</span></span>

<span data-ttu-id="28497-129">Wenn eine Anwendung diese Nachricht empfängt, kann Sie ein Handle an ein großes oder ein kleines Symbol zurückgeben oder die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.</span><span class="sxs-lookup"><span data-stu-id="28497-129">When an application receives this message, it can return a handle to a large or small icon, or pass the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="28497-130">[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt ein Handle für das große oder kleine Symbol zurück, das dem Fenster zugeordnet ist, je nach Wert von *wParam*.</span><span class="sxs-lookup"><span data-stu-id="28497-130">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) returns a handle to the large or small icon associated with the window, depending on the value of *wParam*.</span></span>

<span data-ttu-id="28497-131">Ein Fenster, für das kein Symbol explizit festgelegt ist (mit **WM \_ SetIcon**), verwendet das Symbol für die registrierte Fenster Klasse, und in diesem Fall gibt [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 0 für eine **WM- \_ GetIcon** -Nachricht zurück.</span><span class="sxs-lookup"><span data-stu-id="28497-131">A window that has no icon explicitly set (with **WM\_SETICON**) uses the icon for the registered window class, and in this case [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) will return 0 for a **WM\_GETICON** message.</span></span> <span data-ttu-id="28497-132">Wenn das Senden einer **WM- \_ GetIcon** -Nachricht an ein Fenster 0 zurückgibt, rufen Sie als nächstes die [**getclasslongptr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) -Funktion für das Fenster auf.</span><span class="sxs-lookup"><span data-stu-id="28497-132">If sending a **WM\_GETICON** message to a window returns 0, next try calling the [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) function for the window.</span></span> <span data-ttu-id="28497-133">Wenn der Wert 0 zurückgibt, versuchen Sie es mit der [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="28497-133">If that returns 0 then try the [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28497-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28497-134">Requirements</span></span>



| <span data-ttu-id="28497-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28497-135">Requirement</span></span> | <span data-ttu-id="28497-136">Wert</span><span class="sxs-lookup"><span data-stu-id="28497-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28497-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28497-137">Minimum supported client</span></span><br/> | <span data-ttu-id="28497-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28497-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28497-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28497-139">Minimum supported server</span></span><br/> | <span data-ttu-id="28497-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28497-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28497-141">Header</span><span class="sxs-lookup"><span data-stu-id="28497-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="28497-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="28497-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28497-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28497-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="28497-144">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="28497-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28497-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="28497-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="28497-146">**WM \_ -Ziel**</span><span class="sxs-lookup"><span data-stu-id="28497-146">**WM\_SETICON**</span></span>](wm-seticon.md)
</dt> <dt>

<span data-ttu-id="28497-147">**Licher**</span><span class="sxs-lookup"><span data-stu-id="28497-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28497-148">Windows</span><span class="sxs-lookup"><span data-stu-id="28497-148">Windows</span></span>](windows.md)
</dt> </dl>

 

 
