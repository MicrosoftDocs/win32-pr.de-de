---
title: MM_MOM_DONE Meldung (MMSYSTEM. h)
description: Die \_ von mm MOM \_ durchgeführte Nachricht wird an ein Fenster gesendet, wenn der angegebene System exklusive System-oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040212"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="ba962-104">Nach \_ richten von mm MOM \_</span><span class="sxs-lookup"><span data-stu-id="ba962-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="ba962-105">Die von **mm \_ MOM \_ durch** geführte Nachricht wird an ein Fenster gesendet, wenn der angegebene System exklusive System-oder Streampuffer wiedergegeben wurde und an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba962-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="ba962-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba962-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba962-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*houtput*</span><span class="sxs-lookup"><span data-stu-id="ba962-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="ba962-108">Handle für das MIDI-Ausgabegerät, das den Puffer wiedergegeben hat.</span><span class="sxs-lookup"><span data-stu-id="ba962-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba962-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*</span><span class="sxs-lookup"><span data-stu-id="ba962-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="ba962-110">Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Puffer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba962-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba962-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba962-111">Return Value</span></span>

<span data-ttu-id="ba962-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ba962-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba962-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba962-113">Requirements</span></span>



| <span data-ttu-id="ba962-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba962-114">Requirement</span></span> | <span data-ttu-id="ba962-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ba962-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba962-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba962-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba962-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba962-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ba962-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba962-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba962-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba962-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ba962-120">Header</span><span class="sxs-lookup"><span data-stu-id="ba962-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba962-121"><dt>MMSYSTEM. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba962-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba962-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba962-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba962-123">MIDI-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ba962-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

