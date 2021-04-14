---
title: WM_CAP_DRIVER_CONNECT Meldung (VFW. h)
description: Mit der CONNECT-Nachricht des WM- \_ Cap- \_ Treibers wird \_ ein Aufzeichnungs Fenster mit einem Aufzeichnungs Treiber verbunden. Sie können diese Nachricht explizit oder mithilfe des capdriverconnect-Makros senden.
ms.assetid: 8804bb3c-d06c-4ddc-b116-3d292205a52d
keywords:
- WM_CAP_DRIVER_CONNECT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_CONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fdeb89968926429f7225912e3d1b3b348e287
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391818"
---
# <a name="wm_cap_driver_connect-message"></a><span data-ttu-id="beadf-105">\_ \_ \_ Verbindungs Meldung zum WM-Cap-Treiber</span><span class="sxs-lookup"><span data-stu-id="beadf-105">WM\_CAP\_DRIVER\_CONNECT message</span></span>

<span data-ttu-id="beadf-106">Mit der CONNECT-Nachricht des **WM- \_ Cap- \_ Treibers \_** wird ein Aufzeichnungs Fenster mit einem Aufzeichnungs Treiber verbunden.</span><span class="sxs-lookup"><span data-stu-id="beadf-106">The **WM\_CAP\_DRIVER\_CONNECT** message connects a capture window to a capture driver.</span></span> <span data-ttu-id="beadf-107">Sie können diese Nachricht explizit oder mithilfe des [**capdriverconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="beadf-107">You can send this message explicitly or by using the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_CONNECT 
wParam = (WPARAM) (iIndex); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="beadf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="beadf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beadf-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="beadf-109"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="beadf-110">Der Index des Erfassungs Treibers.</span><span class="sxs-lookup"><span data-stu-id="beadf-110">Index of the capture driver.</span></span> <span data-ttu-id="beadf-111">Der Index kann zwischen 0 und 9 liegen.</span><span class="sxs-lookup"><span data-stu-id="beadf-111">The index can range from 0 through 9.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beadf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="beadf-112">Return Value</span></span>

<span data-ttu-id="beadf-113">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn der angegebene Erfassungs Treiber nicht mit dem Erfassungsfenster verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="beadf-113">Returns **TRUE** if successful or **FALSE** if the specified capture driver cannot be connected to the capture window.</span></span>

## <a name="remarks"></a><span data-ttu-id="beadf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="beadf-114">Remarks</span></span>

<span data-ttu-id="beadf-115">Durch das Verbinden eines Erfassungs Treibers mit einem Aufzeichnungs Fenster wird automatisch eine Verbindung mit allen zuvor verbundenen Aufzeichnungs Treibern getrennt.</span><span class="sxs-lookup"><span data-stu-id="beadf-115">Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="beadf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="beadf-116">Requirements</span></span>



| <span data-ttu-id="beadf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="beadf-117">Requirement</span></span> | <span data-ttu-id="beadf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="beadf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="beadf-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="beadf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="beadf-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beadf-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="beadf-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="beadf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="beadf-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="beadf-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="beadf-123">Header</span><span class="sxs-lookup"><span data-stu-id="beadf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="beadf-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="beadf-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beadf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="beadf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beadf-126">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="beadf-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="beadf-127">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="beadf-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





