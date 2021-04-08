---
title: Imstscadvancedsettings-Eigenschaft (IconFile)
description: Gibt den Namen der Datei mit den Symbol Daten an, auf die zugegriffen wird, wenn der Client im Vollbildmodus angezeigt wird.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- IconFile-Eigenschaft Remotedesktopdienste
- IconFile-Eigenschaft Remotedesktopdienste, imstscadvancedsettings-Schnittstelle
- Imstscadvancedsettings-Schnittstelle Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, IconFile-Eigenschaft
- IconFile-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, IconFile-Eigenschaft
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741505"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="42a3a-122">Imstscadvancedsettings:: IconFile (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="42a3a-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="42a3a-123">Gibt den Namen der Datei mit den Symbol Daten an, auf die zugegriffen wird, wenn der Client im Vollbildmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42a3a-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="42a3a-124">Diese Eigenschaft wird im ActiveX-Steuerelement (Msrdp. ocx) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42a3a-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="42a3a-125">Sie wird in der MsTscAx.dll-Bibliothek unterstützt, die im Standard Client (MsTsc.exe) enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="42a3a-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="42a3a-126">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="42a3a-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a3a-127">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a3a-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="42a3a-128">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="42a3a-128">Property value</span></span>

<span data-ttu-id="42a3a-129">Der voll qualifizierte Pfad der Symbol Datei oder eine Datei, die Symbol Daten enthält, z. b. eine DLL.</span><span class="sxs-lookup"><span data-stu-id="42a3a-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42a3a-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="42a3a-130">Error codes</span></span>

<span data-ttu-id="42a3a-131">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="42a3a-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a3a-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a3a-132">Remarks</span></span>

<span data-ttu-id="42a3a-133">Die Dateinamenerweiterung einer Symbol Datei lautet ". ico".</span><span class="sxs-lookup"><span data-stu-id="42a3a-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="42a3a-134">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="42a3a-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42a3a-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a3a-135">Requirements</span></span>



| <span data-ttu-id="42a3a-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a3a-136">Requirement</span></span> | <span data-ttu-id="42a3a-137">Wert</span><span class="sxs-lookup"><span data-stu-id="42a3a-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a3a-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a3a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="42a3a-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42a3a-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="42a3a-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a3a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="42a3a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42a3a-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="42a3a-142">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="42a3a-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="42a3a-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a3a-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="42a3a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="42a3a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a3a-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a3a-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="42a3a-146">IID</span><span class="sxs-lookup"><span data-stu-id="42a3a-146">IID</span></span><br/>                      | <span data-ttu-id="42a3a-147">IID \_ imstscadvancedsettings ist als 809945cc-4b3b-4a92-a6b0-DBF 9b5s2ef2d definiert.</span><span class="sxs-lookup"><span data-stu-id="42a3a-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42a3a-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a3a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a3a-149">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="42a3a-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="42a3a-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="42a3a-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="42a3a-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="42a3a-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="42a3a-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="42a3a-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="42a3a-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="42a3a-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="42a3a-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="42a3a-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="42a3a-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="42a3a-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="42a3a-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="42a3a-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="42a3a-157">**Imstscadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="42a3a-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





