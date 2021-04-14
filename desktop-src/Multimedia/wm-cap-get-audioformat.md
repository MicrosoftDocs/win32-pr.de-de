---
title: WM_CAP_GET_AUDIOFORMAT Meldung (VFW. h)
description: Die "WM \_ Cap \_ get \_ Audioformat"-Nachricht erhält das Audioformat oder die Größe des Audioformats. Sie können diese Nachricht explizit oder mithilfe der Makros capgetaudioformat und capgetaudioformatsize senden.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- WM_CAP_GET_AUDIOFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391506"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="ac979-105">WM- \_ Cap \_ get \_ Audioformat-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ac979-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="ac979-106">Die " **WM \_ Cap \_ get \_ Audioformat** "-Nachricht erhält das Audioformat oder die Größe des Audioformats.</span><span class="sxs-lookup"><span data-stu-id="ac979-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="ac979-107">Sie können diese Nachricht explizit oder mithilfe der Makros [**capgetaudioformat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) und [**capgetaudioformatsize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) senden.</span><span class="sxs-lookup"><span data-stu-id="ac979-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="ac979-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac979-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac979-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="ac979-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="ac979-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ac979-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="ac979-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psaudioformat*</span><span class="sxs-lookup"><span data-stu-id="ac979-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="ac979-112">Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ac979-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="ac979-113">Wenn der Wert **null** ist, wird die Größe (in Bytes) zurückgegeben, die zum Speichern der Struktur erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ac979-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac979-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac979-114">Return Value</span></span>

<span data-ttu-id="ac979-115">Gibt die Größe des Audioformats in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="ac979-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac979-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac979-116">Remarks</span></span>

<span data-ttu-id="ac979-117">Da komprimierte Audioformate unterschiedlich groß sind, müssen Anwendungen zuerst die Größe abrufen, dann Arbeitsspeicher zuweisen und schließlich die audioformatdaten anfordern.</span><span class="sxs-lookup"><span data-stu-id="ac979-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac979-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac979-118">Requirements</span></span>



| <span data-ttu-id="ac979-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac979-119">Requirement</span></span> | <span data-ttu-id="ac979-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ac979-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac979-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac979-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac979-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac979-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac979-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac979-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ac979-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac979-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac979-125">Header</span><span class="sxs-lookup"><span data-stu-id="ac979-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac979-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac979-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac979-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac979-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac979-128">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="ac979-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ac979-129">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="ac979-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

