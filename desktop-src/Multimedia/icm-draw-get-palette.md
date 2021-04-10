---
title: ICM_DRAW_GET_PALETTE Meldung (VFW. h)
description: Die ICM \_ Draw \_ get- \_ palettennachricht fordert einen renderingtreiber an, eine Palette zurückzugeben.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- ICM_DRAW_GET_PALETTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040223"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="4626d-104">ICM- \_ Zeichnen- \_ \_ palettennachricht</span><span class="sxs-lookup"><span data-stu-id="4626d-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="4626d-105">Die **ICM \_ Draw \_ get- \_ palettennachricht** fordert einen renderingtreiber an, eine Palette zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="4626d-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="4626d-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4626d-106">Return Value</span></span>

<span data-ttu-id="4626d-107">Der Treiber sollte eines der folgenden Werte zurückgeben: ein Handle der verwendeten Palette, **null** , wenn kein Handle vorhanden ist, oder ICERR wird \_ nicht unterstützt, wenn keine Paletten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4626d-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="4626d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4626d-108">Requirements</span></span>



| <span data-ttu-id="4626d-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4626d-109">Requirement</span></span> | <span data-ttu-id="4626d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="4626d-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4626d-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4626d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="4626d-112">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4626d-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4626d-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4626d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="4626d-114">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4626d-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4626d-115">Header</span><span class="sxs-lookup"><span data-stu-id="4626d-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="4626d-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4626d-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4626d-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4626d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4626d-118">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="4626d-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="4626d-119">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4626d-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





