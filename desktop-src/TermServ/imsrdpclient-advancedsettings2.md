---
title: Imsrdpclient AdvancedSettings2 (Eigenschaft)
description: Ruft einen Zeiger auf die imsrdpclientadvancedsettings-Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- AdvancedSettings2-Eigenschaft Remotedesktopdienste
- AdvancedSettings2-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
- AdvancedSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings2-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340371"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="c0713-125">Imsrdpclient:: AdvancedSettings2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0713-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="c0713-126">Ruft einen Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="c0713-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="c0713-127">Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c0713-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="c0713-128">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c0713-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0713-129">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0713-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="c0713-130">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c0713-130">Property value</span></span>

<span data-ttu-id="c0713-131">Zeiger auf die [**imsrdpclientadvancedsettings**](imsrdpclientadvancedsettings-interface.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c0713-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="c0713-132">Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c0713-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0713-133">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c0713-133">Error codes</span></span>

<span data-ttu-id="c0713-134">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c0713-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="c0713-135">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c0713-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0713-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0713-136">Remarks</span></span>

<span data-ttu-id="c0713-137">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c0713-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0713-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0713-138">Requirements</span></span>



| <span data-ttu-id="c0713-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0713-139">Requirement</span></span> | <span data-ttu-id="c0713-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c0713-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0713-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0713-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c0713-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0713-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c0713-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0713-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c0713-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0713-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c0713-145">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c0713-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0713-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0713-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0713-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c0713-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0713-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0713-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0713-149">IID</span><span class="sxs-lookup"><span data-stu-id="c0713-149">IID</span></span><br/>                      | <span data-ttu-id="c0713-150">IID \_ imsrdpclient ist als 92b4a539-7115-4b7c-a5a9-e5d9efc2780a definiert.</span><span class="sxs-lookup"><span data-stu-id="c0713-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c0713-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0713-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0713-152">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="c0713-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="c0713-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="c0713-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="c0713-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="c0713-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="c0713-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="c0713-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="c0713-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="c0713-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="c0713-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="c0713-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="c0713-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c0713-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c0713-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c0713-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c0713-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c0713-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c0713-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c0713-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





