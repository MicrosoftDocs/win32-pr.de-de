---
title: ICM_DECOMPRESS_GET_FORMAT Meldung (VFW. h)
description: Die ICM \_ Decompress \_ get \_ Format-Meldung fordert das Ausgabeformat der dekomprimierten Daten von einem videodecompression-Treiber an. Sie können diese Nachricht explizit oder mithilfe des icdecompressgetformat-Makros senden.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- ICM_DECOMPRESS_GET_FORMAT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040880"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="7852d-105">ICM \_ Decompress \_ get \_ Format-Meldung</span><span class="sxs-lookup"><span data-stu-id="7852d-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="7852d-106">Die **ICM \_ Decompress \_ get \_ Format** -Meldung fordert das Ausgabeformat der dekomprimierten Daten von einem videodecompression-Treiber an.</span><span class="sxs-lookup"><span data-stu-id="7852d-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="7852d-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7852d-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="7852d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7852d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7852d-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="7852d-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7852d-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="7852d-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="7852d-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="7852d-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="7852d-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7852d-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="7852d-113">Sie können NULL angeben, um nur die Größe des Ausgabeformats anzufordern, wie im " [**icdecompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) "-Makro.</span><span class="sxs-lookup"><span data-stu-id="7852d-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7852d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7852d-114">Return Value</span></span>

<span data-ttu-id="7852d-115">Wenn *lpbioutput* gleich 0 (null) ist, wird die Größe der Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7852d-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="7852d-116">Wenn *lpbioutput* ungleich NULL ist, gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7852d-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7852d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7852d-117">Remarks</span></span>

<span data-ttu-id="7852d-118">Wenn *lpbioutput* ungleich NULL ist, sollte der Treiber die [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur mit dem Standardausgabeformat auffüllen, das dem für *lpbiinput* angegebenen Eingabeformat entspricht.</span><span class="sxs-lookup"><span data-stu-id="7852d-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="7852d-119">Wenn der-Kompressor mehrere Formate liefern kann, sollte das Standardformat das Standardformat aufweisen, das die größte Menge an Informationen beibehält.</span><span class="sxs-lookup"><span data-stu-id="7852d-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7852d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7852d-120">Requirements</span></span>



| <span data-ttu-id="7852d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7852d-121">Requirement</span></span> | <span data-ttu-id="7852d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7852d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7852d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7852d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7852d-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7852d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7852d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7852d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7852d-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7852d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7852d-127">Header</span><span class="sxs-lookup"><span data-stu-id="7852d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7852d-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7852d-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7852d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7852d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7852d-130">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="7852d-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7852d-131">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="7852d-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

