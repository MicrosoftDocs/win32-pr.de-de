---
title: MOM_CLOSE Meldung (MMSYSTEM. h)
description: Die MOM- \_ Schließen-Nachricht wird an eine Funktion für die Ausgabe Rückruffunktion von MIDI gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957086"
---
# <a name="mom_close-message"></a><span data-ttu-id="e8941-104">Meldung zum Schließen der MOM \_</span><span class="sxs-lookup"><span data-stu-id="e8941-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="e8941-105">Die **MOM- \_ Schließen** -Nachricht wird an eine Funktion für die Ausgabe Rückruffunktion von MIDI gesendet, wenn ein MIDI-Ausgabegerät geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="e8941-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e8941-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8941-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e8941-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e8941-108">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="e8941-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="e8941-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e8941-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e8941-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="e8941-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8941-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8941-111">Return Value</span></span>

<span data-ttu-id="e8941-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e8941-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8941-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8941-113">Remarks</span></span>

<span data-ttu-id="e8941-114">Das Geräte Handle ist nicht mehr gültig, nachdem diese Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e8941-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8941-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8941-115">Requirements</span></span>



| <span data-ttu-id="e8941-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8941-116">Requirement</span></span> | <span data-ttu-id="e8941-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e8941-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8941-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8941-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e8941-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8941-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e8941-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8941-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e8941-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8941-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e8941-122">Header</span><span class="sxs-lookup"><span data-stu-id="e8941-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8941-123"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8941-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8941-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8941-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8941-125">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="e8941-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





