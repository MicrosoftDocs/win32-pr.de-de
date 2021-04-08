---
title: MM_WOM_DONE Meldung (MMSYSTEM. h)
description: Die \_ Meldung mm WOM \_ done wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird. Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der wavesetzset-Funktion.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743913"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="358ac-105">MM- \_ WOM- \_ Nachricht abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="358ac-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="358ac-106">Die Meldung **mm \_ WOM \_ done** wird an ein Fenster gesendet, wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="358ac-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="358ac-107">Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der [**wavesetzset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="358ac-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="358ac-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="358ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="358ac-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*houtputdev*</span><span class="sxs-lookup"><span data-stu-id="358ac-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="358ac-110">Handle für das Waveform-Audioausgabegerät, das den Puffer wiedergegeben hat.</span><span class="sxs-lookup"><span data-stu-id="358ac-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="358ac-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="358ac-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="358ac-112">Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="358ac-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="358ac-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="358ac-113">Return Value</span></span>

<span data-ttu-id="358ac-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="358ac-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="358ac-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="358ac-115">Requirements</span></span>



| <span data-ttu-id="358ac-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="358ac-116">Requirement</span></span> | <span data-ttu-id="358ac-117">Wert</span><span class="sxs-lookup"><span data-stu-id="358ac-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="358ac-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="358ac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="358ac-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="358ac-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="358ac-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="358ac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="358ac-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="358ac-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="358ac-122">Header</span><span class="sxs-lookup"><span data-stu-id="358ac-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="358ac-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="358ac-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="358ac-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="358ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="358ac-125">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="358ac-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="358ac-126">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="358ac-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

