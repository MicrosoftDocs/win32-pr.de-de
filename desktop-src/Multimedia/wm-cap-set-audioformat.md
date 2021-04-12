---
title: WM_CAP_SET_AUDIOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ Set \_ Audioformat"-Meldung legt das Audioformat fest, das beim Ausführen von Streaming oder Schritt Erfassung verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des capsetaudioformat-Makros senden.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104151"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="efce5-105">WM \_ Cap \_ Set \_ Audioformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="efce5-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="efce5-106">Die " **WM \_ Cap \_ Set \_ Audioformat** "-Meldung legt das Audioformat fest, das beim Ausführen von Streaming oder Schritt Erfassung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efce5-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="efce5-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="efce5-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="efce5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="efce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efce5-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="efce5-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="efce5-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="efce5-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="efce5-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psaudioformat*</span><span class="sxs-lookup"><span data-stu-id="efce5-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="efce5-112">Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -oder [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) -Struktur, die das Audioformat definiert.</span><span class="sxs-lookup"><span data-stu-id="efce5-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efce5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efce5-113">Return Value</span></span>

<span data-ttu-id="efce5-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="efce5-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="efce5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efce5-115">Requirements</span></span>



| <span data-ttu-id="efce5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efce5-116">Requirement</span></span> | <span data-ttu-id="efce5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="efce5-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="efce5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efce5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="efce5-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efce5-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="efce5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efce5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="efce5-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efce5-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="efce5-122">Header</span><span class="sxs-lookup"><span data-stu-id="efce5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="efce5-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="efce5-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efce5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efce5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efce5-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="efce5-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="efce5-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="efce5-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

