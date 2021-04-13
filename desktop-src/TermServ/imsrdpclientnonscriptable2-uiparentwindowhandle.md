---
title: IMsRdpClientNonScriptable2 uianentwindowhandle-Eigenschaft
description: Legt das Fenster Handle fest, das das übergeordnete Fenster für alle Dialogfelder ist, die vom Steuerelement angezeigt werden, oder ruft es ab. Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
- Uiparamegenwindowhandle-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, uiparameentwindowhandle-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475225"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="3de79-113">IMsRdpClientNonScriptable2:: uianentwindowhandle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3de79-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="3de79-114">Legt das Fenster Handle fest, das das übergeordnete Fenster für alle Dialogfelder ist, die vom Steuerelement angezeigt werden, oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="3de79-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="3de79-115">Dadurch können alle Fenster, die vom Steuerelement angezeigt werden, in Bezug auf alle Fenster, die von der übergeordneten Anwendung angezeigt werden, ordnungsgemäß modal sein.</span><span class="sxs-lookup"><span data-stu-id="3de79-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="3de79-116">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3de79-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de79-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="3de79-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="3de79-118">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3de79-118">Property value</span></span>

<span data-ttu-id="3de79-119">Das neue Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="3de79-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3de79-120">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3de79-120">Error codes</span></span>

<span data-ttu-id="3de79-121">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3de79-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de79-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3de79-122">Remarks</span></span>

<span data-ttu-id="3de79-123">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3de79-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3de79-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3de79-124">Requirements</span></span>



| <span data-ttu-id="3de79-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3de79-125">Requirement</span></span> | <span data-ttu-id="3de79-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3de79-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de79-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3de79-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3de79-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3de79-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="3de79-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3de79-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3de79-130">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="3de79-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="3de79-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3de79-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="3de79-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3de79-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3de79-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3de79-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3de79-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3de79-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="3de79-135">IID</span><span class="sxs-lookup"><span data-stu-id="3de79-135">IID</span></span><br/>                      | <span data-ttu-id="3de79-136">IID \_ IMsRdpClientNonScriptable2 ist als 17a5e535-4072-4fa4-af32-c8d0d47345e9 definiert.</span><span class="sxs-lookup"><span data-stu-id="3de79-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3de79-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3de79-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de79-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="3de79-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="3de79-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="3de79-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="3de79-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="3de79-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="3de79-141">**Onauthenticationwarningangezeigte**</span><span class="sxs-lookup"><span data-stu-id="3de79-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="3de79-142">**Onauthenticationwarningverworfen**</span><span class="sxs-lookup"><span data-stu-id="3de79-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="3de79-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="3de79-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





