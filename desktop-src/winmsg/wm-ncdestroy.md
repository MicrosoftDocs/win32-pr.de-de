---
description: Benachrichtigt ein Fenster, dass sein nicht-Client Bereich zerstört wird. Die DestroyWindow-Funktion sendet die WM \_ ncdestroy-Meldung an das Fenster nach der WM-Lösch \_ Nachricht.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959812"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="b5c7e-104">WM- \_ ncdestroy-Meldung</span><span class="sxs-lookup"><span data-stu-id="b5c7e-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="b5c7e-105">Benachrichtigt ein Fenster, dass sein nicht-Client Bereich zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="b5c7e-106">Die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion sendet die **WM \_ ncdestroy** -Meldung an das Fenster nach der WM-Lösch Nachricht. [**\_**](wm-destroy.md) [**Die WM- \_ Zerstörung**](wm-destroy.md) wird verwendet, um das zugeordnete Speicher Objekt freizugeben, das dem Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="b5c7e-107">Die **WM \_ ncdestroy** -Nachricht wird gesendet, nachdem die untergeordneten Fenster zerstört wurden.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="b5c7e-108">Im Gegensatz dazu wird die [**WM- \_ Zerstörung**](wm-destroy.md) gesendet, bevor die untergeordneten Fenster zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="b5c7e-109">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="b5c7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5c7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5c7e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5c7e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5c7e-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5c7e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5c7e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5c7e-114">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5c7e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5c7e-115">Return value</span></span>

<span data-ttu-id="b5c7e-116">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-116">Type: **LRESULT**</span></span>

<span data-ttu-id="b5c7e-117">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c7e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5c7e-118">Remarks</span></span>

<span data-ttu-id="b5c7e-119">Diese Meldung gibt den Arbeitsspeicher frei, der intern für das Fenster reserviert wurde.</span><span class="sxs-lookup"><span data-stu-id="b5c7e-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c7e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5c7e-120">Requirements</span></span>



| <span data-ttu-id="b5c7e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5c7e-121">Requirement</span></span> | <span data-ttu-id="b5c7e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b5c7e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c7e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5c7e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b5c7e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5c7e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b5c7e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5c7e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b5c7e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5c7e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b5c7e-127">Header</span><span class="sxs-lookup"><span data-stu-id="b5c7e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5c7e-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c7e-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c7e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5c7e-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5c7e-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5c7e-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="b5c7e-132">**WM \_ zerstören**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="b5c7e-133">**WM- \_ nccreate**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="b5c7e-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b5c7e-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b5c7e-135">Windows</span><span class="sxs-lookup"><span data-stu-id="b5c7e-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
