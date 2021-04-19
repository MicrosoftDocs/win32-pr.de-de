---
title: Imstscax securedsettingsenabled (Eigenschaft)
description: Gibt an, ob die imstscsecuredsettings-Schnittstelle verfügbar ist. Das heißt, ob sich die Webseite, die das Steuerelement enthält, derzeit in einer der zulässigen Internet Explorer-URL-Sicherheitszonen befindet.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
- Securedsettingsenabled-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, securedsettingsenabled (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342658"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="676fa-125">Imstscax:: securedsettingsenabled (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="676fa-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="676fa-126">Gibt an, ob die [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="676fa-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="676fa-127">Das heißt, ob sich die Webseite, die das Steuerelement enthält, derzeit in einer der zulässigen Internet Explorer-URL-Sicherheitszonen befindet.</span><span class="sxs-lookup"><span data-stu-id="676fa-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="676fa-128">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="676fa-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="676fa-129">Syntax</span><span class="sxs-lookup"><span data-stu-id="676fa-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="676fa-130">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="676fa-130">Property value</span></span>

<span data-ttu-id="676fa-131">Der Wert dieses Parameters ist **true** , wenn die Schnittstelle verfügbar ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="676fa-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="676fa-132">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="676fa-132">Error codes</span></span>

<span data-ttu-id="676fa-133">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="676fa-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="676fa-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="676fa-134">Remarks</span></span>

<span data-ttu-id="676fa-135">Verwenden Sie diese Methode, um abzufragen, ob die [**imstscsecuredsettings**](imstscsecuredsettings-interface.md) -Schnittstelle verfügbar ist, bevor die [**securedsettings**](imstscax-securedsettings.md) -Eigenschaft abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="676fa-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="676fa-136">Eine Liste der eingeschränkten URL-Sicherheitszonen finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="676fa-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="676fa-137">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="676fa-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="676fa-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="676fa-138">Requirements</span></span>



| <span data-ttu-id="676fa-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="676fa-139">Requirement</span></span> | <span data-ttu-id="676fa-140">Wert</span><span class="sxs-lookup"><span data-stu-id="676fa-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="676fa-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="676fa-141">Minimum supported client</span></span><br/> | <span data-ttu-id="676fa-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="676fa-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="676fa-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="676fa-143">Minimum supported server</span></span><br/> | <span data-ttu-id="676fa-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="676fa-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="676fa-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="676fa-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="676fa-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676fa-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="676fa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="676fa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="676fa-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="676fa-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="676fa-149">IID</span><span class="sxs-lookup"><span data-stu-id="676fa-149">IID</span></span><br/>                      | <span data-ttu-id="676fa-150">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="676fa-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="676fa-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="676fa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676fa-152">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="676fa-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="676fa-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="676fa-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="676fa-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="676fa-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="676fa-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="676fa-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="676fa-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="676fa-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="676fa-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="676fa-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="676fa-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="676fa-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="676fa-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="676fa-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="676fa-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="676fa-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="676fa-161">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="676fa-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="676fa-162">**Imstscsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="676fa-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





