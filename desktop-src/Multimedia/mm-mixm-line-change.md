---
title: MM_MIXM_LINE_CHANGE Meldung (MMSYSTEM. h)
description: Die Meldung der mm \_ -mixm- \_ Zeilen \_ Änderung wird von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Status einer audiozeile auf dem angegebenen Gerät geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für die angegebene Audiolinie aktualisieren.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345910"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="f34db-105">Meldung zur mm- \_ mixm- \_ Zeilen \_ Änderung</span><span class="sxs-lookup"><span data-stu-id="f34db-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="f34db-106">Die Meldung der **mm- \_ mixm- \_ Zeilen \_ Änderung** wird von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Status einer audiozeile auf dem angegebenen Gerät geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f34db-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="f34db-107">Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für die angegebene Audiolinie aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f34db-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="f34db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f34db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f34db-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hmixer*</span><span class="sxs-lookup"><span data-stu-id="f34db-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="f34db-110">Handle für das Mischgerät, das die Benachrichtigungs Meldung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="f34db-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="f34db-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwlineid*</span><span class="sxs-lookup"><span data-stu-id="f34db-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="f34db-112">Zeilen Bezeichner für die audiozeile, die den Zustand geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f34db-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="f34db-113">Dieser Bezeichner ist identisch mit dem **dwlineid** -Member der **mixerline**-Struktur, die von der **mixergetlineinfo**-Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f34db-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f34db-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f34db-114">Remarks</span></span>

<span data-ttu-id="f34db-115">Eine Anwendung muss ein Mischgerät öffnen und ein Rückruf Fenster angeben, um die **mm- \_ mixm- \_ Zeilen \_ Änderungs** Meldung zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="f34db-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f34db-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f34db-116">Requirements</span></span>



| <span data-ttu-id="f34db-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f34db-117">Requirement</span></span> | <span data-ttu-id="f34db-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f34db-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34db-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f34db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f34db-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f34db-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f34db-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f34db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f34db-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f34db-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f34db-123">Header</span><span class="sxs-lookup"><span data-stu-id="f34db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f34db-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f34db-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34db-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f34db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34db-126">Audiomixer</span><span class="sxs-lookup"><span data-stu-id="f34db-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="f34db-127">Audiomischmeldungen</span><span class="sxs-lookup"><span data-stu-id="f34db-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





