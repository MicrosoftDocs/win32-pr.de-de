---
title: WM_CAP_GET_SEQUENCE_SETUP Meldung (VFW. h)
description: Die "WM \_ Cap \_ Get Sequence"- \_ \_ Setup Nachricht Ruft die aktuellen Einstellungen der streamingerfassungs Parameter ab. Sie können diese Nachricht explizit oder mithilfe des capcapturegetsetup-Makros senden.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- WM_CAP_GET_SEQUENCE_SETUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949395"
---
# <a name="wm_cap_get_sequence_setup-message"></a><span data-ttu-id="12191-105">Meldung zum Einrichten der WM- \_ Cap- \_ \_ Sequenz \_</span><span class="sxs-lookup"><span data-stu-id="12191-105">WM\_CAP\_GET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="12191-106">Die " **WM \_ Cap \_ get \_ Sequence \_** "-Setup Nachricht Ruft die aktuellen Einstellungen der streamingerfassungs Parameter ab.</span><span class="sxs-lookup"><span data-stu-id="12191-106">The **WM\_CAP\_GET\_SEQUENCE\_SETUP** message retrieves the current settings of the streaming capture parameters.</span></span> <span data-ttu-id="12191-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="12191-107">You can send this message explicitly or by using the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro.</span></span>


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a><span data-ttu-id="12191-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="12191-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12191-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="12191-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="12191-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="12191-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="12191-111"><span id="s"></span><span id="S"></span>*Hymnen*</span><span class="sxs-lookup"><span data-stu-id="12191-111"><span id="s"></span><span id="S"></span>*s*</span></span>
</dt> <dd>

<span data-ttu-id="12191-112">Zeiger auf eine [**captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="12191-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12191-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12191-113">Return Value</span></span>

<span data-ttu-id="12191-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="12191-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12191-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12191-115">Remarks</span></span>

<span data-ttu-id="12191-116">Informationen zu den Parametern, die zum Steuern der streamingerfassung verwendet werden, finden Sie in der Struktur von [**captuprojektms**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="12191-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="12191-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12191-117">Requirements</span></span>



| <span data-ttu-id="12191-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12191-118">Requirement</span></span> | <span data-ttu-id="12191-119">Wert</span><span class="sxs-lookup"><span data-stu-id="12191-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12191-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12191-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12191-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12191-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12191-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12191-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12191-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12191-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12191-124">Header</span><span class="sxs-lookup"><span data-stu-id="12191-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="12191-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="12191-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12191-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12191-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12191-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="12191-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="12191-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="12191-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





