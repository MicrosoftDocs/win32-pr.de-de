---
description: Wird an ein Fenster gesendet, das der Benutzer verschiebt. Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Zieh Rechtecks überwachen und ggf. ihre Position ändern.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: WM_MOVING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346101"
---
# <a name="wm_moving-message"></a><span data-ttu-id="de528-104">WM-Verschiebungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="de528-104">WM\_MOVING message</span></span>

<span data-ttu-id="de528-105">Wird an ein Fenster gesendet, das der Benutzer verschiebt.</span><span class="sxs-lookup"><span data-stu-id="de528-105">Sent to a window that the user is moving.</span></span> <span data-ttu-id="de528-106">Durch die Verarbeitung dieser Nachricht kann eine Anwendung die Position des Zieh Rechtecks überwachen und ggf. ihre Position ändern.</span><span class="sxs-lookup"><span data-stu-id="de528-106">By processing this message, an application can monitor the position of the drag rectangle and, if needed, change its position.</span></span>

<span data-ttu-id="de528-107">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="de528-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a><span data-ttu-id="de528-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de528-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de528-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="de528-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de528-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="de528-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="de528-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de528-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de528-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit der aktuellen Position des Fensters in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="de528-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the current position of the window, in screen coordinates.</span></span> <span data-ttu-id="de528-113">Um die Position des Zieh Rechtecks zu ändern, muss eine Anwendung die Elemente dieser Struktur ändern.</span><span class="sxs-lookup"><span data-stu-id="de528-113">To change the position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de528-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de528-114">Return value</span></span>

<span data-ttu-id="de528-115">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="de528-115">Type: **LRESULT**</span></span>

<span data-ttu-id="de528-116">Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="de528-116">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de528-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de528-117">Requirements</span></span>



| <span data-ttu-id="de528-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de528-118">Requirement</span></span> | <span data-ttu-id="de528-119">Wert</span><span class="sxs-lookup"><span data-stu-id="de528-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de528-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de528-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de528-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de528-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="de528-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de528-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de528-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de528-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de528-124">Header</span><span class="sxs-lookup"><span data-stu-id="de528-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de528-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="de528-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de528-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de528-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="de528-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="de528-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="de528-128">**WM \_ verschieben**</span><span class="sxs-lookup"><span data-stu-id="de528-128">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="de528-129">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="de528-129">**WM\_SIZING**</span></span>](wm-sizing.md)
</dt> <dt>

<span data-ttu-id="de528-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="de528-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="de528-131">Windows</span><span class="sxs-lookup"><span data-stu-id="de528-131">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="de528-132">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="de528-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="de528-133">[**Rect**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de528-133">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
