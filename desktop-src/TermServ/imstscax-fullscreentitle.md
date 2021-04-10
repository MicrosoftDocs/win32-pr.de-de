---
title: Imstscax fullscrebereberegenschaft
description: Gibt den Fenstertitel an, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Fullscrebereberegenschaft Remotedesktopdienste
- Fullscrebereberegenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, fullscrebereberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, fullscrebereberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, fullscreberegenschaft
- Fullscrebereberegenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, fullscreberegenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104325"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="2e737-124">Imstscax:: fullscreberegenschaft</span><span class="sxs-lookup"><span data-stu-id="2e737-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="2e737-125">Gibt den Fenstertitel an, der angezeigt wird, wenn sich das Steuerelement im Vollbildmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="2e737-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="2e737-126">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="2e737-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e737-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e737-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="2e737-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2e737-128">Property value</span></span>

<span data-ttu-id="2e737-129">Der Fenstertitel.</span><span class="sxs-lookup"><span data-stu-id="2e737-129">The window title.</span></span> <span data-ttu-id="2e737-130">Die maximale Länge dieser Zeichenfolge beträgt Max \_ . Pfad-1 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2e737-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2e737-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2e737-131">Error codes</span></span>

<span data-ttu-id="2e737-132">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2e737-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e737-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e737-133">Remarks</span></span>

<span data-ttu-id="2e737-134">Diese Eigenschaft wird verwendet, um den Titel des Steuer Elements des Steuer Elements festzulegen, wenn die Verbindung im Vollbildmodus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="2e737-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="2e737-135">Verwenden Sie diese Eigenschaft nicht für den Container behandelten Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="2e737-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="2e737-136">Wenn die [**imstscadvancedsettings::p UT \_ containerhandledfullscreen**](imstscadvancedsettings-containerhandledfullscreen.md) -Methode aufgerufen wird, zeigt das Containerfenster den Fenstertitel an.</span><span class="sxs-lookup"><span data-stu-id="2e737-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="2e737-137">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2e737-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e737-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e737-138">Requirements</span></span>



| <span data-ttu-id="2e737-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e737-139">Requirement</span></span> | <span data-ttu-id="2e737-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2e737-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e737-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e737-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2e737-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e737-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2e737-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e737-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2e737-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e737-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2e737-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2e737-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="2e737-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e737-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e737-147">DLL</span><span class="sxs-lookup"><span data-stu-id="2e737-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e737-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e737-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2e737-149">IID</span><span class="sxs-lookup"><span data-stu-id="2e737-149">IID</span></span><br/>                      | <span data-ttu-id="2e737-150">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="2e737-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="2e737-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e737-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e737-152">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="2e737-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="2e737-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="2e737-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="2e737-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="2e737-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="2e737-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="2e737-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="2e737-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="2e737-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="2e737-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="2e737-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="2e737-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2e737-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2e737-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2e737-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2e737-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2e737-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2e737-161">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="2e737-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





