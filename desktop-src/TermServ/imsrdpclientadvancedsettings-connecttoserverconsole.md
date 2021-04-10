---
title: Imsrdpclientadvancedsettings connectdeserverconsole (Eigenschaft)
description: Diese Eigenschaft wird nicht unterstützt. Aufrufe von connectdeserverconsole geben immer \_ false zurück.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, connectdeserverconsole-Eigenschaft
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
- Connectdeserverconsole-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, connectdeserverconsole (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949800"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="480ed-121">Imsrdpclientadvancedsettings:: connectdeserverconsole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="480ed-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="480ed-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="480ed-122">This property is not supported.</span></span> <span data-ttu-id="480ed-123">Aufrufe von **connectdeserverconsole** geben immer **\_ false** zurück.</span><span class="sxs-lookup"><span data-stu-id="480ed-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="480ed-124">Verwenden Sie die Eigenschaft [**connectdeadministrasterserver**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) , um eine Verbindung mit der Sitzung herzustellen, die zu Verwaltungszwecken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="480ed-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="480ed-125">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="480ed-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="480ed-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="480ed-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="480ed-127">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="480ed-127">Property value</span></span>

<span data-ttu-id="480ed-128">Legen Sie diesen Parameter auf **Variant \_ false** fest.</span><span class="sxs-lookup"><span data-stu-id="480ed-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="480ed-129">**Variant \_ TRUE** wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="480ed-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="480ed-130">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="480ed-130">Error codes</span></span>

<span data-ttu-id="480ed-131">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="480ed-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="480ed-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="480ed-132">Remarks</span></span>

<span data-ttu-id="480ed-133">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="480ed-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="480ed-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="480ed-134">Requirements</span></span>



| <span data-ttu-id="480ed-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="480ed-135">Requirement</span></span> | <span data-ttu-id="480ed-136">Wert</span><span class="sxs-lookup"><span data-stu-id="480ed-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="480ed-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="480ed-137">Minimum supported client</span></span><br/> | <span data-ttu-id="480ed-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="480ed-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="480ed-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="480ed-139">Minimum supported server</span></span><br/> | <span data-ttu-id="480ed-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="480ed-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="480ed-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="480ed-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="480ed-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480ed-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="480ed-143">DLL</span><span class="sxs-lookup"><span data-stu-id="480ed-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="480ed-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480ed-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="480ed-145">IID</span><span class="sxs-lookup"><span data-stu-id="480ed-145">IID</span></span><br/>                      | <span data-ttu-id="480ed-146">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="480ed-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="480ed-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="480ed-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480ed-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="480ed-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="480ed-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="480ed-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="480ed-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="480ed-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="480ed-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="480ed-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="480ed-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="480ed-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="480ed-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="480ed-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="480ed-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="480ed-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="480ed-155">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="480ed-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





