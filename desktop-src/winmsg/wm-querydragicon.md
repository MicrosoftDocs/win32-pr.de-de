---
description: Wird an ein minimiertes (legendäres) Fenster gesendet.
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: WM_QUERYDRAGICON Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345579"
---
# <a name="wm_querydragicon-message"></a><span data-ttu-id="a05b9-103">WM \_ querydragicon-Meldung</span><span class="sxs-lookup"><span data-stu-id="a05b9-103">WM\_QUERYDRAGICON message</span></span>

<span data-ttu-id="a05b9-104">Wird an ein minimiertes (legendäres) Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="a05b9-104">Sent to a minimized (iconic) window.</span></span> <span data-ttu-id="a05b9-105">Das Fenster wird vom Benutzer gezogen, aber es ist kein Symbol für seine Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="a05b9-105">The window is about to be dragged by the user but does not have an icon defined for its class.</span></span> <span data-ttu-id="a05b9-106">Eine Anwendung kann ein Handle für ein Symbol oder einen Cursor zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a05b9-106">An application can return a handle to an icon or cursor.</span></span> <span data-ttu-id="a05b9-107">Das System zeigt diesen Cursor oder dieses Symbol an, während der Benutzer das Symbol zieht.</span><span class="sxs-lookup"><span data-stu-id="a05b9-107">The system displays this cursor or icon while the user drags the icon.</span></span>

<span data-ttu-id="a05b9-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a05b9-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a><span data-ttu-id="a05b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a05b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05b9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a05b9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a05b9-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a05b9-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a05b9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a05b9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a05b9-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a05b9-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05b9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a05b9-114">Return value</span></span>

<span data-ttu-id="a05b9-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="a05b9-115">Type: **LRESULT**</span></span>

<span data-ttu-id="a05b9-116">Eine Anwendung sollte ein Handle für einen Cursor oder ein Symbol zurückgeben, den das System anzeigen soll, während der Benutzer das Symbol zieht.</span><span class="sxs-lookup"><span data-stu-id="a05b9-116">An application should return a handle to a cursor or icon that the system is to display while the user drags the icon.</span></span> <span data-ttu-id="a05b9-117">Der Cursor oder das Symbol muss mit der Auflösung des Anzeige Treibers kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="a05b9-117">The cursor or icon must be compatible with the display driver's resolution.</span></span> <span data-ttu-id="a05b9-118">Wenn die Anwendung **null** zurückgibt, zeigt das System den Standard Cursor an.</span><span class="sxs-lookup"><span data-stu-id="a05b9-118">If the application returns **NULL**, the system displays the default cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05b9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a05b9-119">Remarks</span></span>

<span data-ttu-id="a05b9-120">Wenn der Benutzer das Symbol eines Fensters ohne ein Klassen Symbol zieht, ersetzt das System das Symbol durch einen Standard Cursor.</span><span class="sxs-lookup"><span data-stu-id="a05b9-120">When the user drags the icon of a window without a class icon, the system replaces the icon with a default cursor.</span></span> <span data-ttu-id="a05b9-121">Wenn die Anwendung erfordert, dass während des Zieh Punkts ein anderer Cursor angezeigt wird, muss ein Handle für den Cursor oder das Symbol zurückgegeben werden, das mit der Auflösung des Anzeige Treibers kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="a05b9-121">If the application requires a different cursor to be displayed during dragging, it must return a handle to the cursor or icon compatible with the display driver's resolution.</span></span> <span data-ttu-id="a05b9-122">Wenn eine Anwendung ein Handle für einen Farb Cursor oder ein Symbol zurückgibt, konvertiert das System den Cursor oder das Symbol in schwarz und weiß.</span><span class="sxs-lookup"><span data-stu-id="a05b9-122">If an application returns a handle to a color cursor or icon, the system converts the cursor or icon to black and white.</span></span> <span data-ttu-id="a05b9-123">Die Anwendung kann die [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) -oder [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) -Funktion aufrufen, um einen Cursor oder ein Symbol aus den Ressourcen in der ausführbaren Datei (. exe) zu laden und dieses Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a05b9-123">The application can call the [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) or [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) function to load a cursor or icon from the resources in its executable (.exe) file and to retrieve this handle.</span></span>

<span data-ttu-id="a05b9-124">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a05b9-124">If a dialog box procedure handles this message, it should cast the desired return value to a **BOOL** and return the value directly.</span></span> <span data-ttu-id="a05b9-125">Der von der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a05b9-125">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="a05b9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a05b9-126">Requirements</span></span>



| <span data-ttu-id="a05b9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a05b9-127">Requirement</span></span> | <span data-ttu-id="a05b9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a05b9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a05b9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a05b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a05b9-130">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a05b9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a05b9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a05b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a05b9-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a05b9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a05b9-133">Header</span><span class="sxs-lookup"><span data-stu-id="a05b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a05b9-134"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a05b9-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a05b9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a05b9-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a05b9-136">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a05b9-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a05b9-137">**LoadCursor**</span><span class="sxs-lookup"><span data-stu-id="a05b9-137">**LoadCursor**</span></span>](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[<span data-ttu-id="a05b9-138">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="a05b9-138">**LoadIcon**</span></span>](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

<span data-ttu-id="a05b9-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a05b9-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a05b9-140">Windows</span><span class="sxs-lookup"><span data-stu-id="a05b9-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
