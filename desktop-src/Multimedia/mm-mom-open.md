---
title: MM_MOM_OPEN Meldung (MMSYSTEM. h)
description: Die \_ Meldung zum \_ Öffnen von mm MOM wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geöffnet wird.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475078"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="2c755-104">Meldung zum Öffnen von mm \_ MOM \_</span><span class="sxs-lookup"><span data-stu-id="2c755-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="2c755-105">Die Meldung zum **\_ \_ Öffnen von mm MOM** wird an ein Fenster gesendet, wenn ein MIDI-Ausgabegerät geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2c755-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="2c755-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c755-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c755-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*houtput*</span><span class="sxs-lookup"><span data-stu-id="2c755-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="2c755-108">Handle für das MIDI-Ausgabegerät.</span><span class="sxs-lookup"><span data-stu-id="2c755-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="2c755-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="2c755-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="2c755-110">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="2c755-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c755-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c755-111">Return Value</span></span>

<span data-ttu-id="2c755-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2c755-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c755-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c755-113">Requirements</span></span>



| <span data-ttu-id="2c755-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c755-114">Requirement</span></span> | <span data-ttu-id="2c755-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2c755-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c755-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c755-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c755-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c755-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2c755-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c755-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c755-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c755-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2c755-120">Header</span><span class="sxs-lookup"><span data-stu-id="2c755-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c755-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c755-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c755-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c755-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c755-123">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="2c755-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





