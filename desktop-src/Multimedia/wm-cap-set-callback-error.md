---
title: WM_CAP_SET_CALLBACK_ERROR Meldung (VFW. h)
description: Die WM- \_ Cap- \_ \_ Rückruf \_ Fehlermeldung legt eine Fehler Rückruffunktion in der Client Anwendung fest. Avicap ruft dieses Verfahren auf, wenn Fehler auftreten. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonerror-Makros senden.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- WM_CAP_SET_CALLBACK_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477247"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="caa0e-106">\_ \_ \_ Rückruf \_ Fehlermeldung für WM-Cap-Satz</span><span class="sxs-lookup"><span data-stu-id="caa0e-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="caa0e-107">Die **WM- \_ Cap- \_ \_ Rückruf \_ Fehlermeldung** legt eine Fehler Rückruffunktion in der Client Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="caa0e-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="caa0e-108">Avicap ruft dieses Verfahren auf, wenn Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="caa0e-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="caa0e-109">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonerror**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="caa0e-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="caa0e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="caa0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caa0e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="caa0e-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="caa0e-112">Zeiger auf die Fehler Rückruffunktion vom Typ " [**caperrorcallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka)".</span><span class="sxs-lookup"><span data-stu-id="caa0e-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="caa0e-113">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Fehler Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="caa0e-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caa0e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="caa0e-114">Return Value</span></span>

<span data-ttu-id="caa0e-115">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="caa0e-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="caa0e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="caa0e-116">Remarks</span></span>

<span data-ttu-id="caa0e-117">Anwendungen können optional eine Fehler Rückruffunktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="caa0e-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="caa0e-118">Wenn diese Einstellung festgelegt ist, wird die Fehler Prozedur von avicap in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="caa0e-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="caa0e-119">Der Datenträger ist voll.</span><span class="sxs-lookup"><span data-stu-id="caa0e-119">The disk is full.</span></span>
-   <span data-ttu-id="caa0e-120">Ein Aufzeichnungs Fenster kann nicht mit einem Aufzeichnungs Treiber verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="caa0e-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="caa0e-121">Ein Waveform-Audiogerät kann nicht geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="caa0e-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="caa0e-122">Die Anzahl der während der Erfassung verworfenen Frames überschreitet den angegebenen Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="caa0e-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="caa0e-123">Die Rahmen können aufgrund vertikaler Synchronisierungs Probleme nicht erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="caa0e-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="caa0e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="caa0e-124">Requirements</span></span>



| <span data-ttu-id="caa0e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="caa0e-125">Requirement</span></span> | <span data-ttu-id="caa0e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="caa0e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="caa0e-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="caa0e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="caa0e-128">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa0e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="caa0e-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="caa0e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="caa0e-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="caa0e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="caa0e-131">Header</span><span class="sxs-lookup"><span data-stu-id="caa0e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="caa0e-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="caa0e-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caa0e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caa0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caa0e-134">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="caa0e-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="caa0e-135">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="caa0e-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





