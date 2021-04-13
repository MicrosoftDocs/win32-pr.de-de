---
title: WM_CAP_DRIVER_GET_CAPS Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ Driver \_ get \_ Caps" gibt die Hardwarefunktionen des Aufzeichnungs Treibers zurück, der zurzeit mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetcaps-Makros senden.
ms.assetid: 898a800c-1109-47cd-bcc9-cb61d86a4a2e
keywords:
- WM_CAP_DRIVER_GET_CAPS-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_CAPS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027e530be82c76afebc343ceebe4905daef9b126
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518959"
---
# <a name="wm_cap_driver_get_caps-message"></a><span data-ttu-id="4d735-105">WM- \_ Cap- \_ Treiber \_ Get Caps- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="4d735-105">WM\_CAP\_DRIVER\_GET\_CAPS message</span></span>

<span data-ttu-id="4d735-106">Die Meldung " **WM \_ Cap \_ Driver \_ get \_ Caps** " gibt die Hardwarefunktionen des Aufzeichnungs Treibers zurück, der zurzeit mit einem Aufzeichnungs Fenster verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4d735-106">The **WM\_CAP\_DRIVER\_GET\_CAPS** message returns the hardware capabilities of the capture driver currently connected to a capture window.</span></span> <span data-ttu-id="4d735-107">Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetcaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4d735-107">You can send this message explicitly or by using the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_CAPS 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPDRIVERCAPS) (psCaps); 
```



## <a name="parameters"></a><span data-ttu-id="4d735-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d735-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d735-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="4d735-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="4d735-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4d735-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="4d735-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*pscaps*</span><span class="sxs-lookup"><span data-stu-id="4d735-111"><span id="psCaps"></span><span id="pscaps"></span><span id="PSCAPS"></span>*psCaps*</span></span>
</dt> <dd>

<span data-ttu-id="4d735-112">Ein Zeiger auf die [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) -Struktur, die die Hardwarefunktionen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="4d735-112">Pointer to the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure to contain the hardware capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d735-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d735-113">Return Value</span></span>

<span data-ttu-id="4d735-114">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4d735-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d735-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d735-115">Remarks</span></span>

<span data-ttu-id="4d735-116">Die in [**capdrivercaps**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) zurückgegebenen Funktionen sind für einen bestimmten Erfassungs Treiber konstant.</span><span class="sxs-lookup"><span data-stu-id="4d735-116">The capabilities returned in [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) are constant for a given capture driver.</span></span> <span data-ttu-id="4d735-117">Anwendungen müssen diese Informationen einmal abrufen, wenn der Erfassungs Treiber zum ersten Mal mit einem Aufzeichnungs Fenster verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4d735-117">Applications need to retrieve this information once when the capture driver is first connected to a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d735-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d735-118">Requirements</span></span>



| <span data-ttu-id="4d735-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d735-119">Requirement</span></span> | <span data-ttu-id="4d735-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4d735-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4d735-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d735-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d735-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d735-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4d735-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d735-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d735-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d735-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4d735-125">Header</span><span class="sxs-lookup"><span data-stu-id="4d735-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d735-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d735-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d735-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d735-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d735-128">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="4d735-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="4d735-129">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="4d735-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





