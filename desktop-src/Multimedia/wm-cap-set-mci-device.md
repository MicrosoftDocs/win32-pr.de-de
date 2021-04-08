---
title: WM_CAP_SET_MCI_DEVICE Meldung (VFW. h)
description: Die \_ \_ MCI-Geräte Meldung "WM Cap Set" \_ \_ gibt den Namen des MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll. Sie können diese Nachricht explizit oder mithilfe des capabtmcidevicename-Makros senden.
ms.assetid: 83fdf567-ceb2-45aa-8529-433a5c64ac0a
keywords:
- WM_CAP_SET_MCI_DEVICE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_MCI_DEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86187f3357bf72866e05b497332454c10bcd2fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740056"
---
# <a name="wm_cap_set_mci_device-message"></a><span data-ttu-id="d4d3f-105">WM- \_ Cap- \_ \_ Geräte Nachricht für MCI- \_ Gerät festlegen</span><span class="sxs-lookup"><span data-stu-id="d4d3f-105">WM\_CAP\_SET\_MCI\_DEVICE message</span></span>

<span data-ttu-id="d4d3f-106">Die **\_ \_ \_ MCI- \_ Geräte Meldung "WM Cap Set** " gibt den Namen des MCI-Videogeräts an, das zum Erfassen von Daten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-106">The **WM\_CAP\_SET\_MCI\_DEVICE** message specifies the name of the MCI video device to be used to capture data.</span></span> <span data-ttu-id="d4d3f-107">Sie können diese Nachricht explizit oder mithilfe des [**capabtmcidevicename**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-107">You can send this message explicitly or by using the [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) macro.</span></span>


```C++
WM_CAP_SET_MCI_DEVICE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="d4d3f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d3f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="d4d3f-109"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="d4d3f-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Geräts enthält.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-110">Pointer to a null-terminated string containing the name of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d3f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4d3f-111">Return Value</span></span>

<span data-ttu-id="d4d3f-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d4d3f-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d3f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d3f-113">Remarks</span></span>

<span data-ttu-id="d4d3f-114">In dieser Meldung wird der MCI-Gerätename in einer internen Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-114">This message stores the MCI device name in an internal structure.</span></span> <span data-ttu-id="d4d3f-115">Das Gerät wird nicht geöffnet, oder es wird nicht darauf zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-115">It does not open or access the device.</span></span> <span data-ttu-id="d4d3f-116">Der Standardgeräte Name ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-116">The default device name is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d3f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d3f-117">Requirements</span></span>



| <span data-ttu-id="d4d3f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d3f-118">Requirement</span></span> | <span data-ttu-id="d4d3f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d3f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4d3f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4d3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d3f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d3f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d4d3f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4d3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d3f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d3f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4d3f-124">Header</span><span class="sxs-lookup"><span data-stu-id="d4d3f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d3f-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d3f-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d3f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4d3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d3f-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="d4d3f-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d4d3f-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="d4d3f-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





