---
title: WM_CAP_SET_CALLBACK_WAVESTREAM Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Callback \_ WaveStream"-Nachricht legt eine Rückruffunktion in der Anwendung fest.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- WM_CAP_SET_CALLBACK_WAVESTREAM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479056"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="bc425-104">WM- \_ Cap- \_ Rückruf- \_ \_ WaveStream-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bc425-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="bc425-105">Die " **WM \_ Cap \_ Set \_ Callback \_ WaveStream** "-Nachricht legt eine Rückruffunktion in der Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="bc425-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="bc425-106">Avicap ruft dieses Verfahren während der streamingerfassung auf, wenn ein neuer Audiopuffer verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="bc425-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="bc425-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonwavestream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="bc425-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="bc425-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc425-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc425-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="bc425-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="bc425-110">Ein Zeiger auf die Funktion "Wave Stream Callback" vom Typ [**capwavestreamcallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="bc425-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="bc425-111">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Wave Stream-Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc425-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc425-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc425-112">Return Value</span></span>

<span data-ttu-id="bc425-113">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc425-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc425-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc425-114">Remarks</span></span>

<span data-ttu-id="bc425-115">Im Fenster erfassen wird die Prozedur aufgerufen, bevor der Audiopuffer auf den Datenträger geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bc425-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="bc425-116">Dies ermöglicht es Anwendungen, den Audiopuffer bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="bc425-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="bc425-117">Wenn eine Wave Stream-Rückruffunktion verwendet wird, muss Sie vor dem Start der Erfassungs Sitzung installiert werden, und Sie muss für die Dauer der Sitzung aktiviert bleiben.</span><span class="sxs-lookup"><span data-stu-id="bc425-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="bc425-118">Sie kann nach Ende der streamingerfassung deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="bc425-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc425-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc425-119">Requirements</span></span>



| <span data-ttu-id="bc425-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc425-120">Requirement</span></span> | <span data-ttu-id="bc425-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bc425-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bc425-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc425-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc425-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc425-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bc425-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc425-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc425-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc425-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bc425-126">Header</span><span class="sxs-lookup"><span data-stu-id="bc425-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc425-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc425-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc425-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc425-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc425-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="bc425-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bc425-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="bc425-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





