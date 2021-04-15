---
title: WM_CAP_FILE_SAVEDIB Meldung (VFW. h)
description: Die \_ savedib-Nachricht der WM-Cap- \_ Datei \_ kopiert den aktuellen Frame in eine DIB-Datei. Sie können diese Nachricht explizit oder mithilfe des capfilesavedib-Makros senden.
ms.assetid: bf6d343b-9236-4e68-bbda-2ed6e197a5cb
keywords:
- WM_CAP_FILE_SAVEDIB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEDIB
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2155febfdac1b3f24133df47ce206c8e5ec33d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479059"
---
# <a name="wm_cap_file_savedib-message"></a><span data-ttu-id="f3357-105">WM- \_ Cap- \_ Datei ( \_ savedib)</span><span class="sxs-lookup"><span data-stu-id="f3357-105">WM\_CAP\_FILE\_SAVEDIB message</span></span>

<span data-ttu-id="f3357-106">Die **\_ \_ \_ savedib** -Nachricht der WM-Cap-Datei kopiert den aktuellen Frame in eine DIB-Datei.</span><span class="sxs-lookup"><span data-stu-id="f3357-106">The **WM\_CAP\_FILE\_SAVEDIB** message copies the current frame to a DIB file.</span></span> <span data-ttu-id="f3357-107">Sie können diese Nachricht explizit oder mithilfe des [**capfilesavedib**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="f3357-107">You can send this message explicitly or by using the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro.</span></span>


```C++
WM_CAP_FILE_SAVEDIB 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="f3357-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3357-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3357-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="f3357-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="f3357-110">Ein Zeiger auf die NULL-terminierte Zeichenfolge, die den Namen der Ziel-DIB-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="f3357-110">Pointer to the null-terminated string that contains the name of the destination DIB file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3357-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3357-111">Return Value</span></span>

<span data-ttu-id="f3357-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f3357-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="f3357-113">Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3357-113">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3357-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3357-114">Remarks</span></span>

<span data-ttu-id="f3357-115">Wenn der Aufzeichnungs Treiber Frames in einem komprimierten Format bereitstellt, versucht dieser Vorgang, den Frame zu dekomprimieren, bevor die Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f3357-115">If the capture driver supplies frames in a compressed format, this call attempts to decompress the frame before writing the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3357-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3357-116">Requirements</span></span>



| <span data-ttu-id="f3357-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3357-117">Requirement</span></span> | <span data-ttu-id="f3357-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f3357-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f3357-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3357-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3357-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3357-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f3357-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3357-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3357-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3357-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f3357-123">Header</span><span class="sxs-lookup"><span data-stu-id="f3357-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3357-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3357-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3357-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3357-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3357-126">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="f3357-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f3357-127">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="f3357-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





