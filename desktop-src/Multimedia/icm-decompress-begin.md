---
title: ICM_DECOMPRESS_BEGIN Meldung (VFW. h)
description: Die ICM \_ dekomprimieren \_ Begin-Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung von Daten vorzubereiten. Sie können diese Nachricht explizit oder mithilfe des icdecompressbegin-Makros senden.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- ICM_DECOMPRESS_BEGIN-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105435"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="a936b-105">ICM- \_ Dekomprimierungs \_ anfangs Nachricht</span><span class="sxs-lookup"><span data-stu-id="a936b-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="a936b-106">Die **ICM \_ dekomprimieren \_ Begin** -Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um die Dekomprimierung von Daten vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="a936b-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="a936b-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressbegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="a936b-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="a936b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a936b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a936b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="a936b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="a936b-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="a936b-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="a936b-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="a936b-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="a936b-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="a936b-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a936b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a936b-113">Return Value</span></span>

<span data-ttu-id="a936b-114">Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.</span><span class="sxs-lookup"><span data-stu-id="a936b-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a936b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a936b-115">Remarks</span></span>

<span data-ttu-id="a936b-116">Wenn der Treiber diese Nachricht empfängt, sollte er Puffer zuordnen und zeitaufwändige Vorgänge ausführen, damit [**ICM \_**](icm-decompress.md) -Nachrichten effizient verarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="a936b-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="a936b-117">Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a936b-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="a936b-118">Die **ICM- \_ Dekomprimierungs \_ Begin** -und [**ICM \_ Decompress \_**](icm-decompress-end.md) -Meldungen werden nicht geschachtelt.</span><span class="sxs-lookup"><span data-stu-id="a936b-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="a936b-119">Wenn der Treiber **ICM \_ Decompress \_** vor dem Beenden der Dekomprimierung mit **ICM \_ Decompress \_ Beenden** empfängt, sollte die Dekomprimierung mit neuen Parametern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a936b-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a936b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a936b-120">Requirements</span></span>



| <span data-ttu-id="a936b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a936b-121">Requirement</span></span> | <span data-ttu-id="a936b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a936b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a936b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a936b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a936b-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a936b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a936b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a936b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a936b-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a936b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a936b-127">Header</span><span class="sxs-lookup"><span data-stu-id="a936b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a936b-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a936b-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a936b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a936b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a936b-130">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="a936b-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a936b-131">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="a936b-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

