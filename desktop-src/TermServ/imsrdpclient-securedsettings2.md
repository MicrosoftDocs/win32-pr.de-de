---
title: Imsrdpclient SecuredSettings2 (Eigenschaft)
description: Ruft einen Zeiger auf die imsrdpclientsecuredsettings-Schnittstelle ab. Diese Schnittstelle kann verwendet werden, um gesicherte Einstellungen für das Client Steuerelement festzulegen.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- SecuredSettings2-Eigenschaft Remotedesktopdienste
- SecuredSettings2-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
- SecuredSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, SecuredSettings2-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517366"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="cfae2-125">Imsrdpclient:: SecuredSettings2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cfae2-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="cfae2-126">Ruft einen Zeiger auf die [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="cfae2-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="cfae2-127">Diese Schnittstelle kann verwendet werden, um gesicherte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cfae2-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="cfae2-128">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cfae2-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfae2-129">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfae2-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="cfae2-130">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cfae2-130">Property value</span></span>

<span data-ttu-id="cfae2-131">Ein [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="cfae2-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cfae2-132">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cfae2-132">Error codes</span></span>

<span data-ttu-id="cfae2-133">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfae2-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="cfae2-134">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cfae2-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfae2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfae2-135">Remarks</span></span>

<span data-ttu-id="cfae2-136">Weitere Informationen finden Sie unter der [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md) -Schnittstelle und unter [Bereitstellen von RDP-Client Sicherheit](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="cfae2-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="cfae2-137">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cfae2-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfae2-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfae2-138">Requirements</span></span>



| <span data-ttu-id="cfae2-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfae2-139">Requirement</span></span> | <span data-ttu-id="cfae2-140">Wert</span><span class="sxs-lookup"><span data-stu-id="cfae2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfae2-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfae2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cfae2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfae2-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cfae2-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfae2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cfae2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfae2-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cfae2-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cfae2-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfae2-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfae2-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfae2-147">DLL</span><span class="sxs-lookup"><span data-stu-id="cfae2-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfae2-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfae2-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfae2-149">IID</span><span class="sxs-lookup"><span data-stu-id="cfae2-149">IID</span></span><br/>                      | <span data-ttu-id="cfae2-150">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="cfae2-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="cfae2-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfae2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfae2-152">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="cfae2-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="cfae2-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="cfae2-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="cfae2-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="cfae2-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="cfae2-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="cfae2-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="cfae2-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="cfae2-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="cfae2-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="cfae2-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="cfae2-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="cfae2-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="cfae2-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="cfae2-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="cfae2-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="cfae2-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="cfae2-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="cfae2-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





