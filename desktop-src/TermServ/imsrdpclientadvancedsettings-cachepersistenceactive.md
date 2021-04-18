---
title: Imsrdpclientadvancedsettings cachepersistenceactive (Eigenschaft)
description: Gibt an, ob das persistente Bitmap-Caching verwendet werden soll. Persistentes zwischenspeichern kann die Leistung verbessern, erfordert jedoch zusätzlichen Speicherplatz.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, cachepersistenceactive-Eigenschaft
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
- Cachepersistenceactive-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, cachepersistenceactive (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344508"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="3d032-121">Imsrdpclientadvancedsettings:: cachepersistenceactive-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3d032-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="3d032-122">Gibt an, ob das persistente Bitmap-Caching verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d032-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="3d032-123">Persistentes zwischenspeichern kann die Leistung verbessern, erfordert jedoch zusätzlichen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="3d032-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="3d032-124">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3d032-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d032-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d032-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="3d032-126">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3d032-126">Property value</span></span>

<span data-ttu-id="3d032-127">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3d032-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d032-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3d032-128">Error codes</span></span>

<span data-ttu-id="3d032-129">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3d032-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d032-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d032-130">Remarks</span></span>

<span data-ttu-id="3d032-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3d032-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d032-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d032-132">Requirements</span></span>



| <span data-ttu-id="3d032-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d032-133">Requirement</span></span> | <span data-ttu-id="3d032-134">Wert</span><span class="sxs-lookup"><span data-stu-id="3d032-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d032-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d032-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3d032-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d032-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3d032-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d032-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3d032-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d032-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3d032-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3d032-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d032-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d032-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d032-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d032-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d032-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d032-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d032-143">IID</span><span class="sxs-lookup"><span data-stu-id="3d032-143">IID</span></span><br/>                      | <span data-ttu-id="3d032-144">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="3d032-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d032-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d032-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d032-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="3d032-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="3d032-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="3d032-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3d032-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="3d032-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="3d032-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3d032-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="3d032-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3d032-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3d032-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3d032-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3d032-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3d032-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3d032-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="3d032-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





