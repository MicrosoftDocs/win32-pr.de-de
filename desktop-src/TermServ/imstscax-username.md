---
title: Imstscax username (Eigenschaft)
description: Gibt die Anmelde Informationen für den Benutzernamen an.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Remotedesktopdienste
- Username-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, UserName-Eigenschaft
- Username-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, UserName-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479029"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="c4085-124">Imstscax:: Username-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4085-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="c4085-125">Gibt die Anmelde Informationen für den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="c4085-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="c4085-126">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c4085-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4085-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4085-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="c4085-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c4085-128">Property value</span></span>

<span data-ttu-id="c4085-129">Der neue Benutzername.</span><span class="sxs-lookup"><span data-stu-id="c4085-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4085-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c4085-130">Error codes</span></span>

<span data-ttu-id="c4085-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c4085-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4085-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4085-132">Remarks</span></span>

<span data-ttu-id="c4085-133">Das Festlegen der **username** -Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="c4085-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="c4085-134">Wenn Sie nicht angegeben ist, kann der Benutzer einen Benutzernamen angeben, wenn das Windows-Anmelde Dialogfeld während der Verbindung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4085-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="c4085-135">Diese Eigenschaft kann nur festgelegt werden, wenn sich das Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="c4085-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="c4085-136">Es wird ein Fehler zurückgegeben, wenn er aufgerufen wird **, wenn das \_** Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="c4085-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="c4085-137">Sie können überprüfen, ob das Steuerelement verbunden ist, indem Sie auf Verbindungs Ereignisse in [**imstscaxevents**](imstscaxevents-interface.md) reagieren oder die [**verbundene**](imstscax-connected.md) Eigenschaft untersuchen.</span><span class="sxs-lookup"><span data-stu-id="c4085-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="c4085-138">Mit der Eigenschaften Methode **get \_ username** wird der erforderliche Arbeitsspeicher für den Puffer zugewiesen, auf den der *pVersion* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="c4085-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="c4085-139">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4085-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="c4085-140">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c4085-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="c4085-141">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c4085-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4085-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4085-142">Requirements</span></span>



| <span data-ttu-id="c4085-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4085-143">Requirement</span></span> | <span data-ttu-id="c4085-144">Wert</span><span class="sxs-lookup"><span data-stu-id="c4085-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4085-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4085-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c4085-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4085-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4085-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4085-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c4085-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4085-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4085-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c4085-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4085-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4085-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4085-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c4085-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4085-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4085-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4085-153">IID</span><span class="sxs-lookup"><span data-stu-id="c4085-153">IID</span></span><br/>                      | <span data-ttu-id="c4085-154">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="c4085-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c4085-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4085-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4085-156">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="c4085-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c4085-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c4085-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c4085-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c4085-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c4085-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c4085-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c4085-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c4085-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c4085-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c4085-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c4085-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c4085-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c4085-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c4085-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c4085-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c4085-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c4085-165">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="c4085-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

