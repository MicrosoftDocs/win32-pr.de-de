---
description: Eine Anwendung sendet die WM- \_ mdicreate-Meldung an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: WM_MDICREATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362597"
---
# <a name="wm_mdicreate-message"></a><span data-ttu-id="8c88a-103">WM- \_ mdicreate-Meldung</span><span class="sxs-lookup"><span data-stu-id="8c88a-103">WM\_MDICREATE message</span></span>

<span data-ttu-id="8c88a-104">Eine Anwendung sendet die **WM- \_ mdicreate** -Meldung an ein MDI-Client Fenster (Multiple Document Interface), um ein untergeordnetes MDI-Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c88a-104">An application sends the **WM\_MDICREATE** message to a multiple-document interface (MDI) client window to create an MDI child window.</span></span>


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a><span data-ttu-id="8c88a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c88a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c88a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c88a-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c88a-107">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c88a-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8c88a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c88a-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c88a-109">Ein Zeiger auf eine [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur, die Informationen enthält, die das System verwendet, um das untergeordnete MDI-Fenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c88a-109">A pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure containing information that the system uses to create the MDI child window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c88a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c88a-110">Return value</span></span>

<span data-ttu-id="8c88a-111">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="8c88a-111">Type: **HWND**</span></span>

<span data-ttu-id="8c88a-112">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert das Handle für das neue untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c88a-112">If the message succeeds, the return value is the handle to the new child window.</span></span>

<span data-ttu-id="8c88a-113">Wenn die Meldung fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="8c88a-113">If the message fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c88a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c88a-114">Remarks</span></span>

<span data-ttu-id="8c88a-115">Das untergeordnete MDI-Fenster wird mit [**den Fenster Stil**](window-styles.md) Bits **WS \_ Child**, **WS \_ clipcaption**, **WS \_ clipchildren**, **WS \_ sysmenu**, **WS \_ Caption**, **WS Thick \_ Frame**, **WS \_ MinimizeBox** und **WS \_ MaximizeBox** sowie zusätzlichen stilbits erstellt, die in der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8c88a-115">The MDI child window is created with the [**window style**](window-styles.md) bits **WS\_CHILD**, **WS\_CLIPSIBLINGS**, **WS\_CLIPCHILDREN**, **WS\_SYSMENU**, **WS\_CAPTION**, **WS\_THICKFRAME**, **WS\_MINIMIZEBOX**, and **WS\_MAXIMIZEBOX**, plus additional style bits specified in the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="8c88a-116">Das System fügt den Titel des neuen untergeordneten Fensters dem Fenstermenü des Rahmen Fensters hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c88a-116">The system adds the title of the new child window to the window menu of the frame window.</span></span> <span data-ttu-id="8c88a-117">Eine Anwendung sollte diese Meldung verwenden, um alle untergeordneten Fenster des Client Fensters zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c88a-117">An application should use this message to create all child windows of the client window.</span></span>

<span data-ttu-id="8c88a-118">Wenn ein MDI-Client Fenster eine Nachricht empfängt, die die Aktivierung der untergeordneten Fenster ändert, während das aktive untergeordnete Fenster maximiert ist, stellt das System das aktive untergeordnete Fenster wieder her und maximiert das neu aktivierte untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c88a-118">If an MDI client window receives any message that changes the activation of its child windows while the active child window is maximized, the system restores the active child window and maximizes the newly activated child window.</span></span>

<span data-ttu-id="8c88a-119">Wenn ein untergeordnetes MDI-Fenster erstellt wird, sendet das System die [**WM \_ Create**](wm-create.md) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c88a-119">When an MDI child window is created, the system sends the [**WM\_CREATE**](wm-create.md) message to the window.</span></span> <span data-ttu-id="8c88a-120">Der *LPARAM* -Parameter der " **WM \_ Create** "-Meldung enthält einen Zeiger auf eine " [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8c88a-120">The *lParam* parameter of the **WM\_CREATE** message contains a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="8c88a-121">Der Member *lpkreateparameams* dieser Struktur enthält einen Zeiger auf die [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur, die mit der **WM- \_ mdicreate** -Meldung übergeben wurde, die das untergeordnete MDI-Fenster erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="8c88a-121">The *lpCreateParams* member of this structure contains a pointer to the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure passed with the **WM\_MDICREATE** message that created the MDI child window.</span></span>

<span data-ttu-id="8c88a-122">Eine Anwendung sollte keine zweite WM- **\_ mdicreate** -Nachricht senden, während eine **WM- \_ mdicreate** -Nachricht noch verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="8c88a-122">An application should not send a second **WM\_MDICREATE** message while a **WM\_MDICREATE** message is still being processed.</span></span> <span data-ttu-id="8c88a-123">Beispielsweise sollte eine **WM- \_ mdicreate** -Nachricht nicht gesendet werden, solange ein untergeordnetes MDI-Fenster die **WM- \_ mdicreate** -Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8c88a-123">For example, it should not send a **WM\_MDICREATE** message while an MDI child window is processing its **WM\_MDICREATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c88a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c88a-124">Requirements</span></span>



| <span data-ttu-id="8c88a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c88a-125">Requirement</span></span> | <span data-ttu-id="8c88a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8c88a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c88a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c88a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c88a-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c88a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8c88a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c88a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c88a-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c88a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8c88a-131">Header</span><span class="sxs-lookup"><span data-stu-id="8c88a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c88a-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8c88a-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c88a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c88a-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c88a-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8c88a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c88a-135">**"Anatemdiwindow"**</span><span class="sxs-lookup"><span data-stu-id="8c88a-135">**CreateMDIWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[<span data-ttu-id="8c88a-136">**CREATESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="8c88a-136">**CREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[<span data-ttu-id="8c88a-137">**Mdikreatestruct**</span><span class="sxs-lookup"><span data-stu-id="8c88a-137">**MDICREATESTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[<span data-ttu-id="8c88a-138">**WM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="8c88a-138">**WM\_CREATE**</span></span>](wm-create.md)
</dt> <dt>

[<span data-ttu-id="8c88a-139">**WM- \_ mdidestroy**</span><span class="sxs-lookup"><span data-stu-id="8c88a-139">**WM\_MDIDESTROY**</span></span>](wm-mdidestroy.md)
</dt> <dt>

<span data-ttu-id="8c88a-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8c88a-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8c88a-141">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8c88a-141">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 
