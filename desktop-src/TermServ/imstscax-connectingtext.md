---
title: Imstscax connectingtext-Eigenschaft
description: Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Connectingtext-Eigenschaft Remotedesktopdienste
- Connectingtext-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
- Connectingtext-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, connectingtext-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392073"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="7f3dc-124">Imstscax:: connectingtext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7f3dc-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="7f3dc-125">Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, während das Steuerelement eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="7f3dc-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f3dc-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f3dc-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="7f3dc-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7f3dc-128">Property value</span></span>

<span data-ttu-id="7f3dc-129">Der neue Anzeige Text.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f3dc-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="7f3dc-130">Error codes</span></span>

<span data-ttu-id="7f3dc-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="7f3dc-132">Gibt ein **HRESULT** ungleich 0 (null) zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f3dc-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f3dc-133">Remarks</span></span>

<span data-ttu-id="7f3dc-134">Ein Beispiel für den Verbindungs Text lautet "Verbindung mit Server wird hergestellt...".</span><span class="sxs-lookup"><span data-stu-id="7f3dc-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="7f3dc-135">Das Festlegen der **connectingtext** -Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="7f3dc-136">Wenn Sie nicht festgelegt ist, wird das Steuerelement leer angezeigt, bevor eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="7f3dc-137">Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="7f3dc-138">Es wird ein Fehler zurückgegeben, wenn er aufgerufen wird **, wenn das \_** Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="7f3dc-139">Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="7f3dc-140">Die Eigenschaften Methode **get \_ connectingtext** ordnet den für den Puffer erforderlichen Arbeitsspeicher zu, auf den der *pconnectingtext* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="7f3dc-141">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="7f3dc-142">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="7f3dc-143">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7f3dc-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f3dc-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f3dc-144">Requirements</span></span>



| <span data-ttu-id="7f3dc-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f3dc-145">Requirement</span></span> | <span data-ttu-id="7f3dc-146">Wert</span><span class="sxs-lookup"><span data-stu-id="7f3dc-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f3dc-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f3dc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7f3dc-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f3dc-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7f3dc-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f3dc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7f3dc-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f3dc-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7f3dc-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7f3dc-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f3dc-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f3dc-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f3dc-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7f3dc-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f3dc-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f3dc-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f3dc-155">IID</span><span class="sxs-lookup"><span data-stu-id="7f3dc-155">IID</span></span><br/>                      | <span data-ttu-id="7f3dc-156">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="7f3dc-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7f3dc-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f3dc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f3dc-158">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7f3dc-167">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="7f3dc-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

