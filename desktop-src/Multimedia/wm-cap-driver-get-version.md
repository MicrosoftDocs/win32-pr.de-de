---
title: WM_CAP_DRIVER_GET_VERSION Meldung (VFW. h)
description: Die Meldung "WM \_ Cap \_ Driver \_ get \_ Version" gibt die Versionsinformationen des Aufzeichnungs Treibers zurück, der mit einem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetversion-Makros senden.
ms.assetid: 762ebe7e-0d09-46ea-ab17-86061f0bd8f9
keywords:
- WM_CAP_DRIVER_GET_VERSION-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_VERSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced70f2d0159ef4bbad3f2d7a8027c30b2c71a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345923"
---
# <a name="wm_cap_driver_get_version-message"></a><span data-ttu-id="6d576-105">WM- \_ Cap- \_ Treiber Version der \_ \_ Nachricht erhalten</span><span class="sxs-lookup"><span data-stu-id="6d576-105">WM\_CAP\_DRIVER\_GET\_VERSION message</span></span>

<span data-ttu-id="6d576-106">Die Meldung " **WM \_ Cap \_ Driver \_ get \_ Version** " gibt die Versionsinformationen des Aufzeichnungs Treibers zurück, der mit einem Aufzeichnungs Fenster verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d576-106">The **WM\_CAP\_DRIVER\_GET\_VERSION** message returns the version information of the capture driver connected to a capture window.</span></span> <span data-ttu-id="6d576-107">Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetversion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="6d576-107">You can send this message explicitly or by using the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_VERSION 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szVer); 
```



## <a name="parameters"></a><span data-ttu-id="6d576-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d576-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d576-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="6d576-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="6d576-110">Größe (in Bytes) des Anwendungs definierten Puffers, auf den von **szver** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6d576-110">Size, in bytes, of the application-defined buffer referenced by **szVer**.</span></span>

</dd> <dt>

<span data-ttu-id="6d576-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szver*</span><span class="sxs-lookup"><span data-stu-id="6d576-111"><span id="szVer"></span><span id="szver"></span><span id="SZVER"></span>*szVer*</span></span>
</dt> <dd>

<span data-ttu-id="6d576-112">Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um die Versionsinformationen als NULL-terminierte Zeichenfolge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="6d576-112">Pointer to an application-defined buffer used to return the version information as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d576-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d576-113">Return Value</span></span>

<span data-ttu-id="6d576-114">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d576-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d576-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d576-115">Remarks</span></span>

<span data-ttu-id="6d576-116">Die Versionsinformationen sind eine Text Zeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6d576-116">The version information is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="6d576-117">Anwendungen sollten für diese Zeichenfolge ungefähr 40 Byte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6d576-117">Applications should allocate approximately 40 bytes for this string.</span></span> <span data-ttu-id="6d576-118">Wenn keine Versionsinformationen verfügbar sind, wird eine **null** -Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6d576-118">If version information is not available, a **NULL** string is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d576-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d576-119">Requirements</span></span>



| <span data-ttu-id="6d576-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d576-120">Requirement</span></span> | <span data-ttu-id="6d576-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6d576-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6d576-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d576-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6d576-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d576-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6d576-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d576-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6d576-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d576-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6d576-126">Header</span><span class="sxs-lookup"><span data-stu-id="6d576-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d576-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d576-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d576-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d576-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d576-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="6d576-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6d576-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="6d576-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





