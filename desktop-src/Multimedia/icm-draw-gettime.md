---
title: ICM_DRAW_GETTIME Meldung (VFW. h)
description: Die ICM \_ Draw \_ GetTime-Nachricht fordert einen renderingtreiber an, der die zeitliche Steuerung der Zeichnungsrahmen steuert, um den aktuellen Wert der internen Uhr zurückzugeben. Sie können diese Nachricht explizit oder mithilfe des icdrawgettime-Makros senden.
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f756a76408d01cb72ee1762f14bb8a5eab19e475
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338552"
---
# <a name="icm_draw_gettime-message"></a><span data-ttu-id="fefaf-105">ICM \_ Zeichnen \_ GetTime-Meldung</span><span class="sxs-lookup"><span data-stu-id="fefaf-105">ICM\_DRAW\_GETTIME message</span></span>

<span data-ttu-id="fefaf-106">Die **ICM \_ Draw \_ GetTime** -Nachricht fordert einen renderingtreiber an, der die zeitliche Steuerung der Zeichnungsrahmen steuert, um den aktuellen Wert der internen Uhr zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fefaf-106">The **ICM\_DRAW\_GETTIME** message requests a rendering driver that controls the timing of drawing frames to return the current value of its internal clock.</span></span> <span data-ttu-id="fefaf-107">Sie können diese Nachricht explizit oder mithilfe des [**icdrawgettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="fefaf-107">You can send this message explicitly or by using the [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) macro.</span></span>


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="fefaf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fefaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fefaf-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lpltime*</span><span class="sxs-lookup"><span data-stu-id="fefaf-109"><span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*</span></span>
</dt> <dd>

<span data-ttu-id="fefaf-110">Adresse, die die aktuelle Uhrzeit enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="fefaf-110">Address to contain the current time.</span></span> <span data-ttu-id="fefaf-111">Der Rückgabewert muss in Samples angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fefaf-111">The return value should be specified in samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fefaf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fefaf-112">Return Value</span></span>

<span data-ttu-id="fefaf-113">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fefaf-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fefaf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fefaf-114">Remarks</span></span>

<span data-ttu-id="fefaf-115">Diese Meldung wird in der Regel von Hardware unterstützt, die eine eigene asynchrone Dekomprimierung, zeitliche Steuerung und Zeichnung ausführt.</span><span class="sxs-lookup"><span data-stu-id="fefaf-115">This message is generally supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span> <span data-ttu-id="fefaf-116">Die Nachricht kann auch gesendet werden, wenn die Hardware als Synchronisierungs Master verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fefaf-116">The message can also be sent if the hardware is being used as the synchronization master.</span></span>

## <a name="requirements"></a><span data-ttu-id="fefaf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fefaf-117">Requirements</span></span>



| <span data-ttu-id="fefaf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fefaf-118">Requirement</span></span> | <span data-ttu-id="fefaf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fefaf-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fefaf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fefaf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fefaf-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fefaf-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fefaf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fefaf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fefaf-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fefaf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fefaf-124">Header</span><span class="sxs-lookup"><span data-stu-id="fefaf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fefaf-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fefaf-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefaf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fefaf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefaf-127">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="fefaf-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="fefaf-128">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="fefaf-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





