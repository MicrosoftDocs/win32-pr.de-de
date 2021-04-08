---
title: WM_CAP_GET_STATUS Meldung (VFW. h)
description: Mit der \_ Statusmeldung "WM-Cap- \_ Status abrufen" wird \_ der Status des Aufzeichnungs Fensters abgerufen. Sie können diese Nachricht explizit oder mithilfe des capgetstatus-Makros senden.
ms.assetid: 31349599-a52c-45ba-8f08-91008773f317
keywords:
- WM_CAP_GET_STATUS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ef6590770e8a9ece3eb8abaffb4dbca0b1a4d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040070"
---
# <a name="wm_cap_get_status-message"></a><span data-ttu-id="1309b-105">\_ \_ \_ Status Meldung zur WM-Abdeckung</span><span class="sxs-lookup"><span data-stu-id="1309b-105">WM\_CAP\_GET\_STATUS message</span></span>

<span data-ttu-id="1309b-106">Mit der Statusmeldung " **WM-Cap- \_ \_ \_ Status** abrufen" wird der Status des Aufzeichnungs Fensters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1309b-106">The **WM\_CAP\_GET\_STATUS** message retrieves the status of the capture window.</span></span> <span data-ttu-id="1309b-107">Sie können diese Nachricht explizit oder mithilfe des [**capgetstatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1309b-107">You can send this message explicitly or by using the [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) macro.</span></span>


```C++
WM_CAP_GET_STATUS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPSTATUS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="1309b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1309b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1309b-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="1309b-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="1309b-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1309b-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="1309b-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="1309b-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="1309b-112">Zeiger auf eine [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1309b-112">Pointer to a [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1309b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1309b-113">Return Value</span></span>

<span data-ttu-id="1309b-114">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1309b-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="1309b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1309b-115">Remarks</span></span>

<span data-ttu-id="1309b-116">Die [**capstatus**](/windows/win32/api/vfw/ns-vfw-capstatus) -Struktur enthält den aktuellen Status des Aufzeichnungs Fensters.</span><span class="sxs-lookup"><span data-stu-id="1309b-116">The [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure contains the current state of the capture window.</span></span> <span data-ttu-id="1309b-117">Da dieser Zustand dynamisch ist und sich als Reaktion auf verschiedene Nachrichten ändert, sollte die Anwendung diese Struktur nach dem Senden der [**WM- \_ Cap- \_ DLG \_**](wm-cap-dlg-videoformat.md) -Nachricht (oder mithilfe des [**capdlgvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) -Makros) und immer dann, wenn Sie Menü Elemente aktivieren oder den tatsächlichen Zustand des Fensters bestimmen muss, initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1309b-117">Since this state is dynamic and changes in response to various messages, the application should initialize this structure after sending the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro) and whenever it needs to enable menu items or determine the actual state of the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1309b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1309b-118">Requirements</span></span>



| <span data-ttu-id="1309b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1309b-119">Requirement</span></span> | <span data-ttu-id="1309b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1309b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1309b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1309b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1309b-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1309b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1309b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1309b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1309b-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1309b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1309b-125">Header</span><span class="sxs-lookup"><span data-stu-id="1309b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1309b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1309b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1309b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1309b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1309b-128">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="1309b-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="1309b-129">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="1309b-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





