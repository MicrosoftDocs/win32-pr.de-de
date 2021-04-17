---
title: ICM_COMPRESS_FRAMES_INFO Meldung (VFW. h)
description: In der Info Meldung zum ICM- \_ komprimieren wird \_ \_ ein Komprimierungs Treiber benachrichtigt, um die Parameter für die ausstehende Komprimierung festzulegen.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478465"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="08d76-104">ICM- \_ Informationen zum Komprimieren von \_ Frames \_</span><span class="sxs-lookup"><span data-stu-id="08d76-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="08d76-105">In der **\_ \_ \_ Info Meldung zum ICM-komprimieren** wird ein Komprimierungs Treiber benachrichtigt, um die Parameter für die ausstehende Komprimierung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="08d76-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="08d76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08d76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d76-107"><span id="icf"></span><span id="ICF"></span>*ICF*</span><span class="sxs-lookup"><span data-stu-id="08d76-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="08d76-108">Zeiger auf eine [**iccompressframes**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="08d76-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="08d76-109">Die **GetData** -und **putdata** -Member dieser Struktur werden mit dieser Nachricht nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="08d76-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="08d76-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="08d76-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="08d76-111">Größe von [**iccompressframes**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)in Bytes.</span><span class="sxs-lookup"><span data-stu-id="08d76-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d76-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08d76-112">Return Value</span></span>

<span data-ttu-id="08d76-113">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="08d76-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="08d76-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08d76-114">Remarks</span></span>

<span data-ttu-id="08d76-115">Ein-Kompressor kann diese Meldung verwenden, um zu bestimmen, wie viel Speicherplatz für jeden Frame während der Komprimierung belegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08d76-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="08d76-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08d76-116">Requirements</span></span>



| <span data-ttu-id="08d76-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08d76-117">Requirement</span></span> | <span data-ttu-id="08d76-118">Wert</span><span class="sxs-lookup"><span data-stu-id="08d76-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="08d76-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08d76-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08d76-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08d76-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="08d76-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08d76-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08d76-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08d76-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="08d76-123">Header</span><span class="sxs-lookup"><span data-stu-id="08d76-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08d76-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="08d76-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08d76-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08d76-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d76-126">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="08d76-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="08d76-127">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="08d76-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





