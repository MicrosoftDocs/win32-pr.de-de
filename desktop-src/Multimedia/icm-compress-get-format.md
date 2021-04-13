---
title: ICM_COMPRESS_GET_FORMAT Meldung (VFW. h)
description: Die ICM \_ Compress \_ get \_ Format-Meldung fordert das Ausgabeformat der komprimierten Daten von einem Video Komprimierungs Treiber an. Sie können diese Nachricht explizit oder mithilfe des iccompressgetformat-Makros senden.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- ICM_COMPRESS_GET_FORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478468"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="4e9a3-105">ICM \_ Compress \_ - \_ Format Meldung "Get"</span><span class="sxs-lookup"><span data-stu-id="4e9a3-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="4e9a3-106">Die **ICM \_ Compress \_ get \_ Format** -Meldung fordert das Ausgabeformat der komprimierten Daten von einem Video Komprimierungs Treiber an.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="4e9a3-107">Sie können diese Nachricht explizit oder mithilfe des [**iccompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="4e9a3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e9a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e9a3-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="4e9a3-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="4e9a3-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="4e9a3-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="4e9a3-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="4e9a3-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="4e9a3-113">Sie können NULL für diesen Parameter angeben, um nur die Größe des Ausgabeformats anzufordern, wie im " [**iccompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) "-Makro.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e9a3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e9a3-114">Return Value</span></span>

<span data-ttu-id="4e9a3-115">Wenn *lpbioutput* gleich 0 (null) ist, wird die Größe der Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="4e9a3-116">Wenn *lpbioutput* ungleich NULL ist, gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e9a3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e9a3-117">Remarks</span></span>

<span data-ttu-id="4e9a3-118">Wenn *lpbioutput* ungleich NULL ist, sollte der Treiber die [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur mit dem Standardausgabeformat auffüllen, das dem für *lpbiinput* angegebenen Eingabeformat entspricht.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="4e9a3-119">Wenn der-Kompressor mehrere Formate liefern kann, sollte das Standardformat das Standardformat aufweisen, das die größte Menge an Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="4e9a3-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e9a3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e9a3-120">Requirements</span></span>



| <span data-ttu-id="4e9a3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e9a3-121">Requirement</span></span> | <span data-ttu-id="4e9a3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4e9a3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4e9a3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e9a3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4e9a3-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e9a3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4e9a3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e9a3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4e9a3-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e9a3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4e9a3-127">Header</span><span class="sxs-lookup"><span data-stu-id="4e9a3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e9a3-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e9a3-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e9a3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e9a3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9a3-130">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="4e9a3-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4e9a3-131">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4e9a3-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

