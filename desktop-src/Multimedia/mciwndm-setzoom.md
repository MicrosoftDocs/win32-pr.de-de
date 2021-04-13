---
title: MCIWNDM_SETZOOM Meldung (VFW. h)
description: Die mciwndm- \_ Nachricht "setzoom" ändert die Größe eines Video Bilds entsprechend einem Zoomfaktor. Dadurch wird die Größe eines mciwnd-Fensters bei gleichzeitiger Beibehaltung eines konstanten Seitenverhältnisses angepasst. Sie können diese Nachricht explizit oder mithilfe des mciwndsetzoom-Makros senden.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475516"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="95943-106">Mciwndm- \_ setzoom-Nachricht</span><span class="sxs-lookup"><span data-stu-id="95943-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="95943-107">Die **mciwndm-Nachricht " \_ setzoom** " ändert die Größe eines Video Bilds entsprechend einem Zoomfaktor.</span><span class="sxs-lookup"><span data-stu-id="95943-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="95943-108">Dadurch wird die Größe eines mciwnd-Fensters bei gleichzeitiger Beibehaltung eines konstanten Seitenverhältnisses angepasst.</span><span class="sxs-lookup"><span data-stu-id="95943-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="95943-109">Sie können diese Nachricht explizit oder mithilfe des [**mciwndsetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="95943-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="95943-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="95943-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95943-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*izoom*</span><span class="sxs-lookup"><span data-stu-id="95943-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="95943-112">Der Zoom Faktor, ausgedrückt als Prozentsatz des ursprünglichen Bilds.</span><span class="sxs-lookup"><span data-stu-id="95943-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="95943-113">Geben Sie 100 an, um das Bild an der erstellten Größe anzuzeigen, 200, um das Bild bei der doppelten Größe anzuzeigen, oder 50, um das Bild in der Hälfte der normalen Größe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="95943-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95943-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95943-114">Return Value</span></span>

<span data-ttu-id="95943-115">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="95943-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95943-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95943-116">Requirements</span></span>



| <span data-ttu-id="95943-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95943-117">Requirement</span></span> | <span data-ttu-id="95943-118">Wert</span><span class="sxs-lookup"><span data-stu-id="95943-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="95943-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95943-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95943-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95943-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95943-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95943-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95943-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95943-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="95943-123">Header</span><span class="sxs-lookup"><span data-stu-id="95943-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95943-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="95943-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95943-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95943-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95943-126">**Mciwndsetzoom**</span><span class="sxs-lookup"><span data-stu-id="95943-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





