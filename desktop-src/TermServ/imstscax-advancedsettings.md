---
title: Imstscax advancedsettings-Eigenschaft
description: Ruft einen imstscadvancedsettings-Schnittstellen Zeiger ab.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Advancedsettings-Eigenschaft Remotedesktopdienste
- Advancedsettings-Eigenschaft Remotedesktopdienste, imstscax-Schnittstelle
- Imstscax-Schnittstelle Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, imsrdpclient-Schnittstelle
- Imsrdpclient-Schnittstelle Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient2-Schnittstelle
- IMsRdpClient2 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
- Advancedsettings-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, advancedsettings-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956460"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="200fc-124">Imstscax:: advancedsettings-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="200fc-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="200fc-125">Ruft einen [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="200fc-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="200fc-126">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="200fc-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="200fc-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="200fc-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="200fc-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="200fc-128">Property value</span></span>

<span data-ttu-id="200fc-129">Ein [**imstscadvancedsettings**](imstscadvancedsettings-interface.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="200fc-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="200fc-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="200fc-130">Error codes</span></span>

<span data-ttu-id="200fc-131">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="200fc-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="200fc-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="200fc-132">Remarks</span></span>

<span data-ttu-id="200fc-133">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="200fc-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="200fc-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="200fc-134">Requirements</span></span>



| <span data-ttu-id="200fc-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="200fc-135">Requirement</span></span> | <span data-ttu-id="200fc-136">Wert</span><span class="sxs-lookup"><span data-stu-id="200fc-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="200fc-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="200fc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="200fc-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="200fc-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="200fc-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="200fc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="200fc-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="200fc-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="200fc-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="200fc-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="200fc-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200fc-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="200fc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="200fc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="200fc-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200fc-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="200fc-145">IID</span><span class="sxs-lookup"><span data-stu-id="200fc-145">IID</span></span><br/>                      | <span data-ttu-id="200fc-146">IID \_ imstscax ist als 8c11efae-92c3-11d1-bc1e-00c04fa31489 definiert.</span><span class="sxs-lookup"><span data-stu-id="200fc-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="200fc-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="200fc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200fc-148">**Imsrdpclient**</span><span class="sxs-lookup"><span data-stu-id="200fc-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="200fc-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="200fc-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="200fc-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="200fc-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="200fc-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="200fc-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="200fc-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="200fc-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="200fc-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="200fc-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="200fc-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="200fc-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="200fc-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="200fc-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="200fc-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="200fc-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="200fc-157">**Imstscax**</span><span class="sxs-lookup"><span data-stu-id="200fc-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





