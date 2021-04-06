---
title: ICM_DECOMPRESSEX_BEGIN Meldung (VFW. h)
description: Die ICM \_ decompressex \_ Begin-Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Dekomprimierung von Daten vorzubereiten.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- ICM_DECOMPRESSEX_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742953"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="08a71-104">ICM- \_ decompressex- \_ Begin-Meldung</span><span class="sxs-lookup"><span data-stu-id="08a71-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="08a71-105">Die **ICM \_ decompressex \_ Begin** -Nachricht benachrichtigt einen Video Komprimierungs Treiber, um die Dekomprimierung von Daten vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="08a71-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="08a71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08a71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a71-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="08a71-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="08a71-108">Zeiger auf eine [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur, die die Eingabe-und Ausgabeformate enthält.</span><span class="sxs-lookup"><span data-stu-id="08a71-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="08a71-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="08a71-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="08a71-110">Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="08a71-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a71-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08a71-111">Return Value</span></span>

<span data-ttu-id="08a71-112">Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.</span><span class="sxs-lookup"><span data-stu-id="08a71-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a71-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08a71-113">Remarks</span></span>

<span data-ttu-id="08a71-114">Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge ausführen, damit [**ICM- \_ decompressex**](icm-decompressex.md) -Nachrichten effizient verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="08a71-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="08a71-115">Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="08a71-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="08a71-116">Die **ICM \_ decompressex \_ Begin** -und [**ICM \_ decompressex- \_ endmeldungen**](icm-decompressex-end.md) werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="08a71-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="08a71-117">Wenn Ihr Treiber **ICM \_ decompressex \_ Begin** empfängt, bevor die Dekomprimierung mit **ICM \_ decompressex \_ End** beendet wird, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="08a71-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a71-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08a71-118">Requirements</span></span>



| <span data-ttu-id="08a71-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08a71-119">Requirement</span></span> | <span data-ttu-id="08a71-120">Wert</span><span class="sxs-lookup"><span data-stu-id="08a71-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08a71-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08a71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08a71-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08a71-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08a71-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08a71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08a71-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08a71-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08a71-125">Header</span><span class="sxs-lookup"><span data-stu-id="08a71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a71-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a71-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a71-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08a71-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a71-128">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="08a71-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="08a71-129">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="08a71-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





