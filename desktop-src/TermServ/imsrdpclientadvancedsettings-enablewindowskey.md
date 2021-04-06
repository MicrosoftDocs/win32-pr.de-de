---
title: Imsrdpclientadvancedsettings enablewindowskey (Eigenschaft)
description: Gibt an, ob der Windows-Schlüssel in der Remote Sitzung verwendet werden kann.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Enablewindowskey-Eigenschaft Remotedesktopdienste
- Enablewindowskey-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, enablewindowskey-Eigenschaft
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
- Enablewindowskey-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, enablewindowskey (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743297"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="6322b-120">Imsrdpclientadvancedsettings:: enablewindowskey-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6322b-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="6322b-121">Gibt an, ob der Windows-Schlüssel in der Remote Sitzung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6322b-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="6322b-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6322b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6322b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6322b-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="6322b-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6322b-124">Property value</span></span>

<span data-ttu-id="6322b-125">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6322b-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6322b-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="6322b-126">Error codes</span></span>

<span data-ttu-id="6322b-127">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6322b-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6322b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6322b-128">Remarks</span></span>

<span data-ttu-id="6322b-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6322b-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6322b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6322b-130">Requirements</span></span>



| <span data-ttu-id="6322b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6322b-131">Requirement</span></span> | <span data-ttu-id="6322b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6322b-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6322b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6322b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6322b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6322b-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6322b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6322b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6322b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6322b-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6322b-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6322b-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="6322b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6322b-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6322b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6322b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6322b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6322b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6322b-141">IID</span><span class="sxs-lookup"><span data-stu-id="6322b-141">IID</span></span><br/>                      | <span data-ttu-id="6322b-142">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="6322b-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6322b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6322b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6322b-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6322b-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6322b-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6322b-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6322b-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6322b-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6322b-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6322b-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6322b-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6322b-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6322b-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6322b-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6322b-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6322b-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6322b-151">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="6322b-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





