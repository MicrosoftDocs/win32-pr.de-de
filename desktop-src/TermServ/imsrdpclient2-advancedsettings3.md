---
title: IMsRdpClient2 AdvancedSettings3-Eigenschaft
description: Ruft einen Zeiger auf die IMsRdpClientAdvancedSettings2-Schnittstelle ab. Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- AdvancedSettings3-Eigenschaft Remotedesktopdienste
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
- AdvancedSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings3-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340817"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="14a1d-123">IMsRdpClient2:: AdvancedSettings3-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14a1d-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="14a1d-124">Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="14a1d-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="14a1d-125">Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="14a1d-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="14a1d-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="14a1d-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a1d-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="14a1d-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="14a1d-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="14a1d-128">Property value</span></span>

<span data-ttu-id="14a1d-129">Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="14a1d-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="14a1d-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="14a1d-130">Error codes</span></span>

<span data-ttu-id="14a1d-131">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="14a1d-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="14a1d-132">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="14a1d-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a1d-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14a1d-133">Remarks</span></span>

<span data-ttu-id="14a1d-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="14a1d-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="14a1d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14a1d-135">Requirements</span></span>



| <span data-ttu-id="14a1d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14a1d-136">Requirement</span></span> | <span data-ttu-id="14a1d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="14a1d-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14a1d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14a1d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="14a1d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14a1d-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="14a1d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14a1d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="14a1d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14a1d-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="14a1d-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="14a1d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="14a1d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a1d-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14a1d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="14a1d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14a1d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a1d-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="14a1d-146">IID</span><span class="sxs-lookup"><span data-stu-id="14a1d-146">IID</span></span><br/>                      | <span data-ttu-id="14a1d-147">IID \_ IMsRdpClient2 ist als e7e17dc4-3b71-4ba7-a8e6-281ffadca28f definiert.</span><span class="sxs-lookup"><span data-stu-id="14a1d-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="14a1d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14a1d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a1d-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="14a1d-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="14a1d-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="14a1d-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="14a1d-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="14a1d-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="14a1d-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="14a1d-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="14a1d-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="14a1d-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="14a1d-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="14a1d-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="14a1d-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="14a1d-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="14a1d-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="14a1d-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="14a1d-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="14a1d-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





