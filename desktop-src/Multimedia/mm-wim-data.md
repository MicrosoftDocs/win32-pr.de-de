---
title: MM_WIM_DATA Meldung (MMSYSTEM. h)
description: Die mm \_ \_ -WIM-Daten Nachricht wird an ein Fenster gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird. Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die waveinreset-Funktion aufgerufen wurde.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- MM_WIM_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338793"
---
# <a name="mm_wim_data-message"></a><span data-ttu-id="5ed38-105">MM- \_ WIM- \_ Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="5ed38-105">MM\_WIM\_DATA message</span></span>

<span data-ttu-id="5ed38-106">Die **mm- \_ WIM- \_ Daten** Nachricht wird an ein Fenster gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ed38-106">The **MM\_WIM\_DATA** message is sent to a window when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="5ed38-107">Die Nachricht kann entweder gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5ed38-107">The message can be sent either when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="5ed38-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ed38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed38-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hinputdev*</span><span class="sxs-lookup"><span data-stu-id="5ed38-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="5ed38-110">Handle für das Waveform-Audioeingabegerät, das die Daten empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="5ed38-110">Handle to the waveform-audio input device that received the data.</span></span>

</dd> <dt>

<span data-ttu-id="5ed38-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="5ed38-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="5ed38-112">Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="5ed38-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed38-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ed38-113">Return Value</span></span>

<span data-ttu-id="5ed38-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed38-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ed38-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ed38-115">Remarks</span></span>

<span data-ttu-id="5ed38-116">Der zurückgegebene Puffer ist möglicherweise nicht voll.</span><span class="sxs-lookup"><span data-stu-id="5ed38-116">The returned buffer might not be full.</span></span> <span data-ttu-id="5ed38-117">Verwenden Sie den **dwbyteslock** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die von *LPARAM* angegeben wird, um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="5ed38-117">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lParam* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed38-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ed38-118">Requirements</span></span>



| <span data-ttu-id="5ed38-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ed38-119">Requirement</span></span> | <span data-ttu-id="5ed38-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5ed38-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed38-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ed38-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed38-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed38-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ed38-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ed38-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed38-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ed38-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ed38-125">Header</span><span class="sxs-lookup"><span data-stu-id="5ed38-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed38-126"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed38-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed38-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ed38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed38-128">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="5ed38-128">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="5ed38-129">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="5ed38-129">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

