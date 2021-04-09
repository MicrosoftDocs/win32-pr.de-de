---
description: Wird an ein Fenster gesendet, wenn die SetWindowLong-Funktion im Begriff ist, mindestens einen Stil des Fensters zu ändern.
ms.assetid: 71034362-3f67-49ae-bbbf-d38853ababb3
title: WM_STYLECHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e587797404bb361a443a60750d4de5ea6a8924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865235"
---
# <a name="wm_stylechanging-message"></a><span data-ttu-id="138c6-103">WM- \_ stylechanging-Meldung</span><span class="sxs-lookup"><span data-stu-id="138c6-103">WM\_STYLECHANGING message</span></span>

<span data-ttu-id="138c6-104">Wird an ein Fenster gesendet, wenn die [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion im Begriff ist, mindestens einen Stil des Fensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="138c6-104">Sent to a window when the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function is about to change one or more of the window's styles.</span></span>

<span data-ttu-id="138c6-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="138c6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_STYLECHANGING                0x007C
```



## <a name="parameters"></a><span data-ttu-id="138c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="138c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="138c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="138c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="138c6-108">Gibt an, ob die Stile des Fensters oder erweiterte Fenster Stile geändert werden.</span><span class="sxs-lookup"><span data-stu-id="138c6-108">Indicates whether the window's styles or extended window styles are changing.</span></span> <span data-ttu-id="138c6-109">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="138c6-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="138c6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="138c6-110">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="138c6-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="138c6-111">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="GWL_EXSTYLE"></span><span id="gwl_exstyle"></span><dl> <span data-ttu-id="138c6-112"><dt>**GWL \_ ExStyle**</dt> <dt>-20</dt></span><span class="sxs-lookup"><span data-stu-id="138c6-112"><dt>**GWL\_EXSTYLE**</dt> <dt>-20</dt></span></span> </dl> | <span data-ttu-id="138c6-113">Die erweiterten Fenster Stile werden geändert.</span><span class="sxs-lookup"><span data-stu-id="138c6-113">The extended window styles are changing.</span></span><br/> |
| <span id="GWL_STYLE"></span><span id="gwl_style"></span><dl> <span data-ttu-id="138c6-114"><dt>**GWL \_ Style**</dt> <dt>-16</dt></span><span class="sxs-lookup"><span data-stu-id="138c6-114"><dt>**GWL\_STYLE**</dt> <dt>-16</dt></span></span> </dl>       | <span data-ttu-id="138c6-115">Die Fenster Stile werden geändert.</span><span class="sxs-lookup"><span data-stu-id="138c6-115">The window styles are changing.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="138c6-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="138c6-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="138c6-117">Ein Zeiger auf eine [**stylestruct**](/windows/win32/api/winuser/ns-winuser-stylestruct) -Struktur, die die vorgeschlagenen neuen Stile für das Fenster enthält.</span><span class="sxs-lookup"><span data-stu-id="138c6-117">A pointer to a [**STYLESTRUCT**](/windows/win32/api/winuser/ns-winuser-stylestruct) structure that contains the proposed new styles for the window.</span></span> <span data-ttu-id="138c6-118">Eine Anwendung kann die Stile untersuchen und ggf. ändern.</span><span class="sxs-lookup"><span data-stu-id="138c6-118">An application can examine the styles and, if necessary, change them.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="138c6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="138c6-119">Return value</span></span>

<span data-ttu-id="138c6-120">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="138c6-120">Type: **LRESULT**</span></span>

<span data-ttu-id="138c6-121">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="138c6-121">An application should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="138c6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="138c6-122">Requirements</span></span>



| <span data-ttu-id="138c6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="138c6-123">Requirement</span></span> | <span data-ttu-id="138c6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="138c6-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="138c6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="138c6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="138c6-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="138c6-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="138c6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="138c6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="138c6-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="138c6-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="138c6-129">Header</span><span class="sxs-lookup"><span data-stu-id="138c6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="138c6-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="138c6-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="138c6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="138c6-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="138c6-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="138c6-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="138c6-133">**Stylestruct**</span><span class="sxs-lookup"><span data-stu-id="138c6-133">**STYLESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-stylestruct)
</dt> <dt>

[<span data-ttu-id="138c6-134">**WM- \_ StyleChanged**</span><span class="sxs-lookup"><span data-stu-id="138c6-134">**WM\_STYLECHANGED**</span></span>](wm-stylechanged.md)
</dt> <dt>

<span data-ttu-id="138c6-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="138c6-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="138c6-136">Windows</span><span class="sxs-lookup"><span data-stu-id="138c6-136">Windows</span></span>](windows.md)
</dt> </dl>

 

 
