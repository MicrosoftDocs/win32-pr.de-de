---
title: ICM_DRAW_SUGGESTFORMAT Meldung (VFW. h)
description: Die ICM \_ Draw- \_ Message-Nachricht fragt einen renderingtreiber ab, um ein dekomprimiertes Format vorzuschlagen, das gezeichnet werden kann.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- ICM_DRAW_SUGGESTFORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475702"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="09576-104">ICM \_ Draw-Vorschlags \_ Format Meldung</span><span class="sxs-lookup"><span data-stu-id="09576-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="09576-105">Die **ICM \_ Draw \_** -Message-Nachricht fragt einen renderingtreiber ab, um ein dekomprimiertes Format vorzuschlagen, das gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="09576-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="09576-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09576-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwvorschlagen*</span><span class="sxs-lookup"><span data-stu-id="09576-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="09576-108">Zeiger auf eine [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="09576-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="09576-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="09576-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="09576-110">Größe (in Bytes) von [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span><span class="sxs-lookup"><span data-stu-id="09576-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09576-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09576-111">Return Value</span></span>

<span data-ttu-id="09576-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="09576-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="09576-113">Wenn der **lpbisuggest** -Member der [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur **null** ist, gibt diese Meldung die Menge an Arbeitsspeicher zurück, die für das vorgeschlagene Format erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="09576-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="09576-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09576-114">Remarks</span></span>

<span data-ttu-id="09576-115">Der Treiber sollte das im **lpbiin** -Member der [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) -Struktur angegebene Format untersuchen und den **lpbisuggest** -Member verwenden, um ein Format zurückzugeben, das es zeichnen kann.</span><span class="sxs-lookup"><span data-stu-id="09576-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="09576-116">Das Ausgabeformat sollte so viele Daten wie möglich aus dem Eingabeformat erhalten.</span><span class="sxs-lookup"><span data-stu-id="09576-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="09576-117">Optional kann der Treiber den installierbaren kompressorhandle verwenden, der im **hicdecompressor** -Member von [**icdrawvorschlagen**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) übergeben wurde, um komplexere Auswahlmöglichkeiten zu treffen.</span><span class="sxs-lookup"><span data-stu-id="09576-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="09576-118">Wenn das Eingabeformat z. b. 24-Bit-JPEG-Daten ist, könnte ein Renderer den Dekompressor Abfragen, um herauszufinden, ob er in ein YUV-Format dekomprimiert werden kann (das möglicherweise effizienter gezeichnet wird), bevor das zu verwendende Format ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="09576-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="09576-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09576-119">Requirements</span></span>



| <span data-ttu-id="09576-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09576-120">Requirement</span></span> | <span data-ttu-id="09576-121">Wert</span><span class="sxs-lookup"><span data-stu-id="09576-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="09576-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09576-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09576-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09576-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="09576-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09576-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09576-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09576-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="09576-126">Header</span><span class="sxs-lookup"><span data-stu-id="09576-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="09576-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="09576-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09576-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09576-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09576-129">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="09576-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="09576-130">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="09576-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





