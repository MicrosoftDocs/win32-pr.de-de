---
title: Imsrdpclientadvancedsettings-Eigenschaft (enablemouse)
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings-Eigenschaft (enablemouse)
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- Enablemouse-Eigenschaft Remotedesktopdienste
- Enablemouse-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
- Enablemouse-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, enablemouse-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0495ba7b48e431efe5746f40b353b5c1ad701d6a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961288"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a><span data-ttu-id="0b19d-121">Imsrdpclientadvancedsettings:: enablemouse-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0b19d-121">IMsRdpClientAdvancedSettings::EnableMouse property</span></span>

<span data-ttu-id="0b19d-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0b19d-122">This property is not supported.</span></span>

<span data-ttu-id="0b19d-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0b19d-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b19d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b19d-124">Syntax</span></span>


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a><span data-ttu-id="0b19d-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0b19d-125">Property value</span></span>

<span data-ttu-id="0b19d-126">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0b19d-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b19d-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0b19d-127">Error codes</span></span>

<span data-ttu-id="0b19d-128">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="0b19d-128">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b19d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b19d-129">Remarks</span></span>

<span data-ttu-id="0b19d-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0b19d-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b19d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b19d-131">Requirements</span></span>



| <span data-ttu-id="0b19d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b19d-132">Requirement</span></span> | <span data-ttu-id="0b19d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0b19d-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b19d-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0b19d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0b19d-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b19d-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0b19d-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0b19d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0b19d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b19d-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0b19d-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0b19d-138">End of client support</span></span><br/>    | <span data-ttu-id="0b19d-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b19d-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0b19d-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0b19d-140">End of server support</span></span><br/>    | <span data-ttu-id="0b19d-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0b19d-141">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="0b19d-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="0b19d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b19d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b19d-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0b19d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0b19d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b19d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b19d-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0b19d-146">IID</span><span class="sxs-lookup"><span data-stu-id="0b19d-146">IID</span></span><br/>                      | <span data-ttu-id="0b19d-147">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="0b19d-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b19d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b19d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b19d-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0b19d-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0b19d-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0b19d-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0b19d-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0b19d-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0b19d-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0b19d-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0b19d-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0b19d-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0b19d-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0b19d-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0b19d-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0b19d-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0b19d-156">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="0b19d-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





