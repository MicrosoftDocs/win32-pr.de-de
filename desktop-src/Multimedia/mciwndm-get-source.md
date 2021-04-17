---
title: MCIWNDM_GET_SOURCE Meldung (VFW. h)
description: Die mciwndm \_ get- \_ Quell Nachricht Ruft die Koordinaten des Quell Rechtecks ab, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird. Sie können diese Nachricht explizit oder mit dem mciwndgetsource-Makro senden.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392095"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="39c11-105">Mciwndm \_ - \_ Quell Nachricht</span><span class="sxs-lookup"><span data-stu-id="39c11-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="39c11-106">Die **mciwndm \_ get- \_ Quell** Nachricht Ruft die Koordinaten des Quell Rechtecks ab, das zum Zuschneiden der Bilder einer AVI-Datei während der Wiedergabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="39c11-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="39c11-107">Sie können diese Nachricht explizit oder mit dem [**mciwndgetsource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="39c11-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="39c11-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c11-109"><span id="prc"></span><span id="PRC"></span>*PRC*</span><span class="sxs-lookup"><span data-stu-id="39c11-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="39c11-110">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten des Quell Rechtecks enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="39c11-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c11-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39c11-111">Return Value</span></span>

<span data-ttu-id="39c11-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="39c11-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c11-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39c11-113">Requirements</span></span>



| <span data-ttu-id="39c11-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c11-114">Requirement</span></span> | <span data-ttu-id="39c11-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39c11-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="39c11-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39c11-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39c11-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39c11-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="39c11-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39c11-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39c11-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39c11-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39c11-120">Header</span><span class="sxs-lookup"><span data-stu-id="39c11-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c11-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c11-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c11-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39c11-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c11-123">**Mciwndgetsource**</span><span class="sxs-lookup"><span data-stu-id="39c11-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

