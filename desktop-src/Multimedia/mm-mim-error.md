---
title: MM_MIM_ERROR Meldung (MMSYSTEM. h)
description: Die mm \_ MIM- \_ Fehlermeldung wird an ein Fenster gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76b45988259601b40a804f9eb8acfbb085bddcda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103034"
---
# <a name="mm_mim_error-message"></a><span data-ttu-id="4247c-104">MM \_ MIM- \_ Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="4247c-104">MM\_MIM\_ERROR message</span></span>

<span data-ttu-id="4247c-105">Die **mm \_ MIM- \_ Fehler** Meldung wird an ein Fenster gesendet, wenn eine ungültige MIDI-Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="4247c-105">The **MM\_MIM\_ERROR** message is sent to a window when an invalid MIDI message is received.</span></span>


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a><span data-ttu-id="4247c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4247c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4247c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hinput*</span><span class="sxs-lookup"><span data-stu-id="4247c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="4247c-108">Handle für das MIDI-Eingabegerät, das die ungültige Nachricht empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="4247c-108">Handle to the MIDI input device that received the invalid message.</span></span>

</dd> <dt>

<span data-ttu-id="4247c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lmidimessage*</span><span class="sxs-lookup"><span data-stu-id="4247c-109"><span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*</span></span>
</dt> <dd>

<span data-ttu-id="4247c-110">Ungültige MIDI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4247c-110">Invalid MIDI message.</span></span> <span data-ttu-id="4247c-111">Die Nachricht wird in einem **DWORD** -Wert mit dem ersten Byte der Nachricht im nieder wertigen Byte verpackt.</span><span class="sxs-lookup"><span data-stu-id="4247c-111">The message is packed into a **DWORD** value with the first byte of the message in the low-order byte.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4247c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4247c-112">Return Value</span></span>

<span data-ttu-id="4247c-113">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4247c-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4247c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4247c-114">Requirements</span></span>



| <span data-ttu-id="4247c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4247c-115">Requirement</span></span> | <span data-ttu-id="4247c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4247c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4247c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4247c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4247c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4247c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4247c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4247c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4247c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4247c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4247c-121">Header</span><span class="sxs-lookup"><span data-stu-id="4247c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4247c-122"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4247c-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4247c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4247c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4247c-124">Digital Instrumentation Digital Interface (MIDI)</span><span class="sxs-lookup"><span data-stu-id="4247c-124">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="4247c-125">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4247c-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





