---
title: WM_CAP_GET_VIDEOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ Get Videoformat"- \_ Meldung Ruft eine Kopie des verwendeten Video Formats oder die erforderliche Größe für das Videoformat ab. Sie können diese Nachricht explizit oder mithilfe der Makros capgetvideoformat und capgetvideoformatsize senden.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956435"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="3dbbc-105">WM-Abdeckung \_ \_ get \_ Videoformat Message</span><span class="sxs-lookup"><span data-stu-id="3dbbc-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="3dbbc-106">Die " **WM \_ Cap \_ get \_ Videoformat** "-Meldung Ruft eine Kopie des verwendeten Video Formats oder die erforderliche Größe für das Videoformat ab.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="3dbbc-107">Sie können diese Nachricht explizit oder mithilfe der Makros [**capgetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) und [**capgetvideoformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) senden.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="3dbbc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dbbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbbc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="3dbbc-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="3dbbc-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="3dbbc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psvideoformat*</span><span class="sxs-lookup"><span data-stu-id="3dbbc-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="3dbbc-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="3dbbc-113">Sie können auch **null** angeben, um die erforderliche Anzahl von Bytes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbbc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dbbc-114">Return Value</span></span>

<span data-ttu-id="3dbbc-115">Gibt die Größe (in Bytes) des Video Formats oder 0 (null) zurück, wenn das Erfassungsfenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="3dbbc-116">Für Videoformate, für die eine Palette erforderlich ist, wird die aktuelle Palette ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbbc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dbbc-117">Remarks</span></span>

<span data-ttu-id="3dbbc-118">Da komprimierte Videoformate die Größenanforderungen variieren, müssen Anwendungen zuerst die Größe abrufen, dann Arbeitsspeicher zuweisen und schließlich die Videoformat Daten anfordern.</span><span class="sxs-lookup"><span data-stu-id="3dbbc-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbbc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dbbc-119">Requirements</span></span>



| <span data-ttu-id="3dbbc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dbbc-120">Requirement</span></span> | <span data-ttu-id="3dbbc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3dbbc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3dbbc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dbbc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbbc-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dbbc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3dbbc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dbbc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbbc-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dbbc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3dbbc-126">Header</span><span class="sxs-lookup"><span data-stu-id="3dbbc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbbc-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbbc-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbbc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dbbc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbbc-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="3dbbc-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3dbbc-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="3dbbc-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

