---
title: WOM_DONE Meldung (MMSYSTEM. h)
description: '\_Wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird, wird die gesendete WOM-Nachricht an eine "Waveform-Audioausgabe"-Rückruffunktion gesendet.'
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103026"
---
# <a name="wom_done-message"></a><span data-ttu-id="44549-104">WOM- \_ done-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44549-104">WOM\_DONE message</span></span>

<span data-ttu-id="44549-105">Wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird, wird die gesendete **WOM \_** -Nachricht an eine "Waveform-Audioausgabe"-Rückruffunktion gesendet.</span><span class="sxs-lookup"><span data-stu-id="44549-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="44549-106">Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der [**wavesetzset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44549-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="44549-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="44549-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44549-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="44549-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="44549-109">Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="44549-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="44549-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="44549-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="44549-111">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="44549-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44549-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44549-112">Return Value</span></span>

<span data-ttu-id="44549-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="44549-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="44549-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44549-114">Requirements</span></span>



| <span data-ttu-id="44549-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44549-115">Requirement</span></span> | <span data-ttu-id="44549-116">Wert</span><span class="sxs-lookup"><span data-stu-id="44549-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44549-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44549-117">Minimum supported client</span></span><br/> | <span data-ttu-id="44549-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44549-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="44549-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44549-119">Minimum supported server</span></span><br/> | <span data-ttu-id="44549-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44549-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="44549-121">Header</span><span class="sxs-lookup"><span data-stu-id="44549-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="44549-122"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44549-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44549-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44549-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44549-124">Waveform-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="44549-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="44549-125">Wellenform Meldungen</span><span class="sxs-lookup"><span data-stu-id="44549-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

