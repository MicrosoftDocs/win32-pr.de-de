---
title: Imsrdpclientadvancedsettings doubleclickdetect (Eigenschaft)
description: Gibt an, ob der Client für den Server Doppelklicks identifiziert.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Doubleclickdetect-Eigenschaft Remotedesktopdienste
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, doubleclickdetect-Eigenschaft
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
- Doubleclickdetect-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, doubleclickdetect (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105867"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="99c7b-120">Imsrdpclientadvancedsettings::D oubleclickdetect-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="99c7b-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="99c7b-121">Gibt an, ob der Client für den Server Doppelklicks identifiziert.</span><span class="sxs-lookup"><span data-stu-id="99c7b-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="99c7b-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="99c7b-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c7b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c7b-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="99c7b-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="99c7b-124">Property value</span></span>

<span data-ttu-id="99c7b-125">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="99c7b-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99c7b-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="99c7b-126">Error codes</span></span>

<span data-ttu-id="99c7b-127">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="99c7b-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c7b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99c7b-128">Remarks</span></span>

<span data-ttu-id="99c7b-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="99c7b-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99c7b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99c7b-130">Requirements</span></span>



| <span data-ttu-id="99c7b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99c7b-131">Requirement</span></span> | <span data-ttu-id="99c7b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="99c7b-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c7b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99c7b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="99c7b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99c7b-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="99c7b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99c7b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="99c7b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99c7b-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="99c7b-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="99c7b-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="99c7b-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c7b-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="99c7b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="99c7b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c7b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c7b-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="99c7b-141">IID</span><span class="sxs-lookup"><span data-stu-id="99c7b-141">IID</span></span><br/>                      | <span data-ttu-id="99c7b-142">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="99c7b-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99c7b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99c7b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c7b-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="99c7b-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="99c7b-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="99c7b-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="99c7b-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="99c7b-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="99c7b-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="99c7b-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="99c7b-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="99c7b-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="99c7b-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="99c7b-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="99c7b-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="99c7b-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="99c7b-151">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="99c7b-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





