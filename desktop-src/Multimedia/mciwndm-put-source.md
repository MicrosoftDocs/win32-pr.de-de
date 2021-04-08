---
title: MCIWNDM_PUT_SOURCE Meldung (VFW. h)
description: Die mciwndm \_ Put- \_ Quell Nachricht definiert die Koordinaten des Quell Rechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mithilfe des mciwndputsource-Makros senden.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739816"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="e9af9-105">Mciwndm \_ Put- \_ Quell Nachricht</span><span class="sxs-lookup"><span data-stu-id="e9af9-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="e9af9-106">Die **mciwndm \_ Put- \_ Quell** Nachricht definiert die Koordinaten des Quell Rechtecks neu, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9af9-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="e9af9-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndputsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="e9af9-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="e9af9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9af9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9af9-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="e9af9-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="e9af9-110">Ein Zeiger auf eine [Rect](/previous-versions//ms536136(v=vs.85)) -Struktur, die die Koordinaten des Quell Rechtecks enthält.</span><span class="sxs-lookup"><span data-stu-id="e9af9-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9af9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9af9-111">Return Value</span></span>

<span data-ttu-id="e9af9-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="e9af9-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9af9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9af9-113">Requirements</span></span>



| <span data-ttu-id="e9af9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9af9-114">Requirement</span></span> | <span data-ttu-id="e9af9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e9af9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e9af9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9af9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9af9-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9af9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e9af9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9af9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9af9-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9af9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e9af9-120">Header</span><span class="sxs-lookup"><span data-stu-id="e9af9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9af9-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9af9-121"><dt>Vfw.h</dt></span></span> </dl> |



 

