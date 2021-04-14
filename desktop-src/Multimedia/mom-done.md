---
title: MOM_DONE Meldung (mciapi. h)
description: Die MOM \_ -done-Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn der angegebene System exklusive oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391780"
---
# <a name="mom_done-message"></a><span data-ttu-id="0d1fd-104">MOM- \_ Nachricht abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="0d1fd-104">MOM\_DONE message</span></span>

<span data-ttu-id="0d1fd-105">Die **MOM- \_ done** -Nachricht wird an eine Funktion für die Funktion "MIDI-Ausgabe" gesendet, wenn der angegebene System exklusive oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d1fd-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="0d1fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d1fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d1fd-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="0d1fd-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="0d1fd-108">Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d1fd-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0d1fd-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0d1fd-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0d1fd-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="0d1fd-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d1fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d1fd-111">Return Value</span></span>

<span data-ttu-id="0d1fd-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0d1fd-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1fd-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d1fd-113">Requirements</span></span>



| <span data-ttu-id="0d1fd-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d1fd-114">Requirement</span></span> | <span data-ttu-id="0d1fd-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0d1fd-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1fd-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d1fd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1fd-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d1fd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d1fd-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d1fd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1fd-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d1fd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d1fd-120">Header</span><span class="sxs-lookup"><span data-stu-id="0d1fd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1fd-121"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1fd-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1fd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d1fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1fd-123">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="0d1fd-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

