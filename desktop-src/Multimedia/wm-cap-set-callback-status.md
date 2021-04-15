---
title: WM_CAP_SET_CALLBACK_STATUS Meldung (VFW. h)
description: Die WM-Cap-Richtlinien- \_ \_ \_ Rückruf \_ Statusmeldung legt eine Status Rückruffunktion in der Anwendung fest. Avicap ruft dieses Verfahren auf, wenn der Status des Aufzeichnungs Fensters geändert wird. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackonstatus-Makros senden.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475492"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="54e36-106">WM- \_ Cap- \_ \_ Rückruf \_ Status Meldung festlegen</span><span class="sxs-lookup"><span data-stu-id="54e36-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="54e36-107">Die WM-Cap-Richtlinien- **\_ \_ \_ Rückruf \_ Status** Meldung legt eine Status Rückruffunktion in der Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="54e36-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="54e36-108">Avicap ruft dieses Verfahren auf, wenn der Status des Aufzeichnungs Fensters geändert wird.</span><span class="sxs-lookup"><span data-stu-id="54e36-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="54e36-109">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackonstatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="54e36-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="54e36-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="54e36-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e36-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="54e36-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="54e36-112">Ein Zeiger auf die Status Rückruffunktion vom Typ [**capstatuscallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="54e36-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="54e36-113">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Status Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="54e36-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e36-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54e36-114">Return Value</span></span>

<span data-ttu-id="54e36-115">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54e36-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e36-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54e36-116">Remarks</span></span>

<span data-ttu-id="54e36-117">Anwendungen können optional eine Status Rückruffunktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="54e36-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="54e36-118">Wenn diese Einstellung festgelegt ist, ruft avicap diese Prozedur in den folgenden Situationen auf:</span><span class="sxs-lookup"><span data-stu-id="54e36-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="54e36-119">Eine Aufzeichnungs Sitzung ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="54e36-119">A capture session is completed.</span></span>
-   <span data-ttu-id="54e36-120">Ein Aufzeichnungs Treiber hat erfolgreich eine Verbindung mit einem Aufzeichnungs Fenster hergestellt.</span><span class="sxs-lookup"><span data-stu-id="54e36-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="54e36-121">Eine optimale Palette wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="54e36-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="54e36-122">Die Anzahl der aufgezeichneten Frames wird gemeldet.</span><span class="sxs-lookup"><span data-stu-id="54e36-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e36-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54e36-123">Requirements</span></span>



| <span data-ttu-id="54e36-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54e36-124">Requirement</span></span> | <span data-ttu-id="54e36-125">Wert</span><span class="sxs-lookup"><span data-stu-id="54e36-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="54e36-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54e36-126">Minimum supported client</span></span><br/> | <span data-ttu-id="54e36-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54e36-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="54e36-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54e36-128">Minimum supported server</span></span><br/> | <span data-ttu-id="54e36-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54e36-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54e36-130">Header</span><span class="sxs-lookup"><span data-stu-id="54e36-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e36-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e36-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e36-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54e36-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e36-133">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="54e36-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="54e36-134">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="54e36-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





