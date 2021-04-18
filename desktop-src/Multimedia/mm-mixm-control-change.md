---
title: MM_MIXM_CONTROL_CHANGE Meldung (MMSYSTEM. h)
description: Die Änderungen an der mm \_ mixm- \_ Steuerungs \_ Änderung werden von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Zustand eines Steuer Elements, das einer audiozeile zugeordnet ist, geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341004"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="de156-105">Meldung zum Ändern des mm \_ mixm- \_ Steuer Elements \_</span><span class="sxs-lookup"><span data-stu-id="de156-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="de156-106">Die **Änderungen an der mm \_ mixm- \_ Steuerungs \_ Änderung** werden von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Zustand eines Steuer Elements, das einer audiozeile zugeordnet ist, geändert hat.</span><span class="sxs-lookup"><span data-stu-id="de156-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="de156-107">Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="de156-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="de156-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de156-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de156-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hmixer*</span><span class="sxs-lookup"><span data-stu-id="de156-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="de156-110">Handle für das Mischgerät (**hmixer**), das die Benachrichtigungs Meldung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="de156-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="de156-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwcontrolid*</span><span class="sxs-lookup"><span data-stu-id="de156-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="de156-112">Steuerelement Bezeichner für das Mixer-Steuerelement, das den Zustand geändert hat</span><span class="sxs-lookup"><span data-stu-id="de156-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="de156-113">Dieser Bezeichner ist identisch mit dem **dwcontrolid** -Member der **mixercontrol**-Struktur, die von der Funktion "**mixergetlinecontrols**" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="de156-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de156-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de156-114">Remarks</span></span>

<span data-ttu-id="de156-115">Eine Anwendung muss ein Mischgerät öffnen und ein Rückruf Fenster angeben, um die Meldung zum **Ändern des mm \_ mixm- \_ Steuer \_** Elements zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="de156-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de156-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de156-116">Requirements</span></span>



| <span data-ttu-id="de156-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de156-117">Requirement</span></span> | <span data-ttu-id="de156-118">Wert</span><span class="sxs-lookup"><span data-stu-id="de156-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de156-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de156-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de156-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de156-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de156-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de156-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de156-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de156-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de156-123">Header</span><span class="sxs-lookup"><span data-stu-id="de156-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de156-124"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de156-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de156-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de156-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de156-126">Audiomixer</span><span class="sxs-lookup"><span data-stu-id="de156-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="de156-127">Audiomischmeldungen</span><span class="sxs-lookup"><span data-stu-id="de156-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





