---
title: WM_PAINTCLIPBOARD Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF \_ -Besitzer Anzeige Format enthält und der Client Bereich der Zwischenablage-Viewer neu gezeichnet werden muss.
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- WM_PAINTCLIPBOARD Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339324"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="5c290-104">WM- \_ paintclipboard-Meldung</span><span class="sxs-lookup"><span data-stu-id="5c290-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="5c290-105">Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, wenn die Zwischenablage Daten im CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Format enthält und der Client Bereich der Zwischenablage-Viewer neu gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="5c290-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="5c290-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c290-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c290-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c290-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c290-108">Ein Handle für das Fenster der Zwischenablage Anzeige.</span><span class="sxs-lookup"><span data-stu-id="5c290-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="5c290-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c290-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c290-110">Ein Handle für ein globales Speicher Objekt, das eine [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="5c290-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="5c290-111">Die-Struktur definiert den zu zeichnenden Teil des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5c290-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c290-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c290-112">Return value</span></span>

<span data-ttu-id="5c290-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5c290-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c290-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c290-114">Remarks</span></span>

<span data-ttu-id="5c290-115">Um zu ermitteln, ob der gesamte Client Bereich oder nur ein Teil davon neu gezeichnet werden muss, muss der Besitzer der Zwischenablage die Dimensionen des Zeichnungs Bereichs im **rcpaint** -Member von [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) mit den Dimensionen vergleichen, die in der letzten [**WM- \_ sizeclipboard**](wm-sizeclipboard.md) -Meldung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="5c290-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="5c290-116">Der Besitzer der Zwischenablage muss die [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) -Funktion verwenden, um den Arbeitsspeicher zu sperren, der die [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="5c290-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="5c290-117">Vor der Rückgabe muss der Besitzer der Zwischenablage diesen Speicher mithilfe der [**globalunlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) -Funktion entsperren.</span><span class="sxs-lookup"><span data-stu-id="5c290-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c290-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c290-118">Requirements</span></span>



| <span data-ttu-id="5c290-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c290-119">Requirement</span></span> | <span data-ttu-id="5c290-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5c290-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c290-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c290-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c290-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c290-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c290-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c290-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c290-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c290-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5c290-125">Header</span><span class="sxs-lookup"><span data-stu-id="5c290-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c290-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5c290-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c290-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c290-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c290-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5c290-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c290-129">**WM- \_ sizeclipboard**</span><span class="sxs-lookup"><span data-stu-id="5c290-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="5c290-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="5c290-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c290-131">Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="5c290-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

