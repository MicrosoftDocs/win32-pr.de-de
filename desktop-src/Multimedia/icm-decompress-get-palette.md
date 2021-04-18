---
title: ICM_DECOMPRESS_GET_PALETTE Meldung (VFW. h)
description: Die ICM- \_ \_ Dekomprimierung get \_ Palette Message fordert an, dass der Video Dekomprimierung-Treiber die Farbtabelle der Ausgabe BITMAPINFOHEADER-Struktur bereitstellt. Sie können diese Nachricht explizit oder mithilfe des icdecompressgetpalette-Makros senden.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- ICM_DECOMPRESS_GET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339362"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="35229-105">ICM- \_ Dekomprimierung \_ get- \_ palettennachricht</span><span class="sxs-lookup"><span data-stu-id="35229-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="35229-106">Die **ICM- \_ Dekomprimierung \_ get \_ Palette** Message fordert an, dass der Video Dekomprimierung-Treiber die Farbtabelle der Ausgabe [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="35229-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="35229-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressgetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="35229-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="35229-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="35229-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35229-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="35229-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="35229-110">Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="35229-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="35229-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="35229-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="35229-112">Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, die die Farbtabelle enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="35229-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="35229-113">Der für die Farbtabelle reservierte Speicherplatz beträgt immer mindestens 256 Farben.</span><span class="sxs-lookup"><span data-stu-id="35229-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="35229-114">Sie können NULL für diesen Parameter angeben, um nur die Größe der Farbtabelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="35229-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35229-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35229-115">Return Value</span></span>

<span data-ttu-id="35229-116">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="35229-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="35229-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35229-117">Remarks</span></span>

<span data-ttu-id="35229-118">Wenn *lpbioutput* ungleich NULL ist, legt der Treiber den **biclrused** -Member von [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) auf die Anzahl der Farben in der Farbtabelle fest.</span><span class="sxs-lookup"><span data-stu-id="35229-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="35229-119">Der Treiber füllt den **bmicolors** -Member von [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) mit den eigentlichen Farben aus.</span><span class="sxs-lookup"><span data-stu-id="35229-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="35229-120">Der Treiber sollte diese Nachricht nur dann unterstützen, wenn er eine andere Palette als die im Eingabeformat angegebene Palette verwendet.</span><span class="sxs-lookup"><span data-stu-id="35229-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="35229-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35229-121">Requirements</span></span>



| <span data-ttu-id="35229-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35229-122">Requirement</span></span> | <span data-ttu-id="35229-123">Wert</span><span class="sxs-lookup"><span data-stu-id="35229-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="35229-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35229-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35229-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35229-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="35229-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35229-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35229-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35229-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35229-128">Header</span><span class="sxs-lookup"><span data-stu-id="35229-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35229-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="35229-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35229-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35229-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35229-131">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="35229-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="35229-132">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="35229-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

