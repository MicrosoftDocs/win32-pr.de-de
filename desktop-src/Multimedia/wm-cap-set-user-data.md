---
title: WM_CAP_SET_USER_DATA Meldung (VFW. h)
description: In der Benutzerdaten Meldung "WM-Cap-Datensatz" wird \_ \_ \_ \_ ein langer \_ ptr-Datenwert mit einem Aufzeichnungs Fenster verknüpft. Sie können diese Nachricht explizit oder mithilfe des capsetuserdata-Makros senden.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106107"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="ac564-105">WM- \_ Cap- \_ \_ Benutzer \_ Daten Meldung festlegen</span><span class="sxs-lookup"><span data-stu-id="ac564-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="ac564-106">In **der \_ \_ \_ Benutzer \_ Daten** Meldung "WM-Cap-Datensatz" wird ein **langer \_ ptr** -Datenwert mit einem Aufzeichnungs Fenster verknüpft.</span><span class="sxs-lookup"><span data-stu-id="ac564-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="ac564-107">Sie können diese Nachricht explizit oder mithilfe des [**capsetuserdata**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ac564-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="ac564-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac564-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac564-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*luser*</span><span class="sxs-lookup"><span data-stu-id="ac564-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="ac564-110">Datenwert, der einem Aufzeichnungs Fenster zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac564-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac564-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac564-111">Return Value</span></span>

<span data-ttu-id="ac564-112">Gibt **true** zurück, wenn erfolgreich oder **false** , wenn die streamingerfassung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac564-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac564-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac564-113">Remarks</span></span>

<span data-ttu-id="ac564-114">In der Regel wird diese Nachricht verwendet, um auf einen Datenblock zu verweisen, der mit einem Aufzeichnungs Fenster verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ac564-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac564-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac564-115">Requirements</span></span>



| <span data-ttu-id="ac564-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac564-116">Requirement</span></span> | <span data-ttu-id="ac564-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ac564-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac564-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac564-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ac564-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac564-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac564-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac564-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ac564-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac564-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ac564-122">Header</span><span class="sxs-lookup"><span data-stu-id="ac564-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac564-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac564-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac564-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac564-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac564-125">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="ac564-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ac564-126">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="ac564-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





