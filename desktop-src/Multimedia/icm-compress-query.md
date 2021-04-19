---
title: ICM_COMPRESS_QUERY Meldung (VFW. h)
description: Die ICM \_ - \_ Abfrage Nachricht zum Komprimieren fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat komprimiert werden kann.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- ICM_COMPRESS_QUERY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346747"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="8d158-104">ICM \_ - \_ Abfrage Nachricht komprimieren</span><span class="sxs-lookup"><span data-stu-id="8d158-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="8d158-105">Die **ICM \_ - \_ Abfrage** Nachricht zum Komprimieren fragt einen Video Komprimierungs Treiber ab, um zu bestimmen, ob ein bestimmtes Eingabeformat unterstützt wird oder ob ein bestimmtes Eingabeformat in ein bestimmtes Ausgabeformat komprimiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d158-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="8d158-106">Sie können diese Nachricht explizit oder mithilfe des [**iccompressquery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8d158-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="8d158-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d158-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d158-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="8d158-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="8d158-109">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="8d158-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="8d158-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="8d158-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="8d158-111">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="8d158-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="8d158-112">Sie können NULL für diesen Parameter angeben, um anzugeben, dass ein beliebiges Ausgabeformat zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8d158-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d158-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d158-113">Return Value</span></span>

<span data-ttu-id="8d158-114">Gibt ICERR \_ OK zurück, wenn die angegebene Komprimierung unterstützt wird, andernfalls wird ICERR \_ badformat zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8d158-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d158-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d158-115">Remarks</span></span>

<span data-ttu-id="8d158-116">Wenn ein Treiber diese Nachricht empfängt, sollte er die mit " *lpbiinput* " verknüpfte [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur untersuchen, um zu bestimmen, ob er das Eingabeformat komprimieren kann.</span><span class="sxs-lookup"><span data-stu-id="8d158-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d158-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d158-117">Requirements</span></span>



| <span data-ttu-id="8d158-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d158-118">Requirement</span></span> | <span data-ttu-id="8d158-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8d158-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d158-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d158-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d158-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d158-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d158-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d158-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d158-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d158-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d158-124">Header</span><span class="sxs-lookup"><span data-stu-id="8d158-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d158-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d158-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d158-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d158-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d158-127">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="8d158-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8d158-128">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="8d158-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

