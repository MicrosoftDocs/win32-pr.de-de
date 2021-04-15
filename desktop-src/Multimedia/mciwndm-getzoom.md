---
title: MCIWNDM_GETZOOM Meldung (VFW. h)
description: Die mciwndm \_ getzoom-Nachricht Ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndgetzoom-Makros senden.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476227"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="32506-105">Mciwndm \_ getzoom-Meldung</span><span class="sxs-lookup"><span data-stu-id="32506-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="32506-106">Die **mciwndm \_ getzoom** -Nachricht Ruft den aktuellen Zoomwert ab, der von einem MCI-Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32506-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="32506-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndgetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="32506-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="32506-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32506-108">Return Value</span></span>

<span data-ttu-id="32506-109">Gibt die neuesten Werte zurück, die mit [**mciwndm- \_ setzoom**](mciwndm-setzoom.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32506-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="32506-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32506-110">Remarks</span></span>

<span data-ttu-id="32506-111">Der Rückgabewert 100 gibt an, dass das Bild nicht verkleinert wird.</span><span class="sxs-lookup"><span data-stu-id="32506-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="32506-112">Der Wert 200 gibt an, dass das Bild auf die doppelte Größe vergrößert wird.</span><span class="sxs-lookup"><span data-stu-id="32506-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="32506-113">Der Wert 50 gibt an, dass das Bild auf die Hälfte seiner ursprünglichen Größe reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="32506-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="32506-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32506-114">Requirements</span></span>



| <span data-ttu-id="32506-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32506-115">Requirement</span></span> | <span data-ttu-id="32506-116">Wert</span><span class="sxs-lookup"><span data-stu-id="32506-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="32506-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32506-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32506-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32506-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="32506-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32506-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32506-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32506-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="32506-121">Header</span><span class="sxs-lookup"><span data-stu-id="32506-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32506-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="32506-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32506-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32506-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32506-124">**Mciwndgetzoom**</span><span class="sxs-lookup"><span data-stu-id="32506-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="32506-125">**mciwndm- \_ setzoom**</span><span class="sxs-lookup"><span data-stu-id="32506-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





