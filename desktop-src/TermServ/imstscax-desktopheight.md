---
title: Imstscax desktopheight (Eigenschaft)
description: Gibt die Höhe des aktuellen Steuer Elements auf dem anfänglichen Remote Desktop in Pixel an.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Desktopheight-Eigenschaft Remotedesktopdienste
- Desktopheight-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
- Desktopheight-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, desktopheight-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956753"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="1c22c-124">Imstscax::D esktopheight-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1c22c-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="1c22c-125">Gibt die Höhe des aktuellen Steuer Elements auf dem anfänglichen Remote Desktop in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="1c22c-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="1c22c-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1c22c-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c22c-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c22c-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="1c22c-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1c22c-128">Property value</span></span>

<span data-ttu-id="1c22c-129">Die neue Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="1c22c-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c22c-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1c22c-130">Error codes</span></span>

<span data-ttu-id="1c22c-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1c22c-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c22c-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c22c-132">Remarks</span></span>

<span data-ttu-id="1c22c-133">Das Festlegen der **desktopheight** -Eigenschaft ist optional, muss jedoch vor dem Aufrufen der [**Connect**](imstscax-connect.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1c22c-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="1c22c-134">Wenn keine Desktop Höhe angegeben wird oder auf 0 (null) festgelegt ist, wird die Höhe des Desktops auf die Höhe des Steuer Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c22c-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="1c22c-135">Die Mindest-und Höchstwerte sind abhängig von der Betriebssystemversion des Remotedesktop Clients.</span><span class="sxs-lookup"><span data-stu-id="1c22c-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="1c22c-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c22c-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="1c22c-137">200 minimal, 8192 maximal</span><span class="sxs-lookup"><span data-stu-id="1c22c-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="1c22c-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c22c-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="1c22c-139">200 minimal, 2048 maximal</span><span class="sxs-lookup"><span data-stu-id="1c22c-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="1c22c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c22c-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="1c22c-141">200 minimal, 1200 maximal</span><span class="sxs-lookup"><span data-stu-id="1c22c-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="1c22c-142">Nachdem eine Verbindung hergestellt wurde, ändern alle Änderungen an der Höhe des Steuer Elements nicht die Höhe des Remote Desktops.</span><span class="sxs-lookup"><span data-stu-id="1c22c-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="1c22c-143">Stattdessen ruft das Steuerelement nach Bedarf Bild Lauf leisten auf oder zentriert den Remote Desktop.</span><span class="sxs-lookup"><span data-stu-id="1c22c-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="1c22c-144">Verwenden Sie die [**IMsRdpClient8:: Reconnect**](imsrdpclient8-reconnect.md) -Methode, um die Desktop Größe einer aktiven Verbindung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1c22c-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="1c22c-145">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1c22c-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c22c-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c22c-146">Requirements</span></span>



| <span data-ttu-id="1c22c-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c22c-147">Requirement</span></span> | <span data-ttu-id="1c22c-148">Wert</span><span class="sxs-lookup"><span data-stu-id="1c22c-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c22c-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c22c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1c22c-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c22c-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c22c-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c22c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1c22c-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c22c-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c22c-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1c22c-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c22c-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c22c-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c22c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1c22c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c22c-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c22c-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c22c-157">IID</span><span class="sxs-lookup"><span data-stu-id="1c22c-157">IID</span></span><br/>                      | <span data-ttu-id="1c22c-158">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="1c22c-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1c22c-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c22c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c22c-160">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="1c22c-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="1c22c-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="1c22c-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="1c22c-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="1c22c-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="1c22c-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="1c22c-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="1c22c-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="1c22c-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="1c22c-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="1c22c-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="1c22c-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1c22c-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1c22c-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1c22c-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1c22c-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1c22c-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1c22c-169">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="1c22c-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





