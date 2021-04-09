---
title: WM_CAP_FILE_GET_CAPTURE_FILE Meldung (VFW. h)
description: Die Meldung "WM- \_ Cap- \_ Datei \_ get \_ Capture \_ file" gibt den Namen der aktuellen Erfassungs Datei zurück. Sie können diese Nachricht explizit oder mithilfe des capfilegetcapturefile-Makros senden.
ms.assetid: 86ce2904-834d-449f-9ef8-5a158c55bbaa
keywords:
- WM_CAP_FILE_GET_CAPTURE_FILE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_GET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7008e0b217f29ad9602afbdc41cc97f9cb7ecaa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858701"
---
# <a name="wm_cap_file_get_capture_file-message"></a><span data-ttu-id="3cb45-105">WM- \_ Cap- \_ Datei Nachricht zum Erfassen der \_ \_ Erfassungs \_ Datei</span><span class="sxs-lookup"><span data-stu-id="3cb45-105">WM\_CAP\_FILE\_GET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="3cb45-106">Die Meldung " **WM- \_ Cap- \_ Datei \_ get \_ Capture \_ File** " gibt den Namen der aktuellen Erfassungs Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="3cb45-106">The **WM\_CAP\_FILE\_GET\_CAPTURE\_FILE** message returns the name of the current capture file.</span></span> <span data-ttu-id="3cb45-107">Sie können diese Nachricht explizit oder mithilfe des [**capfilegetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3cb45-107">You can send this message explicitly or by using the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_GET_CAPTURE_FILE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="3cb45-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb45-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="3cb45-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="3cb45-110">Größe (in Bytes) des Anwendungs definierten Puffers, auf den von **szName** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3cb45-110">Size, in bytes, of the application-defined buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="3cb45-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="3cb45-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="3cb45-112">Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um den Namen der Erfassungs Datei als NULL-terminierte Zeichenfolge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3cb45-112">Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb45-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cb45-113">Return Value</span></span>

<span data-ttu-id="3cb45-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="3cb45-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb45-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cb45-115">Remarks</span></span>

<span data-ttu-id="3cb45-116">Der Standard Dateiname für die Aufzeichnung ist C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="3cb45-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb45-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cb45-117">Requirements</span></span>



| <span data-ttu-id="3cb45-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cb45-118">Requirement</span></span> | <span data-ttu-id="3cb45-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3cb45-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3cb45-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cb45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb45-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cb45-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3cb45-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cb45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb45-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cb45-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3cb45-124">Header</span><span class="sxs-lookup"><span data-stu-id="3cb45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb45-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb45-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb45-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cb45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb45-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="3cb45-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3cb45-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3cb45-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





