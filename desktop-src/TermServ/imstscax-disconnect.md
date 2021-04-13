---
title: Imstscax Disconnect-Methode
description: Trennt die aktive Verbindung.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Disconnect-Methode Remotedesktopdienste
- Disconnect-Methode Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Disconnect-Methode
- Disconnect-Methode Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Disconnect-Methode
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518179"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="076dd-124">Imstscax::D isconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="076dd-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="076dd-125">Trennt die aktive Verbindung.</span><span class="sxs-lookup"><span data-stu-id="076dd-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="076dd-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="076dd-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="076dd-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="076dd-127">Parameters</span></span>

<span data-ttu-id="076dd-128">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="076dd-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="076dd-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="076dd-129">Return value</span></span>

<span data-ttu-id="076dd-130">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="076dd-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="076dd-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="076dd-131">Remarks</span></span>

<span data-ttu-id="076dd-132">Diese Methode gibt einen Fehlerwert zurück, wenn Sie aufgerufen wird, wenn das Steuerelement nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="076dd-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="076dd-133">Es ist auch möglich, das Steuerelement zu trennen, indem das Hauptfenster geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="076dd-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="076dd-134">Wenn das Steuerelement z. b. auf einer Webseite gehostet wird, ist es nicht erforderlich, diese Methode vor dem belassen der Seite aufzurufen. durch das Schließen des-Steuer Elements wird eine Verbindungs Trennung ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="076dd-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="076dd-135">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="076dd-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="076dd-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="076dd-136">Requirements</span></span>



| <span data-ttu-id="076dd-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="076dd-137">Requirement</span></span> | <span data-ttu-id="076dd-138">Wert</span><span class="sxs-lookup"><span data-stu-id="076dd-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="076dd-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="076dd-139">Minimum supported client</span></span><br/> | <span data-ttu-id="076dd-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="076dd-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="076dd-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="076dd-141">Minimum supported server</span></span><br/> | <span data-ttu-id="076dd-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="076dd-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="076dd-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="076dd-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="076dd-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076dd-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="076dd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="076dd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="076dd-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076dd-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="076dd-147">IID</span><span class="sxs-lookup"><span data-stu-id="076dd-147">IID</span></span><br/>                      | <span data-ttu-id="076dd-148">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="076dd-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="076dd-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="076dd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076dd-150">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="076dd-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="076dd-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="076dd-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="076dd-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="076dd-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="076dd-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="076dd-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="076dd-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="076dd-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="076dd-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="076dd-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="076dd-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="076dd-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="076dd-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="076dd-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="076dd-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="076dd-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="076dd-159">**Verbinden**</span><span class="sxs-lookup"><span data-stu-id="076dd-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="076dd-160">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="076dd-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





