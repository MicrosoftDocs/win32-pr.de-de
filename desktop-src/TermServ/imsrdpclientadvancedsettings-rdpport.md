---
title: Imsrdpclientadvancedsettings-RDPport (Eigenschaft)
description: Gibt den Verbindungsport an.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- RDPport-Eigenschaft Remotedesktopdienste
- RDPport-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, RDPport-Eigenschaft
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, RDPport (Eigenschaft)
- RDPport-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, RDPport (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106173"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="e4eab-120">Imsrdpclientadvancedsettings:: RDPport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4eab-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="e4eab-121">Gibt den Verbindungsport an.</span><span class="sxs-lookup"><span data-stu-id="e4eab-121">Specifies the connection port.</span></span>

<span data-ttu-id="e4eab-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e4eab-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4eab-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4eab-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="e4eab-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e4eab-124">Property value</span></span>

<span data-ttu-id="e4eab-125">Der neue Port.</span><span class="sxs-lookup"><span data-stu-id="e4eab-125">The new port.</span></span> <span data-ttu-id="e4eab-126">Der Standardwert ist 3389.</span><span class="sxs-lookup"><span data-stu-id="e4eab-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e4eab-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e4eab-127">Error codes</span></span>

<span data-ttu-id="e4eab-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e4eab-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4eab-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4eab-129">Remarks</span></span>

<span data-ttu-id="e4eab-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e4eab-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4eab-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4eab-131">Requirements</span></span>



| <span data-ttu-id="e4eab-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4eab-132">Requirement</span></span> | <span data-ttu-id="e4eab-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e4eab-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4eab-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4eab-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e4eab-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4eab-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e4eab-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4eab-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e4eab-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4eab-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e4eab-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e4eab-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4eab-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4eab-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e4eab-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e4eab-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4eab-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4eab-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e4eab-142">IID</span><span class="sxs-lookup"><span data-stu-id="e4eab-142">IID</span></span><br/>                      | <span data-ttu-id="e4eab-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="e4eab-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4eab-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4eab-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4eab-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e4eab-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e4eab-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e4eab-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e4eab-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e4eab-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e4eab-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e4eab-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e4eab-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e4eab-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e4eab-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e4eab-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e4eab-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e4eab-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e4eab-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="e4eab-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





