---
title: Imsrdpclientadvancedsettings-Eigenschaft disablectrlaltdel
description: Gibt an, ob der erste erklärende Bildschirm in Winlogon angezeigt werden soll.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
- Disablectrlaltdel-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, disablectrlaltdel-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740560"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="225b3-120">Imsrdpclientadvancedsettings::D isablectrlaltdel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="225b3-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="225b3-121">Gibt an, ob der erste erklärende Bildschirm in Winlogon angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="225b3-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="225b3-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="225b3-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="225b3-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="225b3-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="225b3-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="225b3-124">Property value</span></span>

<span data-ttu-id="225b3-125">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="225b3-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="225b3-126">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="225b3-126">Error codes</span></span>

<span data-ttu-id="225b3-127">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="225b3-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="225b3-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="225b3-128">Remarks</span></span>

<span data-ttu-id="225b3-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="225b3-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="225b3-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="225b3-130">Requirements</span></span>



| <span data-ttu-id="225b3-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="225b3-131">Requirement</span></span> | <span data-ttu-id="225b3-132">Wert</span><span class="sxs-lookup"><span data-stu-id="225b3-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="225b3-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="225b3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="225b3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="225b3-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="225b3-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="225b3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="225b3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="225b3-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="225b3-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="225b3-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="225b3-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="225b3-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="225b3-139">DLL</span><span class="sxs-lookup"><span data-stu-id="225b3-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="225b3-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="225b3-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="225b3-141">IID</span><span class="sxs-lookup"><span data-stu-id="225b3-141">IID</span></span><br/>                      | <span data-ttu-id="225b3-142">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="225b3-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="225b3-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="225b3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="225b3-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="225b3-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="225b3-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="225b3-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="225b3-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="225b3-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="225b3-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="225b3-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="225b3-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="225b3-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="225b3-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="225b3-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="225b3-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="225b3-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="225b3-151">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="225b3-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





