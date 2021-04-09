---
title: ICM_COMPRESS_GET_SIZE Meldung (VFW. h)
description: Mit der ICM- \_ \_ \_ Komprimierung Get Size wird angefordert, dass der Video Komprimierungs Treiber die maximale Größe von einem Datenrahmen bei Komprimierung in das angegebene Ausgabeformat bereitstellt. Sie können diese Nachricht explizit oder mithilfe des iccompressgetsize-Makros senden.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- ICM_COMPRESS_GET_SIZE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956974"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="8952f-105">ICM- \_ Komprimierung \_ get \_ size-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8952f-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="8952f-106">Mit der ICM-Komprimierung **\_ \_ get \_ size** wird angefordert, dass der Video Komprimierungs Treiber die maximale Größe von einem Datenrahmen bei Komprimierung in das angegebene Ausgabeformat bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8952f-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="8952f-107">Sie können diese Nachricht explizit oder mithilfe des [**iccompressgetsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="8952f-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="8952f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8952f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8952f-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiinput*</span><span class="sxs-lookup"><span data-stu-id="8952f-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="8952f-110">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Eingabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="8952f-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="8952f-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbioutput*</span><span class="sxs-lookup"><span data-stu-id="8952f-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="8952f-112">Zeiger auf eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur, die das Ausgabeformat enthält.</span><span class="sxs-lookup"><span data-stu-id="8952f-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8952f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8952f-113">Return Value</span></span>

<span data-ttu-id="8952f-114">Gibt die maximale Anzahl von Bytes zurück, die ein einzelner komprimierter Frame belegen kann.</span><span class="sxs-lookup"><span data-stu-id="8952f-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="8952f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8952f-115">Remarks</span></span>

<span data-ttu-id="8952f-116">Normalerweise senden Anwendungen diese Nachricht, um zu bestimmen, wie groß ein Puffer für den komprimierten Frame ist.</span><span class="sxs-lookup"><span data-stu-id="8952f-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="8952f-117">Der Treiber sollte die Größe des größtmöglichen Frames basierend auf den Eingabe-und Ausgabeformaten berechnen.</span><span class="sxs-lookup"><span data-stu-id="8952f-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="8952f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8952f-118">Requirements</span></span>



| <span data-ttu-id="8952f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8952f-119">Requirement</span></span> | <span data-ttu-id="8952f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8952f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8952f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8952f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8952f-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8952f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8952f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8952f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8952f-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8952f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8952f-125">Header</span><span class="sxs-lookup"><span data-stu-id="8952f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8952f-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8952f-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8952f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8952f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8952f-128">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="8952f-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8952f-129">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="8952f-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

