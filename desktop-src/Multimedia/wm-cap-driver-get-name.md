---
title: WM_CAP_DRIVER_GET_NAME Meldung (VFW. h)
description: Die Meldung "WM- \_ Cap- \_ Treiber \_ get \_ Name" gibt den Namen des Aufzeichnungs Treibers zurück, der mit dem Aufzeichnungs Fenster verbunden ist. Sie können diese Nachricht explizit oder mithilfe des capdrivergetname-Makros senden.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- WM_CAP_DRIVER_GET_NAME-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475858"
---
# <a name="wm_cap_driver_get_name-message"></a><span data-ttu-id="129ca-105">WM- \_ Cap- \_ Treiber get- \_ \_ namens Meldung</span><span class="sxs-lookup"><span data-stu-id="129ca-105">WM\_CAP\_DRIVER\_GET\_NAME message</span></span>

<span data-ttu-id="129ca-106">Die Meldung " **WM- \_ Cap- \_ Treiber \_ get \_ Name** " gibt den Namen des Aufzeichnungs Treibers zurück, der mit dem Aufzeichnungs Fenster verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="129ca-106">The **WM\_CAP\_DRIVER\_GET\_NAME** message returns the name of the capture driver connected to the capture window.</span></span> <span data-ttu-id="129ca-107">Sie können diese Nachricht explizit oder mithilfe des [**capdrivergetname**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="129ca-107">You can send this message explicitly or by using the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro.</span></span>


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="129ca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="129ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="129ca-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="129ca-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="129ca-110">Größe (in Bytes) des Puffers, auf den von **szName** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="129ca-110">Size, in bytes, of the buffer referenced by **szName**.</span></span>

</dd> <dt>

<span data-ttu-id="129ca-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="129ca-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="129ca-112">Ein Zeiger auf einen Anwendungs definierten Puffer, der verwendet wird, um den Gerätenamen als eine auf NULL endende Zeichenfolge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="129ca-112">Pointer to an application-defined buffer used to return the device name as a null-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="129ca-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="129ca-113">Return Value</span></span>

<span data-ttu-id="129ca-114">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn das Aufzeichnungs Fenster nicht mit einem Aufzeichnungs Treiber verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="129ca-114">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="129ca-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="129ca-115">Remarks</span></span>

<span data-ttu-id="129ca-116">Der Name ist eine Text Zeichenfolge, die aus dem Ressourcenbereich des Treibers abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="129ca-116">The name is a text string retrieved from the driver's resource area.</span></span> <span data-ttu-id="129ca-117">Anwendungen sollten für diese Zeichenfolge ungefähr 80 Byte zuordnen.</span><span class="sxs-lookup"><span data-stu-id="129ca-117">Applications should allocate approximately 80 bytes for this string.</span></span> <span data-ttu-id="129ca-118">Wenn der Treiber keine namens Ressource enthält, wird der vollständige Pfadname des Treibers, der in der Registrierung oder in der SYSTEM.INI Datei aufgeführt ist, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="129ca-118">If the driver does not contain a name resource, the full path name of the driver listed in the registry or in the SYSTEM.INI file is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="129ca-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="129ca-119">Requirements</span></span>



| <span data-ttu-id="129ca-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="129ca-120">Requirement</span></span> | <span data-ttu-id="129ca-121">Wert</span><span class="sxs-lookup"><span data-stu-id="129ca-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="129ca-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="129ca-122">Minimum supported client</span></span><br/> | <span data-ttu-id="129ca-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="129ca-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="129ca-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="129ca-124">Minimum supported server</span></span><br/> | <span data-ttu-id="129ca-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="129ca-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="129ca-126">Header</span><span class="sxs-lookup"><span data-stu-id="129ca-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="129ca-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="129ca-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="129ca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="129ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="129ca-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="129ca-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="129ca-130">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="129ca-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





