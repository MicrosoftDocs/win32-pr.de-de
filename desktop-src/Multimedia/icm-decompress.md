---
title: ICM_DECOMPRESS Meldung (VFW. h)
description: Die ICM \_ dekomprimieren-Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um einen Datenrahmen in einen Anwendungs definierten Puffer zu dekomprimieren.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- ICM_DECOMPRESS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040878"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="99e3f-104">ICM- \_ Dekomprimierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="99e3f-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="99e3f-105">Die **ICM \_ dekomprimieren** -Meldung benachrichtigt einen Video Dekomprimierung-Treiber, um einen Datenrahmen in einen Anwendungs definierten Puffer zu dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="99e3f-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="99e3f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99e3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e3f-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="99e3f-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="99e3f-108">Zeiger auf eine [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="99e3f-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="99e3f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="99e3f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="99e3f-110">Größe von [**icdebug**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="99e3f-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e3f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99e3f-111">Return Value</span></span>

<span data-ttu-id="99e3f-112">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="99e3f-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e3f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99e3f-113">Remarks</span></span>

<span data-ttu-id="99e3f-114">Wenn Sie möchten, dass der Treiber Daten direkt auf dem Bildschirm dekomprimiert, senden Sie die [**ICM \_ Draw**](icm-draw.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="99e3f-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="99e3f-115">Der Treiber gibt einen Fehler zurück, wenn diese Nachricht vor der [**ICM- \_ Dekomprimierungs \_ Begin**](icm-decompress-begin.md) -Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="99e3f-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="99e3f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99e3f-116">Requirements</span></span>



| <span data-ttu-id="99e3f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99e3f-117">Requirement</span></span> | <span data-ttu-id="99e3f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="99e3f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="99e3f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99e3f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99e3f-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99e3f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="99e3f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99e3f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99e3f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99e3f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="99e3f-123">Header</span><span class="sxs-lookup"><span data-stu-id="99e3f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="99e3f-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e3f-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99e3f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99e3f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e3f-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="99e3f-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="99e3f-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="99e3f-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





