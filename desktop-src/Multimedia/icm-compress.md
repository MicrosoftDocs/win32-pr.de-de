---
title: ICM_COMPRESS Meldung (VFW. h)
description: In der ICM- \_ Komprimierungs Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen in einen Anwendungs definierten Puffer zu komprimieren.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- ICM_COMPRESS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340359"
---
# <a name="icm_compress-message"></a><span data-ttu-id="19035-104">ICM- \_ Komprimierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="19035-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="19035-105">In der **ICM- \_ Komprimierungs** Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um einen Datenrahmen in einen Anwendungs definierten Puffer zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="19035-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="19035-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="19035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19035-107"><span id="icc"></span><span id="ICC"></span>*ausgeliefert*</span><span class="sxs-lookup"><span data-stu-id="19035-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="19035-108">Zeiger auf eine [**iccompress**](/windows/desktop/api/Vfw/ns-vfw-iccompress) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="19035-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="19035-109">Die folgenden Member dieser Struktur geben die Komprimierungs Parameter an: **lpbiinput**, **lpinput**, **lpbioutput**, **lpoutput**, **lpbiprev**, **lpprev**, **lpckid**, **lpdwflags**, **dwframesize** und **dwquality**.</span><span class="sxs-lookup"><span data-stu-id="19035-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="19035-110">Der Treiber sollte auch den **bisizeimage** -Member der [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) -Struktur verwenden, die **lpbioutput** von **iccompress** zugeordnet ist, um die Größe des komprimierten Rahmens zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="19035-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="19035-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*</span><span class="sxs-lookup"><span data-stu-id="19035-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="19035-112">Größe von [**iccompress**](/windows/desktop/api/Vfw/ns-vfw-iccompress)(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="19035-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19035-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19035-113">Return Value</span></span>

<span data-ttu-id="19035-114">Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="19035-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="19035-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19035-115">Requirements</span></span>



| <span data-ttu-id="19035-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19035-116">Requirement</span></span> | <span data-ttu-id="19035-117">Wert</span><span class="sxs-lookup"><span data-stu-id="19035-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="19035-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19035-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19035-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19035-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="19035-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19035-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19035-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19035-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="19035-122">Header</span><span class="sxs-lookup"><span data-stu-id="19035-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="19035-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="19035-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19035-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19035-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19035-125">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="19035-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="19035-126">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="19035-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

