---
title: Imstscax-Version (Eigenschaft)
description: Gibt die Versionsnummer des aktuellen Steuer Elements an.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Versions Eigenschaft Remotedesktopdienste
- Versions Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, Version-Eigenschaft
- Versions Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, Version-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476737"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="06d75-124">Imstscax:: Version-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="06d75-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="06d75-125">Gibt die Versionsnummer des aktuellen Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="06d75-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="06d75-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="06d75-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d75-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="06d75-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="06d75-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="06d75-128">Property value</span></span>

<span data-ttu-id="06d75-129">Die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="06d75-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="06d75-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="06d75-130">Error codes</span></span>

<span data-ttu-id="06d75-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="06d75-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d75-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06d75-132">Remarks</span></span>

<span data-ttu-id="06d75-133">Mit dieser Methode wird der erforderliche Speicherplatz für den Puffer zugewiesen, auf den der *pVersion* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="06d75-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="06d75-134">Beim Aufrufen von C/C++-Anwendungen muss der Arbeitsspeicher durch einen Aufruf der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06d75-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="06d75-135">Dies ist für Visual Basic-und Skript Clients nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06d75-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="06d75-136">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="06d75-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06d75-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06d75-137">Requirements</span></span>



| <span data-ttu-id="06d75-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06d75-138">Requirement</span></span> | <span data-ttu-id="06d75-139">Wert</span><span class="sxs-lookup"><span data-stu-id="06d75-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06d75-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06d75-140">Minimum supported client</span></span><br/> | <span data-ttu-id="06d75-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06d75-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="06d75-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06d75-142">Minimum supported server</span></span><br/> | <span data-ttu-id="06d75-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06d75-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="06d75-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="06d75-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="06d75-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06d75-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="06d75-146">DLL</span><span class="sxs-lookup"><span data-stu-id="06d75-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06d75-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06d75-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="06d75-148">IID</span><span class="sxs-lookup"><span data-stu-id="06d75-148">IID</span></span><br/>                      | <span data-ttu-id="06d75-149">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="06d75-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="06d75-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06d75-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d75-151">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="06d75-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="06d75-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="06d75-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="06d75-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="06d75-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="06d75-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="06d75-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="06d75-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="06d75-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="06d75-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="06d75-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="06d75-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="06d75-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="06d75-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="06d75-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="06d75-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="06d75-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="06d75-160">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="06d75-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

