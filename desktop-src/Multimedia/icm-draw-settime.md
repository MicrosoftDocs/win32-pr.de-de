---
title: ICM_DRAW_SETTIME Meldung (VFW. h)
description: Der ICM \_ Draw \_ setTime stellt Synchronisierungs Informationen für einen renderingtreiber bereit, der die zeitliche Steuerung von Zeichnungs Frames behandelt.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- ICM_DRAW_SETTIME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858810"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="67693-104">ICM \_ Draw- \_ setTime-Meldung</span><span class="sxs-lookup"><span data-stu-id="67693-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="67693-105">Der **ICM \_ Draw \_ setTime** stellt Synchronisierungs Informationen für einen renderingtreiber bereit, der die zeitliche Steuerung von Zeichnungs Frames behandelt.</span><span class="sxs-lookup"><span data-stu-id="67693-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="67693-106">Die Synchronisierungs Informationen sind die Beispiel Nummer des Frames, der gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="67693-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="67693-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawsettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="67693-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="67693-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67693-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67693-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lptime*</span><span class="sxs-lookup"><span data-stu-id="67693-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="67693-110">Die Stichproben Nummer des zu Rendering enden Frames.</span><span class="sxs-lookup"><span data-stu-id="67693-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67693-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67693-111">Return Value</span></span>

<span data-ttu-id="67693-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="67693-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="67693-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67693-113">Remarks</span></span>

<span data-ttu-id="67693-114">Normalerweise vergleicht der Treiber den angegebenen Wert mit der dem Zeitpunkt der internen Uhr zugeordneten Frame Nummer und versucht, die beiden zu synchronisieren, wenn der Unterschied signifikant ist.</span><span class="sxs-lookup"><span data-stu-id="67693-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="67693-115">Verwenden Sie diese Meldung, wenn die Hardware eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt und die Hardware auf einem externen Synchronisierungs Signal basiert (die Hardware wird nicht als Synchronisierungs Master verwendet).</span><span class="sxs-lookup"><span data-stu-id="67693-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="67693-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67693-116">Requirements</span></span>



| <span data-ttu-id="67693-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67693-117">Requirement</span></span> | <span data-ttu-id="67693-118">Wert</span><span class="sxs-lookup"><span data-stu-id="67693-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67693-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67693-119">Minimum supported client</span></span><br/> | <span data-ttu-id="67693-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67693-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="67693-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67693-121">Minimum supported server</span></span><br/> | <span data-ttu-id="67693-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67693-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67693-123">Header</span><span class="sxs-lookup"><span data-stu-id="67693-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="67693-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="67693-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67693-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67693-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67693-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="67693-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="67693-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="67693-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





