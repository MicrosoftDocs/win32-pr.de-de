---
description: Eine Anwendung sendet die WM- \_ mdidestroy-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.
ms.assetid: b415393d-a5c2-4b70-af18-0dc7b3939a47
title: WM_MDIDESTROY Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edea8fe8dadc691ca912df4e9ee5d57421124bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751209"
---
# <a name="wm_mdidestroy-message"></a><span data-ttu-id="9ab08-103">WM- \_ mdidestroy-Meldung</span><span class="sxs-lookup"><span data-stu-id="9ab08-103">WM\_MDIDESTROY message</span></span>

<span data-ttu-id="9ab08-104">Eine Anwendung sendet die **WM- \_ mdidestroy** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9ab08-104">An application sends the **WM\_MDIDESTROY** message to a multiple-document interface (MDI) client window to close an MDI child window.</span></span>


```C++
#define WM_MDIDESTROY                   0x0221
```



## <a name="parameters"></a><span data-ttu-id="9ab08-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ab08-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab08-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ab08-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab08-107">Ein Handle für das untergeordnete MDI-Fenster, das geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ab08-107">A handle to the MDI child window to be closed.</span></span>

</dd> <dt>

<span data-ttu-id="9ab08-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ab08-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ab08-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ab08-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ab08-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ab08-110">Return value</span></span>

<span data-ttu-id="9ab08-111">Typ: **null**</span><span class="sxs-lookup"><span data-stu-id="9ab08-111">Type: **zero**</span></span>

<span data-ttu-id="9ab08-112">Diese Meldung gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="9ab08-112">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab08-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ab08-113">Remarks</span></span>

<span data-ttu-id="9ab08-114">Diese Meldung entfernt den Titel des untergeordneten MDI-Fensters aus dem MDI-Rahmen Fenster und deaktiviert das untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="9ab08-114">This message removes the title of the MDI child window from the MDI frame window and deactivates the child window.</span></span> <span data-ttu-id="9ab08-115">Eine Anwendung sollte diese Nachricht verwenden, um alle untergeordneten MDI-Fenster zu schließen.</span><span class="sxs-lookup"><span data-stu-id="9ab08-115">An application should use this message to close all MDI child windows.</span></span>

<span data-ttu-id="9ab08-116">Wenn ein MDI-Client Fenster eine Meldung empfängt, mit der die Aktivierung der untergeordneten Fenster geändert wird, und das aktive untergeordnete MDI-Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="9ab08-116">If an MDI client window receives a message that changes the activation of its child windows and the active MDI child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab08-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ab08-117">Requirements</span></span>



| <span data-ttu-id="9ab08-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ab08-118">Requirement</span></span> | <span data-ttu-id="9ab08-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9ab08-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab08-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ab08-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab08-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ab08-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ab08-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ab08-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab08-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ab08-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9ab08-124">Header</span><span class="sxs-lookup"><span data-stu-id="9ab08-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab08-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9ab08-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ab08-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ab08-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ab08-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9ab08-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ab08-128">**WM- \_ mdicreate**</span><span class="sxs-lookup"><span data-stu-id="9ab08-128">**WM\_MDICREATE**</span></span>](wm-mdicreate.md)
</dt> <dt>

<span data-ttu-id="9ab08-129">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9ab08-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ab08-130">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9ab08-130">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




