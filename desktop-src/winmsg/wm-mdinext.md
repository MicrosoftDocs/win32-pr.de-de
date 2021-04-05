---
description: Eine Anwendung sendet die WM- \_ mdinext-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.
ms.assetid: a4822b99-330a-4094-bad9-b9a5923e02a8
title: WM_MDINEXT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e0af031c11ea37129e1405e31b07b18f023b7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751208"
---
# <a name="wm_mdinext-message"></a><span data-ttu-id="c7b2f-103">WM- \_ mdinext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c7b2f-103">WM\_MDINEXT message</span></span>

<span data-ttu-id="c7b2f-104">Eine Anwendung sendet die **WM- \_ mdinext** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um das nächste oder vorherige untergeordnete Fenster zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-104">An application sends the **WM\_MDINEXT** message to a multiple-document interface (MDI) client window to activate the next or previous child window.</span></span>


```C++
#define WM_MDINEXT                      0x0224
```



## <a name="parameters"></a><span data-ttu-id="c7b2f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7b2f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b2f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7b2f-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b2f-107">Ein Handle für das untergeordnete MDI-Fenster.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-107">A handle to the MDI child window.</span></span> <span data-ttu-id="c7b2f-108">Das System aktiviert das untergeordnete Fenster direkt vor oder nach dem angegebenen untergeordneten Fenster, abhängig vom Wert des *LPARAM* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-108">The system activates the child window that is immediately before or after the specified child window, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="c7b2f-109">Wenn der *wParam* -Parameter **null** ist, aktiviert das System das untergeordnete Fenster, das unmittelbar vor oder nach dem momentan aktiven untergeordneten Fenster liegt.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-109">If the *wParam* parameter is **NULL**, the system activates the child window that is immediately before or after the currently active child window.</span></span>

</dd> <dt>

<span data-ttu-id="c7b2f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7b2f-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b2f-111">Wenn dieser Parameter NULL ist, aktiviert das System das nächste untergeordnete MDI-Fenster und platziert das untergeordnete Fenster, das durch den *wParam* -Parameter identifiziert wird, hinter allen anderen untergeordneten Fenstern.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-111">If this parameter is zero, the system activates the next MDI child window and places the child window identified by the *wParam* parameter behind all other child windows.</span></span> <span data-ttu-id="c7b2f-112">Wenn dieser Parameter ungleich NULL ist, aktiviert das System das vorherige untergeordnete Fenster und platziert es vor dem durch *wParam* identifizierten untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-112">If this parameter is nonzero, the system activates the previous child window, placing it in front of the child window identified by *wParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b2f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7b2f-113">Return value</span></span>

<span data-ttu-id="c7b2f-114">Typ: **null**</span><span class="sxs-lookup"><span data-stu-id="c7b2f-114">Type: **zero**</span></span>

<span data-ttu-id="c7b2f-115">Der Rückgabewert ist immer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="c7b2f-115">The return value is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b2f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7b2f-116">Remarks</span></span>

<span data-ttu-id="c7b2f-117">Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="c7b2f-117">If an MDI client window receives any message that changes the activation of its child windows while the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b2f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7b2f-118">Requirements</span></span>



| <span data-ttu-id="c7b2f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7b2f-119">Requirement</span></span> | <span data-ttu-id="c7b2f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c7b2f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b2f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7b2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b2f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7b2f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c7b2f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7b2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b2f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7b2f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7b2f-125">Header</span><span class="sxs-lookup"><span data-stu-id="c7b2f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7b2f-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c7b2f-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b2f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7b2f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7b2f-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c7b2f-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c7b2f-129">**WM- \_ mdiaktivierung**</span><span class="sxs-lookup"><span data-stu-id="c7b2f-129">**WM\_MDIACTIVATE**</span></span>](wm-mdiactivate.md)
</dt> <dt>

[<span data-ttu-id="c7b2f-130">**WM- \_ mdigetactive**</span><span class="sxs-lookup"><span data-stu-id="c7b2f-130">**WM\_MDIGETACTIVE**</span></span>](wm-mdigetactive.md)
</dt> <dt>

<span data-ttu-id="c7b2f-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c7b2f-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c7b2f-132">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c7b2f-132">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




