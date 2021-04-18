---
title: MM_MOM_CLOSE Meldung (MMSYSTEM. h)
description: Die \_ Meldung zum \_ Schließen von mm MOM wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475501"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="f1a77-104">Meldung zum Schließen von mm \_ MOM \_</span><span class="sxs-lookup"><span data-stu-id="f1a77-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="f1a77-105">Die Meldung zum **\_ \_ Schließen von mm MOM** wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f1a77-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f1a77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a77-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*houtput*</span><span class="sxs-lookup"><span data-stu-id="f1a77-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="f1a77-108">Handle für das MIDI-Ausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="f1a77-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="f1a77-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="f1a77-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f1a77-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="f1a77-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1a77-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f1a77-111">Return Value</span></span>

<span data-ttu-id="f1a77-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f1a77-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a77-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1a77-113">Remarks</span></span>

<span data-ttu-id="f1a77-114">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f1a77-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a77-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1a77-115">Requirements</span></span>



| <span data-ttu-id="f1a77-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1a77-116">Requirement</span></span> | <span data-ttu-id="f1a77-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f1a77-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a77-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1a77-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a77-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1a77-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1a77-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f1a77-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a77-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f1a77-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1a77-122">Header</span><span class="sxs-lookup"><span data-stu-id="f1a77-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1a77-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1a77-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a77-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1a77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a77-125">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f1a77-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





