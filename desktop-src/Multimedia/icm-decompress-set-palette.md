---
title: ICM_DECOMPRESS_SET_PALETTE Meldung (VFW. h)
description: Die ICM \_ Decompress \_ Set \_ Palette-Meldung gibt eine Palette für einen Video Dekomprimierungs Treiber an, der verwendet werden soll, wenn er zu einem Format dekomprimiert, das eine Palette verwendet. Sie können diese Nachricht explizit oder mithilfe des icdecompresssetpalette-Makros senden.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- ICM_DECOMPRESS_SET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345502"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="1d4c3-105">ICM- \_ Dekomprimierungs Meldung zum Dekomprimieren der \_ \_ Palette</span><span class="sxs-lookup"><span data-stu-id="1d4c3-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="1d4c3-106">Die **ICM \_ Decompress \_ Set \_ Palette** -Meldung gibt eine Palette für einen Video Dekomprimierungs Treiber an, der verwendet werden soll, wenn er zu einem Format dekomprimiert, das eine Palette verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="1d4c3-107">Sie können diese Nachricht explizit oder mithilfe des [**icdecompresssetpalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="1d4c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d4c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d4c3-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbipalette*</span><span class="sxs-lookup"><span data-stu-id="1d4c3-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="1d4c3-110">Zeiger auf eine [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur, deren Farbtabelle die Farben enthält, die nach Möglichkeit verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="1d4c3-111">Sie können NULL angeben, um den Standardsatz von Ausgabe Farben zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d4c3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d4c3-112">Return Value</span></span>

<span data-ttu-id="1d4c3-113">Gibt ICERR \_ OK zurück, wenn der Debug-Treiber Bilder mithilfe des Satzes von Farben, die in der Palette angeordnet sind, genau in die vorgeschlagene Palette decokomprimieren kann.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="1d4c3-114">Gibt ICERR zurück, \_ wird andernfalls nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d4c3-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d4c3-115">Remarks</span></span>

<span data-ttu-id="1d4c3-116">Diese Meldung sollte sich nicht auf die bereits ausgeführte Dekomprimierung auswirken. Stattdessen sollten mit dieser Nachricht über gegebene Farben als Reaktion auf zukünftiges [**ICM \_ Decompress get- \_ \_ Format**](icm-decompress-get-format.md) und [**ICM \_ Decompress \_ get \_ Palette**](icm-decompress-get-palette.md) Messages zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="1d4c3-117">Farben werden in einer zukünftigen [**ICM- \_ Dekomprimierungs \_ Begin**](icm-decompress-begin.md) -Meldung an den dekomprimierungstreiber zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="1d4c3-118">Diese Meldung wird hauptsächlich verwendet, wenn ein Treiber Bilder auf den Bildschirm dekomprimiert und eine andere Anwendung, die eine Palette verwendet, im Vordergrund steht, wodurch der dekomprimierungstreiber an einen anderen Satz von Farben angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="1d4c3-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4c3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d4c3-119">Requirements</span></span>



| <span data-ttu-id="1d4c3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d4c3-120">Requirement</span></span> | <span data-ttu-id="1d4c3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1d4c3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1d4c3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d4c3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4c3-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4c3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1d4c3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d4c3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4c3-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d4c3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d4c3-126">Header</span><span class="sxs-lookup"><span data-stu-id="1d4c3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4c3-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4c3-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4c3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d4c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4c3-129">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="1d4c3-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="1d4c3-130">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="1d4c3-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

