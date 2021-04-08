---
title: MOM_OPEN Meldung (MMSYSTEM. h)
description: Die MOM- \_ Öffnungs Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn ein Ausgabegerät von MIDI geöffnet wird.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743361"
---
# <a name="mom_open-message"></a><span data-ttu-id="1047f-104">MOM- \_ Öffnungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="1047f-104">MOM\_OPEN message</span></span>

<span data-ttu-id="1047f-105">Die **MOM- \_ Öffnungs** Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn ein Ausgabegerät von MIDI geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="1047f-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="1047f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1047f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1047f-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1047f-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1047f-108">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="1047f-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="1047f-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1047f-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1047f-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="1047f-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1047f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1047f-111">Return Value</span></span>

<span data-ttu-id="1047f-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1047f-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1047f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1047f-113">Requirements</span></span>



| <span data-ttu-id="1047f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1047f-114">Requirement</span></span> | <span data-ttu-id="1047f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1047f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1047f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1047f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1047f-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1047f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1047f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1047f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1047f-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1047f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1047f-120">Header</span><span class="sxs-lookup"><span data-stu-id="1047f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1047f-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1047f-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1047f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1047f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1047f-123">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1047f-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





