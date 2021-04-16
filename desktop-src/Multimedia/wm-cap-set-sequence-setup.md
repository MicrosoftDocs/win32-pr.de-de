---
title: WM_CAP_SET_SEQUENCE_SETUP Meldung (VFW. h)
description: Mit der Einstellung für die WM- \_ Cap- \_ Setup Sequenz wird festgelegt, welche \_ \_ Konfigurationsparameter mit der streamingerfassung Sie können diese Nachricht explizit oder mithilfe des capcapturesetsetup-Makros senden.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- WM_CAP_SET_SEQUENCE_SETUP-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518953"
---
# <a name="wm_cap_set_sequence_setup-message"></a><span data-ttu-id="ec1eb-105">\_ \_ \_ \_ Setup Nachricht für die WM-Cap-Einrichtung</span><span class="sxs-lookup"><span data-stu-id="ec1eb-105">WM\_CAP\_SET\_SEQUENCE\_SETUP message</span></span>

<span data-ttu-id="ec1eb-106">Mit der Einstellung für die **WM- \_ Cap- \_ \_ \_ Setup Sequenz wird fest** gelegt, welche Konfigurationsparameter mit der streamingerfassung</span><span class="sxs-lookup"><span data-stu-id="ec1eb-106">The **WM\_CAP\_SET\_SEQUENCE\_SETUP** message sets the configuration parameters used with streaming capture.</span></span> <span data-ttu-id="ec1eb-107">Sie können diese Nachricht explizit oder mithilfe des [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="ec1eb-107">You can send this message explicitly or by using the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro.</span></span>


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a><span data-ttu-id="ec1eb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec1eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec1eb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wsize*</span><span class="sxs-lookup"><span data-stu-id="ec1eb-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="ec1eb-110">Größe (in Bytes) der Struktur, auf die von **s** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ec1eb-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="ec1eb-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*pscapparms*</span><span class="sxs-lookup"><span data-stu-id="ec1eb-111"><span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*</span></span>
</dt> <dd>

<span data-ttu-id="ec1eb-112">Zeiger auf eine [**captureparms**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ec1eb-112">Pointer to a [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec1eb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ec1eb-113">Return Value</span></span>

<span data-ttu-id="ec1eb-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ec1eb-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec1eb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec1eb-115">Remarks</span></span>

<span data-ttu-id="ec1eb-116">Informationen zu den Parametern, die zum Steuern der streamingerfassung verwendet werden, finden Sie in der Struktur von [**captuprojektms**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="ec1eb-116">For information about the parameters used to control streaming capture, see the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1eb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec1eb-117">Requirements</span></span>



| <span data-ttu-id="ec1eb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec1eb-118">Requirement</span></span> | <span data-ttu-id="ec1eb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ec1eb-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec1eb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec1eb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1eb-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec1eb-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec1eb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec1eb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1eb-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec1eb-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec1eb-124">Header</span><span class="sxs-lookup"><span data-stu-id="ec1eb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec1eb-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec1eb-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec1eb-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec1eb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1eb-127">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="ec1eb-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ec1eb-128">Video Erfassungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="ec1eb-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





