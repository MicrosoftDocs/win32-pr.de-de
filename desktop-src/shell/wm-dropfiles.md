---
description: Wird gesendet, wenn der Benutzer eine Datei im Fenster einer Anwendung löscht, die sich selbst als Empfänger von gelöschten Dateien registriert hat.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: WM_DROPFILES Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979465"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="d0cdd-103">WM \_ dropfiles-Meldung</span><span class="sxs-lookup"><span data-stu-id="d0cdd-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="d0cdd-104">Wird gesendet, wenn der Benutzer eine Datei im Fenster einer Anwendung löscht, die sich selbst als Empfänger von gelöschten Dateien registriert hat.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="d0cdd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0cdd-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0cdd-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="d0cdd-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="d0cdd-107">Ein Handle für eine interne-Struktur, die die gelöschten Dateien beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="d0cdd-108">Übergeben Sie das Handle [**dragfinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**dragqueryfile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)oder [**dragquerypoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) , um Informationen zu den gelöschten Dateien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="d0cdd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0cdd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0cdd-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0cdd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d0cdd-111">Return value</span></span>

<span data-ttu-id="d0cdd-112">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0cdd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0cdd-113">Remarks</span></span>

<span data-ttu-id="d0cdd-114">Das HDROP-Handle wird in shellapi. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="d0cdd-115">Sie müssen diesen Header in Ihren Build einschließen, um **WM \_ dropfiles** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="d0cdd-116">Weitere Informationen zur Verwendung von Drag & amp; Drop zum Übertragen von shelldaten finden Sie unter über [tragen von shelldaten per Drag & Drop oder Zwischenablage](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="d0cdd-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0cdd-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d0cdd-117">Requirements</span></span>



| <span data-ttu-id="d0cdd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0cdd-118">Requirement</span></span> | <span data-ttu-id="d0cdd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d0cdd-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0cdd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0cdd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d0cdd-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0cdd-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d0cdd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0cdd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d0cdd-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0cdd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0cdd-124">Header</span><span class="sxs-lookup"><span data-stu-id="d0cdd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0cdd-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0cdd-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0cdd-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0cdd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0cdd-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="d0cdd-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="d0cdd-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="d0cdd-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
