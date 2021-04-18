---
title: WM_INITMENU Meldung (Winuser. h)
description: Wird gesendet, wenn ein Menü aktiv wird.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340007"
---
# <a name="wm_initmenu-message"></a><span data-ttu-id="07c29-104">WM- \_ InitMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="07c29-104">WM\_INITMENU message</span></span>

<span data-ttu-id="07c29-105">Wird gesendet, wenn ein Menü aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="07c29-105">Sent when a menu is about to become active.</span></span> <span data-ttu-id="07c29-106">Sie tritt auf, wenn der Benutzer auf ein Element in der Menüleiste klickt oder eine Menü Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="07c29-106">It occurs when the user clicks an item on the menu bar or presses a menu key.</span></span> <span data-ttu-id="07c29-107">Dadurch kann die Anwendung das Menü ändern, bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="07c29-107">This allows the application to modify the menu before it is displayed.</span></span>

<span data-ttu-id="07c29-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="07c29-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a><span data-ttu-id="07c29-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="07c29-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c29-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07c29-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07c29-111">Ein Handle für das Menü, das initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="07c29-111">A handle to the menu to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="07c29-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07c29-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07c29-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="07c29-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c29-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07c29-114">Return value</span></span>

<span data-ttu-id="07c29-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="07c29-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c29-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07c29-116">Remarks</span></span>

<span data-ttu-id="07c29-117">Eine **WM- \_ InitMenu** -Meldung wird nur gesendet, wenn zum ersten Mal auf ein Menü zugegriffen wird. für jeden Zugriff wird nur eine **WM- \_ InitMenu** -Nachricht generiert.</span><span class="sxs-lookup"><span data-stu-id="07c29-117">A **WM\_INITMENU** message is sent only when a menu is first accessed; only one **WM\_INITMENU** message is generated for each access.</span></span> <span data-ttu-id="07c29-118">Wenn Sie die Maus z. b. über mehrere Menü Elemente bewegen, während Sie die Schaltfläche gedrückt halten, werden keine neuen Nachrichten generiert.</span><span class="sxs-lookup"><span data-stu-id="07c29-118">For example, moving the mouse across several menu items while holding down the button does not generate new messages.</span></span> <span data-ttu-id="07c29-119">**WM \_ InitMenu** bietet keine Informationen zu Menü Elementen.</span><span class="sxs-lookup"><span data-stu-id="07c29-119">**WM\_INITMENU** does not provide information about menu items.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c29-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07c29-120">Requirements</span></span>



| <span data-ttu-id="07c29-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07c29-121">Requirement</span></span> | <span data-ttu-id="07c29-122">Wert</span><span class="sxs-lookup"><span data-stu-id="07c29-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c29-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07c29-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07c29-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c29-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="07c29-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07c29-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07c29-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07c29-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="07c29-127">Header</span><span class="sxs-lookup"><span data-stu-id="07c29-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c29-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="07c29-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c29-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07c29-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="07c29-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="07c29-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="07c29-131">**WM \_ initmenupopup**</span><span class="sxs-lookup"><span data-stu-id="07c29-131">**WM\_INITMENUPOPUP**</span></span>](wm-initmenupopup.md)
</dt> <dt>

<span data-ttu-id="07c29-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="07c29-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="07c29-133">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="07c29-133">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

