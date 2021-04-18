---
title: WIM_DATA Meldung (MMSYSTEM. h)
description: Die WIM \_ -Daten Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340365"
---
# <a name="wim_data-message"></a><span data-ttu-id="e3490-104">Wim- \_ Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="e3490-104">WIM\_DATA message</span></span>

<span data-ttu-id="e3490-105">Die **WIM- \_ Daten** Nachricht wird an die angegebene Waveform-audioeingaberückruf-Funktion gesendet, wenn Waveform-Audiodaten im Eingabepuffer vorhanden sind und der Puffer an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3490-105">The **WIM\_DATA** message is sent to the given waveform-audio input callback function when waveform-audio data is present in the input buffer and the buffer is being returned to the application.</span></span> <span data-ttu-id="e3490-106">Die Nachricht kann gesendet werden, wenn der Puffer voll ist oder nachdem die [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) -Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3490-106">The message can be sent when the buffer is full or after the [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) function is called.</span></span>


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e3490-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3490-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3490-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e3490-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e3490-109">Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e3490-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies the buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="e3490-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e3490-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e3490-111">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e3490-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3490-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3490-112">Return Value</span></span>

<span data-ttu-id="e3490-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e3490-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3490-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3490-114">Remarks</span></span>

<span data-ttu-id="e3490-115">Der zurückgegebene Puffer ist möglicherweise nicht voll.</span><span class="sxs-lookup"><span data-stu-id="e3490-115">The returned buffer might not be full.</span></span> <span data-ttu-id="e3490-116">Verwenden Sie den **dwbyteslock** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die von *lpwvhdr* angegeben wird, um die Anzahl von Bytes zu bestimmen, die im zurückgegebenen Puffer aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e3490-116">Use the **dwBytesRecorded** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure specified by *lpwvhdr* to determine the number of bytes recorded into the returned buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3490-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3490-117">Requirements</span></span>



| <span data-ttu-id="e3490-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3490-118">Requirement</span></span> | <span data-ttu-id="e3490-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e3490-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3490-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3490-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3490-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3490-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3490-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3490-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3490-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3490-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3490-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3490-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3490-125"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3490-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3490-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3490-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3490-127">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="e3490-127">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="e3490-128">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="e3490-128">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

