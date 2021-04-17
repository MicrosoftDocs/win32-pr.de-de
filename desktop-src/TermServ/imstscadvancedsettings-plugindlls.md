---
title: Imstscadvancedsettings-plugindlls (Eigenschaft)
description: Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Plugindlls-Eigenschaft Remotedesktopdienste
- Plugindlls-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
- Plugindlls-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, plugindlls (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476743"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="326f9-122">Imstscadvancedsettings::P lugindlls (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="326f9-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="326f9-123">Gibt die Namen der zu ladenden Virtual Channel-Client-DLLs an.</span><span class="sxs-lookup"><span data-stu-id="326f9-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="326f9-124">Client-DLLs für virtuelle Kanäle werden auch als Plug-in-DLLs bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="326f9-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="326f9-125">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="326f9-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="326f9-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="326f9-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="326f9-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="326f9-127">Property value</span></span>

<span data-ttu-id="326f9-128">Durch Trennzeichen getrennte Liste mit den Namen der zu ladenden DLLs des virtuellen Channel-Clients.</span><span class="sxs-lookup"><span data-stu-id="326f9-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="326f9-129">Die DLL-Namen dürfen nur alphanumerische Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="326f9-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="326f9-130">Weitere Informationen zum Format dieser Namen finden Sie unter [DVC-Plug-in-Registrierung](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="326f9-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="326f9-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="326f9-131">Error codes</span></span>

<span data-ttu-id="326f9-132">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="326f9-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="326f9-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="326f9-133">Remarks</span></span>

<span data-ttu-id="326f9-134">Wenn das Steuerelement auf einer Webseite gehostet wird, akzeptiert die **plugindlls** -Eigenschaft aus Sicherheitsgründen nur eine benannte Liste von Client-DLLs für virtuelle Kanäle.</span><span class="sxs-lookup"><span data-stu-id="326f9-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="326f9-135">Das-Steuerelement gibt einen Fehler zurück, wenn ein Dateisystem oder ein UNC-Pfad angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="326f9-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="326f9-136">Virtuelle channelclientdlls, auf die von einer Webseite zugegriffen wird, müssen im Verzeichnis "% windir% \\ system32" installiert sein, da das Remotedesktop ActiveX-Steuerelement nur auf DLL-Dateien an diesem Speicherort zugreift.</span><span class="sxs-lookup"><span data-stu-id="326f9-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="326f9-137">Wenn das Steuerelement nicht auf einer Webseite gehostet wird, ist diese Sicherheits Einschränkung nicht vorhanden, und vollständige Pfade können verwendet werden, um auf virtuelle channelclientdlls zuzugreifen und Sie zu laden, die sich an beliebiger Stelle im Dateisystem befinden.</span><span class="sxs-lookup"><span data-stu-id="326f9-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="326f9-138">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="326f9-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="326f9-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="326f9-139">Requirements</span></span>



| <span data-ttu-id="326f9-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="326f9-140">Requirement</span></span> | <span data-ttu-id="326f9-141">Wert</span><span class="sxs-lookup"><span data-stu-id="326f9-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="326f9-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="326f9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="326f9-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="326f9-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="326f9-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="326f9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="326f9-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="326f9-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="326f9-146">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="326f9-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="326f9-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="326f9-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="326f9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="326f9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="326f9-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="326f9-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="326f9-150">IID</span><span class="sxs-lookup"><span data-stu-id="326f9-150">IID</span></span><br/>                      | <span data-ttu-id="326f9-151">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="326f9-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="326f9-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="326f9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="326f9-153">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="326f9-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="326f9-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="326f9-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="326f9-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="326f9-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="326f9-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="326f9-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="326f9-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="326f9-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="326f9-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="326f9-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="326f9-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="326f9-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="326f9-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="326f9-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="326f9-161">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="326f9-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





