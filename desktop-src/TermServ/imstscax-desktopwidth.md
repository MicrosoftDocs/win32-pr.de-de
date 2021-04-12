---
title: Imstscax desktopwidth (Eigenschaft)
description: Gibt die Breite des aktuellen Steuer Elements auf dem ersten Remote Desktop in Pixel an.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Desktopwidth-Eigenschaft Remotedesktopdienste
- Desktopwidth-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
- Desktopwidth-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, desktopwidth-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517747"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="06a80-124">Imstscax::D esktopwidth-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="06a80-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="06a80-125">Gibt die Breite des aktuellen Steuer Elements auf dem ersten Remote Desktop in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="06a80-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="06a80-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="06a80-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06a80-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="06a80-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="06a80-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="06a80-128">Property value</span></span>

<span data-ttu-id="06a80-129">Die neue Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="06a80-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06a80-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="06a80-130">Error codes</span></span>

<span data-ttu-id="06a80-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="06a80-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a80-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06a80-132">Remarks</span></span>

<span data-ttu-id="06a80-133">Das Festlegen der **desktopwidth** -Eigenschaft ist optional, muss jedoch vor dem Aufrufen der [**Connect**](imstscax-connect.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="06a80-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="06a80-134">Wenn keine Desktop Breite angegeben wird oder auf 0 (null) festgelegt ist, wird die Breite des Desktops auf die Breite des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06a80-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="06a80-135">Die Mindest-und Höchstwerte sind abhängig von der Betriebssystemversion des Remotedesktop Clients.</span><span class="sxs-lookup"><span data-stu-id="06a80-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="06a80-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="06a80-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="06a80-137">200 minimal, 8192 maximal</span><span class="sxs-lookup"><span data-stu-id="06a80-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="06a80-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06a80-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="06a80-139">200 minimal, 2048 maximal</span><span class="sxs-lookup"><span data-stu-id="06a80-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="06a80-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06a80-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="06a80-141">200 minimal, 1200 maximal</span><span class="sxs-lookup"><span data-stu-id="06a80-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="06a80-142">Nachdem eine Verbindung hergestellt wurde, ändern alle Änderungen an der Breite des Steuer Elements nicht die Breite des Remote Desktops.</span><span class="sxs-lookup"><span data-stu-id="06a80-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="06a80-143">Stattdessen ruft das Steuerelement nach Bedarf Bild Lauf leisten auf oder zentriert den Remote Desktop.</span><span class="sxs-lookup"><span data-stu-id="06a80-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="06a80-144">Verwenden Sie die [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) -Methode, um die Desktop Größe einer aktiven Verbindung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="06a80-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="06a80-145">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="06a80-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06a80-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06a80-146">Requirements</span></span>



| <span data-ttu-id="06a80-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06a80-147">Requirement</span></span> | <span data-ttu-id="06a80-148">Wert</span><span class="sxs-lookup"><span data-stu-id="06a80-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06a80-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06a80-149">Minimum supported client</span></span><br/> | <span data-ttu-id="06a80-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06a80-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="06a80-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06a80-151">Minimum supported server</span></span><br/> | <span data-ttu-id="06a80-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06a80-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="06a80-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="06a80-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="06a80-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06a80-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="06a80-155">DLL</span><span class="sxs-lookup"><span data-stu-id="06a80-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06a80-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06a80-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="06a80-157">IID</span><span class="sxs-lookup"><span data-stu-id="06a80-157">IID</span></span><br/>                      | <span data-ttu-id="06a80-158">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="06a80-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="06a80-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06a80-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a80-160">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="06a80-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="06a80-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="06a80-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="06a80-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="06a80-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="06a80-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="06a80-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="06a80-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="06a80-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="06a80-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="06a80-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="06a80-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="06a80-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="06a80-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="06a80-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="06a80-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="06a80-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="06a80-169">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="06a80-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





