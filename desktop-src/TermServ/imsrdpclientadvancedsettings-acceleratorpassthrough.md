---
title: Imsrdpclientadvancedsettings acceleratorpassthrough (Eigenschaft)
description: Gibt an, ob Tastaturbeschleuniger an den Server übermittelt werden sollen.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough
- Beschleunigungs atorpassthrough-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
- Eigenschaften Remotedesktopdienste von acceleratorpassthrough, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, acceleratorpassthrough-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340322"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="e114a-120">Imsrdpclientadvancedsettings:: acceleratorpassthrough (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e114a-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="e114a-121">Gibt an, ob Tastaturbeschleuniger an den Server übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e114a-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="e114a-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e114a-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e114a-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e114a-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="e114a-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e114a-124">Property value</span></span>

<span data-ttu-id="e114a-125">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="e114a-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="e114a-126">Der Standardwert ist ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e114a-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e114a-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e114a-127">Error codes</span></span>

<span data-ttu-id="e114a-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e114a-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e114a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e114a-129">Remarks</span></span>

<span data-ttu-id="e114a-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e114a-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e114a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e114a-131">Requirements</span></span>



| <span data-ttu-id="e114a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e114a-132">Requirement</span></span> | <span data-ttu-id="e114a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e114a-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e114a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e114a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e114a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e114a-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e114a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e114a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e114a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e114a-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e114a-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="e114a-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e114a-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e114a-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e114a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e114a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e114a-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e114a-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e114a-142">IID</span><span class="sxs-lookup"><span data-stu-id="e114a-142">IID</span></span><br/>                      | <span data-ttu-id="e114a-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="e114a-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e114a-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e114a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e114a-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e114a-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e114a-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e114a-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e114a-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e114a-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e114a-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e114a-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e114a-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e114a-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e114a-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e114a-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e114a-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e114a-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e114a-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="e114a-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





