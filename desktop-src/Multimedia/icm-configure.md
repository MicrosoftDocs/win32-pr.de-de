---
title: ICM_CONFIGURE Meldung (VFW. h)
description: In der ICM-Konfigurations \_ Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Konfigurations Dialogfeld anzuzeigen oder einen Video Komprimierungs Treiber zu Fragen
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342868"
---
# <a name="icm_configure-message"></a><span data-ttu-id="55a0d-104">ICM- \_ Konfigurations Meldung</span><span class="sxs-lookup"><span data-stu-id="55a0d-104">ICM\_CONFIGURE message</span></span>

<span data-ttu-id="55a0d-105">In der **ICM- \_ Konfigurations** Meldung wird ein Video Komprimierungs Treiber benachrichtigt, um das Konfigurations Dialogfeld anzuzeigen oder einen Video Komprimierungs Treiber zu Fragen</span><span class="sxs-lookup"><span data-stu-id="55a0d-105">The **ICM\_CONFIGURE** message notifies a video compression driver to display its configuration dialog box or queries a video compression driver to determine if it has a configuration dialog box.</span></span> <span data-ttu-id="55a0d-106">Sie können diese Nachricht explizit oder mithilfe des [**icconfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="55a0d-106">You can send this message explicitly or by using the [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) macro.</span></span>


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="55a0d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55a0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55a0d-108"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="55a0d-108"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="55a0d-109">Handle für das übergeordnete Fenster des angezeigten Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="55a0d-109">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="55a0d-110">Sie können feststellen, ob ein Treiber über ein Konfigurations Dialogfeld verfügt, indem Sie 1 in diesem Parameter angeben, wie im [**icqueryconfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) -Makro.</span><span class="sxs-lookup"><span data-stu-id="55a0d-110">You can determine if a driver has a configuration dialog box by specifying  1 in this parameter, as in the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55a0d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55a0d-111">Return Value</span></span>

<span data-ttu-id="55a0d-112">Gibt ICERR \_ OK zurück, wenn der Treiber diese Nachricht unterstützt oder wenn ICERR \_ andernfalls nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="55a0d-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a0d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55a0d-113">Remarks</span></span>

<span data-ttu-id="55a0d-114">Diese Meldung unterscheidet sich von der für die Hardwarekonfiguration verwendeten drv-Konfigurations Nachricht. [**\_**](drv-configure.md)</span><span class="sxs-lookup"><span data-stu-id="55a0d-114">This message is different from the [**DRV\_CONFIGURE**](drv-configure.md) message used for hardware configuration.</span></span> <span data-ttu-id="55a0d-115">Im Dialogfeld für diese Meldung soll der Benutzer den internen Zustand festlegen und bearbeiten können, auf den die ICM-Meldungen " [**\_ GetState**](icm-getstate.md) " und " [**ICM \_ SetState**](icm-setstate.md) " verweisen.</span><span class="sxs-lookup"><span data-stu-id="55a0d-115">The dialog box for this message should let the user set and edit the internal state referenced by the [**ICM\_GETSTATE**](icm-getstate.md) and [**ICM\_SETSTATE**](icm-setstate.md) messages.</span></span> <span data-ttu-id="55a0d-116">Mithilfe dieses Dialog Felds kann der Benutzer beispielsweise die Parameter ändern, die die Qualitätsstufe und andere ähnliche Komprimierungs Optionen beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="55a0d-116">For example, this dialog box can let the user change parameters affecting the quality level and other similar compression options.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a0d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55a0d-117">Requirements</span></span>



| <span data-ttu-id="55a0d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55a0d-118">Requirement</span></span> | <span data-ttu-id="55a0d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="55a0d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="55a0d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55a0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55a0d-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a0d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="55a0d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55a0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55a0d-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55a0d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="55a0d-124">Header</span><span class="sxs-lookup"><span data-stu-id="55a0d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a0d-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a0d-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a0d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55a0d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a0d-127">Videokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="55a0d-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="55a0d-128">Video Komprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="55a0d-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





