---
title: WM_POINTERDEVICEINRANGE Meldung
description: Wird an ein Fenster gesendet, wenn ein Zeiger Gerät innerhalb des Bereichs eines eingabedigitalisierers erkannt wird. Diese Meldung enthält Informationen zum Gerät und seiner Nähe.
ms.assetid: 04244758-E662-4FB2-850E-20B4B3D1294A
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERDEVICEINRANGE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEINRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 76ab6ac4f96d1df4e4e29afbcefe86d34b8b602d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518767"
---
# <a name="wm_pointerdeviceinrange-message"></a><span data-ttu-id="1e7f0-105">WM_POINTERDEVICEINRANGE Meldung</span><span class="sxs-lookup"><span data-stu-id="1e7f0-105">WM_POINTERDEVICEINRANGE message</span></span>

<span data-ttu-id="1e7f0-106">Wird an ein Fenster gesendet, wenn ein Zeiger Gerät innerhalb des Bereichs eines eingabedigitalisierers erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-106">Sent to a window when a pointer device is detected within range of an input digitizer.</span></span> <span data-ttu-id="1e7f0-107">Diese Meldung enthält Informationen zum Gerät und seiner Nähe.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="1e7f0-108">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="1e7f0-108">\[!Important\]</span></span>  
> <span data-ttu-id="1e7f0-109">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="1e7f0-110">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="1e7f0-111">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="1e7f0-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="1e7f0-112">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1e7f0-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEINRANGE       0X239
```



## <a name="parameters"></a><span data-ttu-id="1e7f0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e7f0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7f0-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e7f0-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7f0-115">Zusätzliche meldungsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="1e7f0-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e7f0-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7f0-117">Zusätzliche meldungsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7f0-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e7f0-118">Return value</span></span>

<span data-ttu-id="1e7f0-119">Wenn die Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="1e7f0-120">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1e7f0-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7f0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e7f0-121">Requirements</span></span>



| <span data-ttu-id="1e7f0-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e7f0-122">Requirement</span></span> | <span data-ttu-id="1e7f0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1e7f0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e7f0-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e7f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7f0-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e7f0-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="1e7f0-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e7f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7f0-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e7f0-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1e7f0-128">Header</span><span class="sxs-lookup"><span data-stu-id="1e7f0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e7f0-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1e7f0-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e7f0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e7f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7f0-131">Meldungen</span><span class="sxs-lookup"><span data-stu-id="1e7f0-131">Messages</span></span>](messages.md)
</dt> </dl>

 

