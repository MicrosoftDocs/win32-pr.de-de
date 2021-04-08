---
title: WM_CAP_SET_VIDEOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set Videoformat"- \_ Meldung legt das Format der aufgezeichneten Videodaten fest. Sie können diese Nachricht explizit oder mithilfe des capsetvideoformat-Makros senden.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957133"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="42ad0-105">WM- \_ Cap- \_ Set- \_ videoformatmeldung</span><span class="sxs-lookup"><span data-stu-id="42ad0-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="42ad0-106">Die " **WM \_ Cap \_ Set \_ Videoformat** "-Meldung legt das Format der aufgezeichneten Videodaten fest.</span><span class="sxs-lookup"><span data-stu-id="42ad0-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="42ad0-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetvideoformat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="42ad0-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="42ad0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ad0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ad0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="42ad0-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="42ad0-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="42ad0-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="42ad0-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psvideoformat*</span><span class="sxs-lookup"><span data-stu-id="42ad0-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="42ad0-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="42ad0-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42ad0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42ad0-113">Return Value</span></span>

<span data-ttu-id="42ad0-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="42ad0-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="42ad0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42ad0-115">Remarks</span></span>

<span data-ttu-id="42ad0-116">Da Videoformate gerätespezifisch sind, sollten Anwendungen den Rückgabewert dieser Funktion überprüfen, um festzustellen, ob das Format vom Treiber akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="42ad0-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ad0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42ad0-117">Requirements</span></span>



| <span data-ttu-id="42ad0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42ad0-118">Requirement</span></span> | <span data-ttu-id="42ad0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="42ad0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="42ad0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42ad0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42ad0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42ad0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="42ad0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42ad0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42ad0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42ad0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="42ad0-124">Header</span><span class="sxs-lookup"><span data-stu-id="42ad0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="42ad0-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ad0-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ad0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42ad0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ad0-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="42ad0-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="42ad0-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="42ad0-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

