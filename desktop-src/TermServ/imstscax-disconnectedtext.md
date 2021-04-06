---
title: Imstscax disconnectedtext-Eigenschaft
description: Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Disconnectedtext-Eigenschaft Remotedesktopdienste
- Disconnectedtext-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
- Disconnectedtext-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, disconnectedtext-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742128"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="df931-124">Imstscax::D isconnectedtext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df931-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="df931-125">Gibt den Text an, der im-Steuerelement zentriert angezeigt wird, bevor eine Verbindung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="df931-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="df931-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="df931-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df931-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="df931-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="df931-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="df931-128">Property value</span></span>

<span data-ttu-id="df931-129">Der neue Anzeige Text.</span><span class="sxs-lookup"><span data-stu-id="df931-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="df931-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="df931-130">Error codes</span></span>

<span data-ttu-id="df931-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="df931-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="df931-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df931-132">Remarks</span></span>

<span data-ttu-id="df931-133">Das Festlegen der **disconnectedtext** -Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="df931-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="df931-134">Wenn Sie nicht angegeben ist, wird das Steuerelement leer angezeigt, bevor eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="df931-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="df931-135">Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="df931-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="df931-136">Die Methode gibt " **E \_ Fail** " zurück, wenn Sie aufgerufen wird, nachdem das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="df931-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="df931-137">Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="df931-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="df931-138">Mit dieser Methode wird der erforderliche Speicherplatz für den Puffer zugewiesen, auf den der *pdisconnectedtext* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="df931-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="df931-139">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="df931-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="df931-140">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df931-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="df931-141">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="df931-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="df931-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df931-142">Requirements</span></span>



| <span data-ttu-id="df931-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df931-143">Requirement</span></span> | <span data-ttu-id="df931-144">Wert</span><span class="sxs-lookup"><span data-stu-id="df931-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df931-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df931-145">Minimum supported client</span></span><br/> | <span data-ttu-id="df931-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df931-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df931-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df931-147">Minimum supported server</span></span><br/> | <span data-ttu-id="df931-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df931-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df931-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="df931-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="df931-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df931-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df931-151">DLL</span><span class="sxs-lookup"><span data-stu-id="df931-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df931-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df931-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="df931-153">IID</span><span class="sxs-lookup"><span data-stu-id="df931-153">IID</span></span><br/>                      | <span data-ttu-id="df931-154">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="df931-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="df931-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df931-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df931-156">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="df931-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="df931-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="df931-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="df931-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="df931-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="df931-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="df931-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="df931-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="df931-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="df931-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="df931-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="df931-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="df931-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="df931-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="df931-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="df931-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="df931-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="df931-165">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="df931-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

