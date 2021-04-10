---
title: MCIWNDM_GET_DEST Meldung (VFW. h)
description: Die mciwndm \_ get \_ dest-Nachricht Ruft die Koordinaten des Ziel Rechtecks ab, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des Makros mciwndgetdest senden.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040075"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="de818-105">Mciwndm- \_ get- \_ dest-Meldung</span><span class="sxs-lookup"><span data-stu-id="de818-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="de818-106">Die **mciwndm \_ get \_ dest** -Nachricht Ruft die Koordinaten des Ziel Rechtecks ab, das zum Zoomen oder Strecken der Bilder einer AVI-Datei während der Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de818-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="de818-107">Sie können diese Nachricht explizit oder mithilfe des Makros [**mciwndgetdest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) senden.</span><span class="sxs-lookup"><span data-stu-id="de818-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="de818-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de818-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de818-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="de818-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="de818-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, um die Koordinaten des Ziel Rechtecks zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="de818-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de818-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de818-111">Return Value</span></span>

<span data-ttu-id="de818-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="de818-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de818-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de818-113">Requirements</span></span>



| <span data-ttu-id="de818-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de818-114">Requirement</span></span> | <span data-ttu-id="de818-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de818-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de818-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de818-116">Minimum supported client</span></span><br/> | <span data-ttu-id="de818-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de818-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="de818-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de818-118">Minimum supported server</span></span><br/> | <span data-ttu-id="de818-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de818-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="de818-120">Header</span><span class="sxs-lookup"><span data-stu-id="de818-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="de818-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="de818-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de818-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de818-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de818-123">**Mciwndgetdest**</span><span class="sxs-lookup"><span data-stu-id="de818-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

