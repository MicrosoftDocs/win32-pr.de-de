---
title: MCIWNDM_PUT_DEST Meldung (VFW. h)
description: Die "mciwndm"- \_ \_ dest-Nachricht definiert die Koordinaten des Ziel Rechtecks neu, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndputdest-Makros senden.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742952"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="3b0a6-105">Mciwndm \_ - \_ dest-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3b0a6-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="3b0a6-106">Die " **mciwndm"- \_ \_ dest** -Nachricht definiert die Koordinaten des Ziel Rechtecks neu, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="3b0a6-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndputdest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="3b0a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3b0a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b0a6-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="3b0a6-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="3b0a6-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Ziel Rechtecks enthält.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b0a6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3b0a6-111">Return Value</span></span>

<span data-ttu-id="3b0a6-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="3b0a6-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b0a6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b0a6-113">Requirements</span></span>



| <span data-ttu-id="3b0a6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b0a6-114">Requirement</span></span> | <span data-ttu-id="3b0a6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3b0a6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3b0a6-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b0a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b0a6-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b0a6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3b0a6-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b0a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b0a6-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3b0a6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b0a6-120">Header</span><span class="sxs-lookup"><span data-stu-id="3b0a6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b0a6-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b0a6-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b0a6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b0a6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b0a6-123">**Mciwndputdest**</span><span class="sxs-lookup"><span data-stu-id="3b0a6-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

