---
title: ICM_DECOMPRESSEX_QUERY Meldung (VFW. h)
description: Die ICM \_ decompressex- \_ Abfrage Nachricht fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.
ms.assetid: 7778a52d-2ed8-495c-8656-c6beb1863499
keywords:
- ICM_DECOMPRESSEX_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b2ef5999b9e0619ccbd9ccabd9bc5223b3bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859142"
---
# <a name="icm_decompressex_query-message"></a><span data-ttu-id="0ccc3-104">ICM- \_ decompressex- \_ Abfrage Nachricht</span><span class="sxs-lookup"><span data-stu-id="0ccc3-104">ICM\_DECOMPRESSEX\_QUERY message</span></span>

<span data-ttu-id="0ccc3-105">Die **ICM \_ decompressex- \_ Abfrage** Nachricht fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0ccc3-105">The **ICM\_DECOMPRESSEX\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span>


```C++
ICM_DECOMPRESSEX_QUERY 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="0ccc3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ccc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ccc3-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="0ccc3-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="0ccc3-108">Zeiger auf eine [**icdecompressex**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="0ccc3-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="0ccc3-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="0ccc3-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="0ccc3-110">Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="0ccc3-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ccc3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ccc3-111">Return Value</span></span>

<span data-ttu-id="0ccc3-112">Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.</span><span class="sxs-lookup"><span data-stu-id="0ccc3-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ccc3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ccc3-113">Requirements</span></span>



| <span data-ttu-id="0ccc3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ccc3-114">Requirement</span></span> | <span data-ttu-id="0ccc3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="0ccc3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ccc3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ccc3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ccc3-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ccc3-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ccc3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ccc3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ccc3-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ccc3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ccc3-120">Header</span><span class="sxs-lookup"><span data-stu-id="0ccc3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ccc3-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ccc3-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ccc3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ccc3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ccc3-123">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="0ccc3-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0ccc3-124">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="0ccc3-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





