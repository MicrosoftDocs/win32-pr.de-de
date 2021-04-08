---
title: WM_CAP_FILE_SET_CAPTURE_FILE Meldung (VFW. h)
description: Die Datei Satz-Erfassungs Datei für die WM-Abdeckung gibt \_ \_ \_ \_ \_ die für die Video Erfassung verwendete Datei an. Sie können diese Nachricht explizit oder mithilfe des capfilesetcapturefile-Makros senden.
ms.assetid: d96e498b-6322-4d48-a5d7-156e95f23740
keywords:
- WM_CAP_FILE_SET_CAPTURE_FILE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SET_CAPTURE_FILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b3f59edfc9bf01f6bd2af3b9028f8e3315e2de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949396"
---
# <a name="wm_cap_file_set_capture_file-message"></a><span data-ttu-id="88cc4-105">WM- \_ Cap- \_ Datei Satz- \_ \_ Erfassungs \_ Datei Nachricht</span><span class="sxs-lookup"><span data-stu-id="88cc4-105">WM\_CAP\_FILE\_SET\_CAPTURE\_FILE message</span></span>

<span data-ttu-id="88cc4-106">Die **Datei \_ \_ Satz- \_ \_ Erfassungs \_** Datei für die WM-Abdeckung gibt die für die Video Erfassung verwendete Datei an.</span><span class="sxs-lookup"><span data-stu-id="88cc4-106">The **WM\_CAP\_FILE\_SET\_CAPTURE\_FILE** message names the file used for video capture.</span></span> <span data-ttu-id="88cc4-107">Sie können diese Nachricht explizit oder mithilfe des [**capfilesetcapturefile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="88cc4-107">You can send this message explicitly or by using the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro.</span></span>


```C++
WM_CAP_FILE_SET_CAPTURE_FILE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="88cc4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88cc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88cc4-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="88cc4-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="88cc4-110">Ein Zeiger auf die auf NULL endende Zeichenfolge, die den Namen der zu verwendenden Erfassungs Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="88cc4-110">Pointer to the null-terminated string that contains the name of the capture file to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88cc4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88cc4-111">Return Value</span></span>

<span data-ttu-id="88cc4-112">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn der Dateiname ungültig ist, oder wenn ein Streaming oder eine einzelne Frame-Erfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88cc4-112">Returns **TRUE** if successful or **FALSE** if the filename is invalid, or if streaming or single-frame capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="88cc4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88cc4-113">Remarks</span></span>

<span data-ttu-id="88cc4-114">In dieser Meldung wird der Dateiname in einer internen Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="88cc4-114">This message stores the filename in an internal structure.</span></span> <span data-ttu-id="88cc4-115">Die angegebene Datei wird nicht erstellt, neu erstellt oder geöffnet.</span><span class="sxs-lookup"><span data-stu-id="88cc4-115">It does not create, allocate, or open the specified file.</span></span> <span data-ttu-id="88cc4-116">Der Standard Dateiname für die Aufzeichnung ist C: \\CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="88cc4-116">The default capture filename is C:\\CAPTURE.AVI.</span></span>

## <a name="requirements"></a><span data-ttu-id="88cc4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88cc4-117">Requirements</span></span>



| <span data-ttu-id="88cc4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88cc4-118">Requirement</span></span> | <span data-ttu-id="88cc4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="88cc4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="88cc4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88cc4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88cc4-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88cc4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="88cc4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88cc4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88cc4-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88cc4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="88cc4-124">Header</span><span class="sxs-lookup"><span data-stu-id="88cc4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88cc4-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="88cc4-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cc4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88cc4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cc4-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="88cc4-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="88cc4-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="88cc4-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





