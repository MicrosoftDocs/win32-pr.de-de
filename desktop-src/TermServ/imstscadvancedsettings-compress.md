---
title: Imstscadvancedsettings-Eigenschaft komprimieren
description: Gibt an, ob die Komprimierung aktiviert ist.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
- Eigenschaften Remotedesktopdienste komprimieren, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, Eigenschaft komprimieren
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956670"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="ad794-122">Imstscadvancedsettings:: Compress-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad794-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="ad794-123">Gibt an, ob die Komprimierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ad794-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="ad794-124">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ad794-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad794-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad794-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="ad794-126">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ad794-126">Property value</span></span>

<span data-ttu-id="ad794-127">Legen Sie diesen Parameter auf 0 fest, um die Komprimierung zu deaktivieren oder einen Wert ungleich 0 (null) zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="ad794-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ad794-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ad794-128">Error codes</span></span>

<span data-ttu-id="ad794-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="ad794-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad794-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad794-130">Remarks</span></span>

<span data-ttu-id="ad794-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ad794-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad794-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad794-132">Requirements</span></span>



| <span data-ttu-id="ad794-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad794-133">Requirement</span></span> | <span data-ttu-id="ad794-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ad794-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad794-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad794-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ad794-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad794-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ad794-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad794-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ad794-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad794-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ad794-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ad794-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad794-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad794-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ad794-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ad794-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad794-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad794-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ad794-143">IID</span><span class="sxs-lookup"><span data-stu-id="ad794-143">IID</span></span><br/>                      | <span data-ttu-id="ad794-144">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="ad794-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad794-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad794-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad794-146">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="ad794-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ad794-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ad794-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ad794-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ad794-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="ad794-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ad794-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ad794-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ad794-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ad794-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ad794-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ad794-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ad794-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ad794-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ad794-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ad794-154">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="ad794-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





