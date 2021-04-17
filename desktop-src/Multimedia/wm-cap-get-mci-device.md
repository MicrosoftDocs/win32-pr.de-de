---
title: WM_CAP_GET_MCI_DEVICE Meldung (VFW. h)
description: Die "WM \_ Cap \_ get \_ MCI Device"- \_ Meldung Ruft den Namen eines MCI-Geräts ab, das zuvor mit der "WM \_ Cap \_ Set \_ MCI \_ Device"-Meldung festgelegt wurde. Sie können diese Nachricht explizit oder mithilfe des capgetmcidevicename-Makros senden.
ms.assetid: c5d7d955-ab6a-4959-b79e-9ff35a282ba2
keywords:
- WM_CAP_GET_MCI_DEVICE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0960ff9aa1366802611f444383212c4bcc45bcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475072"
---
# <a name="wm_cap_get_mci_device-message"></a><span data-ttu-id="d9b79-105">WM- \_ Cap- \_ \_ MCI- \_ Geräte Nachricht erhalten</span><span class="sxs-lookup"><span data-stu-id="d9b79-105">WM\_CAP\_GET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="d9b79-106">Die " **WM \_ Cap \_ get \_ MCI \_ Device** "-Meldung Ruft den Namen eines MCI-Geräts ab, das zuvor mit der " [**WM \_ Cap \_ Set \_ MCI \_ Device**](wm-cap-set-mci-device.md) "-Meldung festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9b79-106">The **WM\_CAP\_GET\_MCI\_DEVICE** message retrieves the name of an MCI device previously set with the [**WM\_CAP\_SET\_MCI\_DEVICE**](wm-cap-set-mci-device.md) message.</span></span> <span data-ttu-id="d9b79-107">Sie können diese Nachricht explizit oder mithilfe des [**capgetmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d9b79-107">You can send this message explicitly or by using the [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) macro.</span></span>


```C++
WM_CAP_GET_MCI_DEVICE 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="d9b79-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9b79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b79-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="d9b79-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d9b79-110">Länge (in Byte) des Puffers, auf den von **szName** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d9b79-110">Length, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="d9b79-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="d9b79-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="d9b79-112">Zeiger auf eine mit NULL endenden Zeichenfolge, die den MCI-Gerätenamen enthält.</span><span class="sxs-lookup"><span data-stu-id="d9b79-112">Pointer to a null-terminated string that contains the MCI device name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b79-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9b79-113">Return Value</span></span>

<span data-ttu-id="d9b79-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d9b79-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9b79-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9b79-115">Requirements</span></span>



| <span data-ttu-id="d9b79-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9b79-116">Requirement</span></span> | <span data-ttu-id="d9b79-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d9b79-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d9b79-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9b79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b79-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9b79-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d9b79-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9b79-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b79-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9b79-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9b79-122">Header</span><span class="sxs-lookup"><span data-stu-id="d9b79-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b79-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b79-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b79-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9b79-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b79-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="d9b79-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d9b79-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d9b79-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





