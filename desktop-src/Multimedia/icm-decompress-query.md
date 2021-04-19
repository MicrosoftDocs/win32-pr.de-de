---
title: ICM_DECOMPRESS_QUERY Meldung (VFW. h)
description: Die ICM \_ dekomprimieren- \_ Abfrage Nachricht fragt einen Video Dekomprimierung-Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- ICM_DECOMPRESS_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342867"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="7c60f-104">ICM- \_ \_ Abfrage Nachricht dekomprimieren</span><span class="sxs-lookup"><span data-stu-id="7c60f-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="7c60f-105">Die **ICM \_ dekomprimieren- \_ Abfrage** Nachricht fragt einen Video Dekomprimierung-Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat dekomprimiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c60f-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="7c60f-106">Sie können diese Nachricht explizit oder mithilfe des [**icdecompressquery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="7c60f-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="7c60f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c60f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c60f-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="7c60f-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="7c60f-109">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="7c60f-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="7c60f-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="7c60f-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="7c60f-111">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="7c60f-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="7c60f-112">Sie können NULL für diesen Parameter angeben, um anzugeben, dass ein beliebiges Ausgabeformat zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7c60f-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c60f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c60f-113">Return Value</span></span>

<span data-ttu-id="7c60f-114">Gibt ICERR \_ OK zurück, wenn die angegebene Dekomprimierung unterstützt wird oder andernfalls ICERR \_ badformat.</span><span class="sxs-lookup"><span data-stu-id="7c60f-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c60f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c60f-115">Requirements</span></span>



| <span data-ttu-id="7c60f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c60f-116">Requirement</span></span> | <span data-ttu-id="7c60f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7c60f-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7c60f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c60f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c60f-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c60f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7c60f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c60f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c60f-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c60f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7c60f-122">Header</span><span class="sxs-lookup"><span data-stu-id="7c60f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c60f-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c60f-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c60f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c60f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c60f-125">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="7c60f-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7c60f-126">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="7c60f-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

