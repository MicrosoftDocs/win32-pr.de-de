---
title: Imsrdpclientadvancedsettings-Eigenschaft (maximizeshell)
description: Gibt an, ob Programme, die mit der StartProgram-Eigenschaft gestartet werden, maximiert werden sollen.
ms.assetid: d8c194b6-04ef-495f-a763-7e18064230e6
ms.tgt_platform: multiple
keywords:
- Maximizeshell-Eigenschaft Remotedesktopdienste
- Maximizeshell-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, maximizeshell-Eigenschaft
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
- Maximizeshell-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, maximizeshell (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MaximizeShell
- IMsRdpClientAdvancedSettings.get_MaximizeShell
- IMsRdpClientAdvancedSettings.put_MaximizeShell
- IMsRdpClientAdvancedSettings2.MaximizeShell
- IMsRdpClientAdvancedSettings2.get_MaximizeShell
- IMsRdpClientAdvancedSettings2.put_MaximizeShell
- IMsRdpClientAdvancedSettings3.MaximizeShell
- IMsRdpClientAdvancedSettings3.get_MaximizeShell
- IMsRdpClientAdvancedSettings3.put_MaximizeShell
- IMsRdpClientAdvancedSettings4.MaximizeShell
- IMsRdpClientAdvancedSettings4.get_MaximizeShell
- IMsRdpClientAdvancedSettings4.put_MaximizeShell
- IMsRdpClientAdvancedSettings5.MaximizeShell
- IMsRdpClientAdvancedSettings5.get_MaximizeShell
- IMsRdpClientAdvancedSettings5.put_MaximizeShell
- IMsRdpClientAdvancedSettings6.MaximizeShell
- IMsRdpClientAdvancedSettings6.get_MaximizeShell
- IMsRdpClientAdvancedSettings6.put_MaximizeShell
- IMsRdpClientAdvancedSettings7.MaximizeShell
- IMsRdpClientAdvancedSettings7.get_MaximizeShell
- IMsRdpClientAdvancedSettings7.put_MaximizeShell
- IMsRdpClientAdvancedSettings8.MaximizeShell
- IMsRdpClientAdvancedSettings8.get_MaximizeShell
- IMsRdpClientAdvancedSettings8.put_MaximizeShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c172dd71fcf57f2028f6ba64c93ceaeec2ffb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949631"
---
# <a name="imsrdpclientadvancedsettingsmaximizeshell-property"></a><span data-ttu-id="2ff2d-120">Imsrdpclientadvancedsettings:: maximizeshell-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ff2d-120">IMsRdpClientAdvancedSettings::MaximizeShell property</span></span>

<span data-ttu-id="2ff2d-121">Gibt an, ob Programme, die mit der [**StartProgram**](imstscsecuredsettings-startprogram.md) -Eigenschaft gestartet werden, maximiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-121">Specifies if programs launched with the [**StartProgram**](imstscsecuredsettings-startprogram.md) property should be maximized.</span></span>

<span data-ttu-id="2ff2d-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff2d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ff2d-123">Syntax</span></span>


```C++
HRESULT put_MaximizeShell(
  [in]  LONG maximizeShell
);

HRESULT get_MaximizeShell(
  [out] LONG *pmaximizeShell
);
```



## <a name="property-value"></a><span data-ttu-id="2ff2d-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2ff2d-124">Property value</span></span>

<span data-ttu-id="2ff2d-125">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2ff2d-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2ff2d-126">Error codes</span></span>

<span data-ttu-id="2ff2d-127">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff2d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ff2d-128">Remarks</span></span>

<span data-ttu-id="2ff2d-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2ff2d-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff2d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ff2d-130">Requirements</span></span>



| <span data-ttu-id="2ff2d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ff2d-131">Requirement</span></span> | <span data-ttu-id="2ff2d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2ff2d-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff2d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ff2d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ff2d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ff2d-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2ff2d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ff2d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ff2d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ff2d-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2ff2d-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2ff2d-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ff2d-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2d-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2ff2d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2ff2d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ff2d-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ff2d-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2ff2d-141">IID</span><span class="sxs-lookup"><span data-stu-id="2ff2d-141">IID</span></span><br/>                      | <span data-ttu-id="2ff2d-142">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ff2d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ff2d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff2d-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2ff2d-151">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="2ff2d-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





