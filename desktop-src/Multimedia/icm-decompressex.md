---
title: ICM_DECOMPRESSEX Meldung (VFW. h)
description: Durch die ICM \_ decompressex-Nachricht wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen direkt auf dem Bildschirm zu dekomprimieren, auf ein aufwärts Bild aufgeschalteter DIB zu dekomprimieren oder mit Quell-und Ziel Rechtecke beschriebene Bilder zu dekomprimieren.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- ICM_DECOMPRESSEX-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040877"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="396c0-104">ICM- \_ decompressex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="396c0-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="396c0-105">Durch die **ICM \_ decompressex** -Nachricht wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen direkt auf dem Bildschirm zu dekomprimieren, auf ein aufwärts Bild aufgeschalteter DIB zu dekomprimieren oder mit Quell-und Ziel Rechtecke beschriebene Bilder zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="396c0-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="396c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="396c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396c0-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="396c0-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="396c0-108">Zeiger auf eine [**icbecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="396c0-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="396c0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="396c0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="396c0-110">Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="396c0-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="396c0-111">Return Value</span></span>

<span data-ttu-id="396c0-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="396c0-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="396c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="396c0-113">Remarks</span></span>

<span data-ttu-id="396c0-114">Diese Meldung ähnelt [**ICM \_ Decompress**](icm-decompress.md) , mit dem Unterschied, dass Sie die [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur verwendet, um die dekomprimierungsinformationen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="396c0-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="396c0-115">Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="396c0-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="396c0-116">Der Treiber gibt einen Fehler zurück, wenn diese Nachricht vor der [**ICM- \_ decompressex- \_ Begin**](icm-decompressex-begin.md) -Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="396c0-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="396c0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="396c0-117">Requirements</span></span>



| <span data-ttu-id="396c0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="396c0-118">Requirement</span></span> | <span data-ttu-id="396c0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="396c0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="396c0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="396c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="396c0-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="396c0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="396c0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="396c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="396c0-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="396c0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="396c0-124">Header</span><span class="sxs-lookup"><span data-stu-id="396c0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="396c0-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="396c0-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="396c0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="396c0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396c0-127">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="396c0-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="396c0-128">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="396c0-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





