---
title: Imstscax-Domänen Eigenschaft
description: Gibt die Domäne an, an der der aktuelle Benutzer sich anmeldet.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Domänen Eigenschaft Remotedesktopdienste
- Domänen Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
- Domänen Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957063"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="4d016-124">Imstscax::D omain-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d016-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="4d016-125">Gibt die Domäne an, an der der aktuelle Benutzer sich anmeldet.</span><span class="sxs-lookup"><span data-stu-id="4d016-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="4d016-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4d016-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d016-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d016-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="4d016-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4d016-128">Property value</span></span>

<span data-ttu-id="4d016-129">Der neue Domänen Name.</span><span class="sxs-lookup"><span data-stu-id="4d016-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d016-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4d016-130">Error codes</span></span>

<span data-ttu-id="4d016-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4d016-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d016-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d016-132">Remarks</span></span>

<span data-ttu-id="4d016-133">Das Festlegen der **Domänen** Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="4d016-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="4d016-134">Wenn Sie nicht festgelegt ist, kann der Benutzer eine Domäne auswählen, wenn das Windows-Anmelde Dialogfeld während der Verbindung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4d016-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="4d016-135">Die **get \_ Domain** -Methode ordnet den erforderlichen Arbeitsspeicher für den Puffer zu, auf den der *pdomain* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="4d016-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="4d016-136">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4d016-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="4d016-137">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4d016-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="4d016-138">Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="4d016-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="4d016-139">Es wird ein Fehler zurückgegeben, wenn er aufgerufen wird **, wenn das \_** Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4d016-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="4d016-140">Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="4d016-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="4d016-141">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4d016-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d016-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d016-142">Requirements</span></span>



| <span data-ttu-id="4d016-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d016-143">Requirement</span></span> | <span data-ttu-id="4d016-144">Wert</span><span class="sxs-lookup"><span data-stu-id="4d016-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d016-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d016-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4d016-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d016-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4d016-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d016-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4d016-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d016-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4d016-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4d016-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d016-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d016-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d016-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4d016-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d016-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d016-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4d016-153">IID</span><span class="sxs-lookup"><span data-stu-id="4d016-153">IID</span></span><br/>                      | <span data-ttu-id="4d016-154">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="4d016-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4d016-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d016-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d016-156">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="4d016-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="4d016-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="4d016-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="4d016-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4d016-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4d016-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4d016-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4d016-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4d016-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4d016-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4d016-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4d016-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4d016-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4d016-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4d016-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4d016-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4d016-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4d016-165">**Verbunden**</span><span class="sxs-lookup"><span data-stu-id="4d016-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="4d016-166">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="4d016-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="4d016-167">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="4d016-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

