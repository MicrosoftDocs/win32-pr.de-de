---
title: WM_POINTERDEVICEOUTOFRANGE Meldung
description: Wird an ein Fenster gesendet, wenn ein Zeiger Gerät den Bereich eines eingabedigitalisierers verlassen hat. Diese Meldung enthält Informationen zum Gerät und seiner Nähe.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERDEVICEOUTOFRANGE Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103390"
---
# <a name="wm_pointerdeviceoutofrange-message"></a><span data-ttu-id="750ac-105">WM_POINTERDEVICEOUTOFRANGE Meldung</span><span class="sxs-lookup"><span data-stu-id="750ac-105">WM_POINTERDEVICEOUTOFRANGE message</span></span>

<span data-ttu-id="750ac-106">Wird an ein Fenster gesendet, wenn ein Zeiger Gerät den Bereich eines eingabedigitalisierers verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="750ac-106">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="750ac-107">Diese Meldung enthält Informationen zum Gerät und seiner Nähe.</span><span class="sxs-lookup"><span data-stu-id="750ac-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="750ac-108">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="750ac-108">\[!Important\]</span></span>  
> <span data-ttu-id="750ac-109">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="750ac-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="750ac-110">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="750ac-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="750ac-111">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="750ac-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="750ac-112">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="750ac-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a><span data-ttu-id="750ac-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="750ac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="750ac-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="750ac-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750ac-115">Zusätzliche meldungsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="750ac-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="750ac-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="750ac-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="750ac-117">Zusätzliche meldungsspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="750ac-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="750ac-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="750ac-118">Return value</span></span>

<span data-ttu-id="750ac-119">Wenn die Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="750ac-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="750ac-120">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="750ac-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="750ac-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="750ac-121">Requirements</span></span>



| <span data-ttu-id="750ac-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="750ac-122">Requirement</span></span> | <span data-ttu-id="750ac-123">Wert</span><span class="sxs-lookup"><span data-stu-id="750ac-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="750ac-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="750ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="750ac-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="750ac-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="750ac-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="750ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="750ac-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="750ac-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="750ac-128">Header</span><span class="sxs-lookup"><span data-stu-id="750ac-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="750ac-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="750ac-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="750ac-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="750ac-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="750ac-131">Meldungen</span><span class="sxs-lookup"><span data-stu-id="750ac-131">Messages</span></span>](messages.md)
</dt> </dl>

 

