---
title: Imstscnonscriptable cleartextpassword (Eigenschaft)
description: Legt das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format fest.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Cleartextpassword-Eigenschaft Remotedesktopdienste
- Cleartextpassword-Eigenschaft Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, imsrdpclientnonscriptable-Schnittstelle
- Imsrdpclientnonscriptable-Schnittstelle Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable2-Schnittstelle
- IMsRdpClientNonScriptable2 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
- Cleartextpassword-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, cleartextpassword (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743528"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="6ff8b-124">Imstscnonscriptable:: cleartextpassword-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ff8b-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="6ff8b-125">Legt das Remotedesktop ActiveX-Steuerelement Kennwort im nur-Text-Format fest.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="6ff8b-126">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff8b-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ff8b-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="6ff8b-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6ff8b-128">Property value</span></span>

<span data-ttu-id="6ff8b-129">Das Kennwort, das zum Herstellen der Verbindung verwendet werden soll, angegeben im nur-Text-Format.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ff8b-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6ff8b-130">Error codes</span></span>

<span data-ttu-id="6ff8b-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff8b-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ff8b-132">Remarks</span></span>

<span data-ttu-id="6ff8b-133">Das Kennwort wird im sicheren verschlüsselten RDP-Kommunikationskanal an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="6ff8b-134">Nachdem ein Klartext-Kennwort festgelegt wurde, kann es nicht im nur-Text-Format abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="6ff8b-135">Die **cleartextpassword** -Eigenschaft kann nur festgelegt werden, wenn sich das Remotedesktop ActiveX-Steuerelement nicht im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="6ff8b-136">Das Festlegen dieser Eigenschaft schlägt fehl, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="6ff8b-137">Zum Überprüfen des verbundenen Zustands rufen Sie die [**imstscax:: Connected**](imstscax-connected.md) -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="6ff8b-138">Sie können diese Methode auch aufrufen, um ein nur-Text-Kennwort festzulegen, bevor Sie es in ein portables codiertes Kennwort oder ein binäres (nicht Portables) codiertes Kennwort umwandelt.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="6ff8b-139">Beachten Sie jedoch, dass codierte Kenn Wörter nicht als sicher verschlüsselt angesehen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="6ff8b-140">Wenn Sie diese Methode zum ersten Mal aufrufen, um ein Kennwort im nur-Text-Format festzulegen, können Sie das Kennwort in ein codiertes Format konvertieren.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="6ff8b-141">**So konvertieren Sie ein Klartext-Kennwort in ein codiertes Format**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="6ff8b-142">Legen Sie das Kennwort im Klartext-Format in der **cleartextpassword** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="6ff8b-143">Rufen Sie die Eigenschaft [**binarypassword**](imstscnonscriptable-binarypassword.md) und die Eigenschaften [**binarysalt**](imstscnonscriptable-binarysalt.md) ab, um das Kennwort im Binärformat (nicht portabel) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="6ff8b-144">Sowohl das codierte Kennwort als auch der Salt-Teil sind erforderlich, um ein Kennwort im Binärformat festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="6ff8b-145">Rufen Sie die [**portablepassword**](imstscnonscriptable-portablepassword.md) -Methode und die [**portablesalt**](imstscnonscriptable-portablesalt.md) -Eigenschaften ab, um das Kennwort im portablen codierten Format abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="6ff8b-146">Beide Teile sind erforderlich, um ein Kennwort im portablen codierten Format festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="6ff8b-147">Nachdem Sie die vorangegangenen drei Schritte ausgeführt haben, können Sie das Kennwort im codierten Format festlegen, indem Sie die Eigenschaften [**binarypassword**](imstscnonscriptable-binarypassword.md) und [**binarysalt**](imstscnonscriptable-binarysalt.md) oder [**portablepassword**](imstscnonscriptable-portablepassword.md) und [**portablesalt**](imstscnonscriptable-portablesalt.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="6ff8b-148">Beide Teile sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-148">Both parts are required.</span></span>

<span data-ttu-id="6ff8b-149">Um die automatische Anmeldung zu aktivieren, müssen Sie auch den [**Benutzernamen**](imstscax-username.md) und die [**Domänen**](imstscax-domain.md) Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="6ff8b-150">Wenn das Kennwort den Benutzer nicht authentifizieren kann, wird das Dialogfeld Windows-Anmeldung auf dem Server angezeigt, um den Benutzer zur Eingabe des Kennworts aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="6ff8b-151">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6ff8b-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff8b-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ff8b-152">Requirements</span></span>



| <span data-ttu-id="6ff8b-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ff8b-153">Requirement</span></span> | <span data-ttu-id="6ff8b-154">Wert</span><span class="sxs-lookup"><span data-stu-id="6ff8b-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff8b-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ff8b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff8b-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ff8b-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ff8b-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ff8b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff8b-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ff8b-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ff8b-159">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6ff8b-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ff8b-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ff8b-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ff8b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff8b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff8b-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ff8b-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ff8b-163">IID</span><span class="sxs-lookup"><span data-stu-id="6ff8b-163">IID</span></span><br/>                      | <span data-ttu-id="6ff8b-164">IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.</span><span class="sxs-lookup"><span data-stu-id="6ff8b-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ff8b-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ff8b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff8b-166">**Imsrdpclientnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="6ff8b-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="6ff8b-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="6ff8b-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="6ff8b-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6ff8b-171">**Imstscnonscriptable**</span><span class="sxs-lookup"><span data-stu-id="6ff8b-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





