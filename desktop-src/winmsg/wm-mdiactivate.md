---
description: Eine Anwendung sendet die WM- \_ mdiaktivierungs-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Client Fenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.
ms.assetid: c5de18b5-fac3-4e55-9eca-3b6672df0e7b
title: WM_MDIACTIVATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b240c41d3b7127a5d69b855f3a5587e194b02d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367953"
---
# <a name="wm_mdiactivate-message"></a><span data-ttu-id="9c452-103">WM- \_ mdiaktivierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="9c452-103">WM\_MDIACTIVATE message</span></span>

<span data-ttu-id="9c452-104">Eine Anwendung sendet die **WM- \_ mdiaktivierungs** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um das Client Fenster anzuweisen, ein anderes untergeordnetes MDI-Fenster zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9c452-104">An application sends the **WM\_MDIACTIVATE** message to a multiple-document interface (MDI) client window to instruct the client window to activate a different MDI child window.</span></span>


```C++
#define WM_MDIACTIVATE                  0x0222
```



## <a name="parameters"></a><span data-ttu-id="9c452-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c452-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c452-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c452-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c452-107">Ein Handle für das untergeordnete MDI-Fenster, das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c452-107">A handle to the MDI child window to be activated.</span></span>

</dd> <dt>

<span data-ttu-id="9c452-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c452-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c452-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c452-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c452-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c452-110">Return value</span></span>

<span data-ttu-id="9c452-111">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="9c452-111">Type: **LRESULT**</span></span>

<span data-ttu-id="9c452-112">Wenn eine Anwendung diese Nachricht an ein MDI-Client Fenster sendet, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9c452-112">If an application sends this message to an MDI client window, the return value is zero.</span></span>

<span data-ttu-id="9c452-113">Ein untergeordnetes MDI-Fenster sollte NULL zurückgeben, wenn es diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9c452-113">An MDI child window should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c452-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c452-114">Remarks</span></span>

<span data-ttu-id="9c452-115">Wenn das Client Fenster diese Nachricht verarbeitet, sendet es die **WM- \_ mdiaktivierung** an das untergeordnete Fenster, das deaktiviert wird, und an das untergeordnete Fenster, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9c452-115">As the client window processes this message, it sends **WM\_MDIACTIVATE** to the child window being deactivated and to the child window being activated.</span></span> <span data-ttu-id="9c452-116">Die von einem untergeordneten MDI-Fenster empfangenen Nachrichten Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9c452-116">The message parameters received by an MDI child window are as follows:</span></span>

<dl> <dt>

<span data-ttu-id="9c452-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c452-117"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="9c452-118">Ein Handle für das untergeordnete MDI-Fenster, das deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9c452-118">A handle to the MDI child window being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="9c452-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="9c452-119"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9c452-120">Ein Handle für das untergeordnete MDI-Fenster, das aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="9c452-120">A handle to the MDI child window being activated.</span></span>

</dd> </dl>

<span data-ttu-id="9c452-121">Ein untergeordnetes MDI-Fenster wird unabhängig vom MDI-Rahmen Fenster aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9c452-121">An MDI child window is activated independently of the MDI frame window.</span></span> <span data-ttu-id="9c452-122">Wenn das Rahmen Fenster aktiv wird, empfängt das untergeordnete Fenster, das zuletzt mithilfe der " **WM \_ mdiaktivierungs** "-Meldung aktiviert wurde, die [**WM- \_ ncaktivierungs**](wm-ncactivate.md) Nachricht, um einen aktiven Fensterrahmen und eine Titelleiste zu zeichnen. das untergeordnete Fenster empfängt keine weitere **WM- \_ mdiaktivierungs** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9c452-122">When the frame window becomes active, the child window last activated by using the **WM\_MDIACTIVATE** message receives the [**WM\_NCACTIVATE**](wm-ncactivate.md) message to draw an active window frame and title bar; the child window does not receive another **WM\_MDIACTIVATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c452-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c452-123">Requirements</span></span>



| <span data-ttu-id="9c452-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c452-124">Requirement</span></span> | <span data-ttu-id="9c452-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9c452-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c452-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c452-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9c452-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c452-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c452-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c452-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9c452-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c452-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c452-130">Header</span><span class="sxs-lookup"><span data-stu-id="9c452-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c452-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9c452-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c452-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c452-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c452-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9c452-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c452-134">**WM- \_ mdigetactive**</span><span class="sxs-lookup"><span data-stu-id="9c452-134">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

[<span data-ttu-id="9c452-135">**WM- \_ mdinext**</span><span class="sxs-lookup"><span data-stu-id="9c452-135">**WM\_MDINEXT**</span></span>](wm-mdinext.md)
</dt> <dt>

[<span data-ttu-id="9c452-136">**WM- \_ ncaktivierung**</span><span class="sxs-lookup"><span data-stu-id="9c452-136">**WM\_NCACTIVATE**</span></span>](wm-ncactivate.md)
</dt> <dt>

<span data-ttu-id="9c452-137">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9c452-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c452-138">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9c452-138">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




