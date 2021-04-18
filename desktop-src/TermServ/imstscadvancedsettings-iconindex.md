---
title: Imstscadvancedsettings IconIndex-Eigenschaft
description: Gibt den Index des Symbols in der aktuellen Symbol Datei an.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- IconIndex-Eigenschaft Remotedesktopdienste
- IconIndex-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, IconIndex-Eigenschaft
- IconIndex-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, IconIndex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517750"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="766df-122">Imstscadvancedsettings:: IconIndex-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="766df-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="766df-123">Gibt den Index des Symbols in der aktuellen Symbol Datei an.</span><span class="sxs-lookup"><span data-stu-id="766df-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="766df-124">Diese Eigenschaft wird im ActiveX-Steuerelement (Msrdp. ocx) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="766df-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="766df-125">Sie wird in der MsTscAx.dll-Bibliothek unterstützt, die im Standard Client (MsTsc.exe) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="766df-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="766df-126">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="766df-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="766df-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="766df-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="766df-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="766df-128">Property value</span></span>

<span data-ttu-id="766df-129">Der Index des Symbols.</span><span class="sxs-lookup"><span data-stu-id="766df-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="766df-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="766df-130">Error codes</span></span>

<span data-ttu-id="766df-131">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="766df-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="766df-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="766df-132">Remarks</span></span>

<span data-ttu-id="766df-133">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="766df-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="766df-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="766df-134">Requirements</span></span>



| <span data-ttu-id="766df-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="766df-135">Requirement</span></span> | <span data-ttu-id="766df-136">Wert</span><span class="sxs-lookup"><span data-stu-id="766df-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="766df-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="766df-137">Minimum supported client</span></span><br/> | <span data-ttu-id="766df-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="766df-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="766df-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="766df-139">Minimum supported server</span></span><br/> | <span data-ttu-id="766df-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="766df-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="766df-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="766df-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="766df-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="766df-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="766df-143">DLL</span><span class="sxs-lookup"><span data-stu-id="766df-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="766df-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="766df-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="766df-145">IID</span><span class="sxs-lookup"><span data-stu-id="766df-145">IID</span></span><br/>                      | <span data-ttu-id="766df-146">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="766df-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="766df-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="766df-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="766df-148">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="766df-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="766df-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="766df-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="766df-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="766df-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="766df-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="766df-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="766df-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="766df-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="766df-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="766df-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="766df-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="766df-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="766df-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="766df-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="766df-156">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="766df-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





