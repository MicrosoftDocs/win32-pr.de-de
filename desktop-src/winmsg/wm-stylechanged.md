---
description: Wird an ein Fenster gesendet, nachdem die Funktion SetWindowLong mindestens einen Stil des Fensters geändert hat.
ms.assetid: 37bc4e1a-f75d-4851-8dee-97fa2da90254
title: WM_STYLECHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5429db06dea95dbbc003e432a2b619c5cf8d056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529834"
---
# <a name="wm_stylechanged-message"></a><span data-ttu-id="9874a-103">Meldung "WM- \_ StyleChanged"</span><span class="sxs-lookup"><span data-stu-id="9874a-103">WM\_STYLECHANGED message</span></span>

<span data-ttu-id="9874a-104">Wird an ein Fenster gesendet, nachdem die Funktion [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) mindestens einen Stil des Fensters geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9874a-104">Sent to a window after the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function has changed one or more of the window's styles.</span></span>

<span data-ttu-id="9874a-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9874a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGED                 0x007D
```



## <a name="parameters"></a><span data-ttu-id="9874a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9874a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9874a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9874a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9874a-108">Gibt an, ob die Stile des Fensters oder erweiterte Fenster Stile geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="9874a-108">Indicates whether the window's styles or extended window styles have changed.</span></span> <span data-ttu-id="9874a-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9874a-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9874a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9874a-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="9874a-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9874a-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="9874a-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="9874a-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="9874a-113">Die erweiterten Fenster Stile wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="9874a-113">The extended window styles have changed.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="9874a-114"><dt>**GWL \_ Style**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="9874a-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="9874a-115">Die Fenster Stile wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="9874a-115">The window styles have changed.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="9874a-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9874a-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9874a-117">Ein Zeiger auf eine [**stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct) -Struktur, die die neuen Stile für das Fenster enthält.</span><span class="sxs-lookup"><span data-stu-id="9874a-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the new styles for the window.</span></span> <span data-ttu-id="9874a-118">Eine Anwendung kann die Stile untersuchen, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9874a-118">An application can examine the styles, but cannot change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9874a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9874a-119">Return value</span></span>

<span data-ttu-id="9874a-120">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9874a-120">Type: **LRESULT**</span></span>

<span data-ttu-id="9874a-121">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9874a-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9874a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9874a-122">Requirements</span></span>



| <span data-ttu-id="9874a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9874a-123">Requirement</span></span> | <span data-ttu-id="9874a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9874a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9874a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9874a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9874a-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9874a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9874a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9874a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9874a-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9874a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9874a-129">Header</span><span class="sxs-lookup"><span data-stu-id="9874a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9874a-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9874a-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9874a-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9874a-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="9874a-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9874a-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9874a-133">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="9874a-133">**SetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

[<span data-ttu-id="9874a-134">**Stylestruct**</span><span class="sxs-lookup"><span data-stu-id="9874a-134">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="9874a-135">**WM- \_ stylechanging**</span><span class="sxs-lookup"><span data-stu-id="9874a-135">**WM\_STYLECHANGING**</span></span>](wm-stylechanging.md)
</dt> <dt>

<span data-ttu-id="9874a-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9874a-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9874a-137">Windows</span><span class="sxs-lookup"><span data-stu-id="9874a-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
