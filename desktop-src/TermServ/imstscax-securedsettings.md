---
title: Imstscax securedsettings (Eigenschaft)
description: Ruft einen imstscsecuredsettings-Schnittstellen Zeiger ab.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Securedsettings-Eigenschaft Remotedesktopdienste
- Securedsettings-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, securedsettings-Eigenschaft
- Securedsettings-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, securedsettings-Eigenschaft
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
- Securedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, securedsettings (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103683"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="b2f38-124">Imstscax:: securedsettings-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2f38-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="b2f38-125">Ruft einen [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="b2f38-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="b2f38-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b2f38-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f38-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2f38-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="b2f38-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b2f38-128">Property value</span></span>

<span data-ttu-id="b2f38-129">Ein [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b2f38-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2f38-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b2f38-130">Error codes</span></span>

<span data-ttu-id="b2f38-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b2f38-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f38-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2f38-132">Remarks</span></span>

<span data-ttu-id="b2f38-133">Wenn das Steuerelement auf einer Webseite gehostet wird und die aktuelle Internet Explorer-URL-Sicherheitszone das Abrufen der Schnittstellen Adresse nicht zulässt, gibt diese Methode **E \_ Fail** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2f38-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="b2f38-134">Einschränkungen bei der Verfügbarkeit der [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle finden Sie unter [**securedsettingsenabled**](imstscax-securedsettingsenabled.md) .</span><span class="sxs-lookup"><span data-stu-id="b2f38-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="b2f38-135">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b2f38-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f38-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2f38-136">Requirements</span></span>



| <span data-ttu-id="b2f38-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2f38-137">Requirement</span></span> | <span data-ttu-id="b2f38-138">Wert</span><span class="sxs-lookup"><span data-stu-id="b2f38-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f38-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b2f38-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b2f38-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2f38-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b2f38-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b2f38-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b2f38-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2f38-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b2f38-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b2f38-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2f38-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2f38-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2f38-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b2f38-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2f38-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2f38-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2f38-147">IID</span><span class="sxs-lookup"><span data-stu-id="b2f38-147">IID</span></span><br/>                      | <span data-ttu-id="b2f38-148">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="b2f38-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="b2f38-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2f38-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f38-150">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="b2f38-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="b2f38-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="b2f38-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="b2f38-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="b2f38-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="b2f38-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="b2f38-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="b2f38-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="b2f38-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="b2f38-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="b2f38-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="b2f38-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b2f38-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b2f38-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b2f38-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b2f38-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b2f38-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b2f38-159">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="b2f38-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="b2f38-160">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="b2f38-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





