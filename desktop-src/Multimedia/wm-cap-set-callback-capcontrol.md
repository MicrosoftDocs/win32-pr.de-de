---
title: WM_CAP_SET_CALLBACK_CAPCONTROL Meldung (VFW. h)
description: Die \_ \_ \_ capcontrol-Rückruffunktion für die WM-Abdeckung \_ legt eine Rückruffunktion in der Anwendung fest, die ihr ein präzises Aufzeichnungs Steuerelement gibt. Sie können diese Nachricht explizit oder mithilfe des capsetcallbackoncapcontrol-Makros senden.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338741"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="2f8b3-105">WM- \_ Cap-Rückruf-Rückruf- \_ \_ \_ capcontrol-Meldung</span><span class="sxs-lookup"><span data-stu-id="2f8b3-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="2f8b3-106">Die **\_ \_ \_ \_ capcontrol-Rückruf** Funktion für die WM-Abdeckung legt eine Rückruffunktion in der Anwendung fest, die ihr ein präzises Aufzeichnungs Steuerelement gibt.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="2f8b3-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetcallbackoncapcontrol**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="2f8b3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f8b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8b3-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpproc*</span><span class="sxs-lookup"><span data-stu-id="2f8b3-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="2f8b3-110">Ein Zeiger auf die Rückruffunktion vom Typ [**capcontrolcallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="2f8b3-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="2f8b3-111">Geben Sie **null** für diesen Parameter an, um eine zuvor installierte Rückruffunktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f8b3-112">Return Value</span></span>

<span data-ttu-id="2f8b3-113">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn eine streamingerfassung oder eine Single-Frame-Erfassungs Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f8b3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f8b3-114">Remarks</span></span>

<span data-ttu-id="2f8b3-115">Eine einzelne Rückruffunktion wird verwendet, um der Anwendung die genaue Kontrolle über die Momente zu verschaffen, in denen die streamingerfassung beginnt und abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="2f8b3-116">Im Aufzeichnungs Fenster wird zuerst die Prozedur aufgerufen, bei der *nState* auf controlcallback \_ Preroll festgelegt wurde, nachdem alle Puffer zugeordnet wurden und alle anderen Aufzeichnungs Vorbereitungen abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="2f8b3-117">Dadurch erhält die Anwendung die Möglichkeit, Videoquellen vorab zu überarbeiten und die Rückruffunktion zu dem Zeitpunkt zurückzugeben, zu dem die Aufzeichnung beginnt.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="2f8b3-118">Der Rückgabewert **true** von der Rückruffunktion setzt die Erfassung fort, und der Rückgabewert **false** bricht Capture ab.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="2f8b3-119">Nachdem die Erfassung begonnen hat, wird diese Rückruffunktion häufig aufgerufen, wobei *nState* auf controlcallback Capture festgelegt ist, \_ damit die Anwendung die Erfassung beenden kann, indem **false** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f8b3-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8b3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f8b3-120">Requirements</span></span>



| <span data-ttu-id="2f8b3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f8b3-121">Requirement</span></span> | <span data-ttu-id="2f8b3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2f8b3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2f8b3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f8b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8b3-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f8b3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2f8b3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f8b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8b3-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f8b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f8b3-127">Header</span><span class="sxs-lookup"><span data-stu-id="2f8b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f8b3-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8b3-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f8b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f8b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f8b3-130">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="2f8b3-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2f8b3-131">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="2f8b3-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





