---
title: Imsrdpclientadvancedsettings loadbalanceinfo-Eigenschaft
description: Gibt das Lasten Ausgleichs Cookie an, das in der Verbindungs Sequenz des Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Protokolls in das X. 224-Verbindungs Anforderungspaket eingefügt wird.
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste
- Loadbalanceinfo-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, loadbalanceinfo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
- Loadbalanceingefo-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8-Schnittstelle Remotedesktopdienste, loadbalanceingefo-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391737"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="36093-120">Imsrdpclientadvancedsettings:: loadbalanceinfo-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="36093-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="36093-121">Gibt das Lasten Ausgleichs Cookie an, das in der Verbindungs Sequenz des Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server Protokolls in das X. 224-Verbindungs Anforderungspaket eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="36093-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="36093-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="36093-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="36093-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="36093-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="36093-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="36093-124">Property value</span></span>

<span data-ttu-id="36093-125">Zeiger auf das neue Cookie.</span><span class="sxs-lookup"><span data-stu-id="36093-125">Pointer to the new cookie.</span></span> <span data-ttu-id="36093-126">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="36093-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="36093-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="36093-127">Error codes</span></span>

<span data-ttu-id="36093-128">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="36093-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="36093-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36093-129">Remarks</span></span>

<span data-ttu-id="36093-130">Die Informationen zum Lastenausgleich werden von Lasten Ausgleichs Routern verwendet, um den besten Server für den Client auszuwählen, wenn RD-Sitzungshost Serverfarmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36093-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="36093-131">Der RD-Sitzungshost Server selbst verwendet diese Informationen nicht und verwirft ihn.</span><span class="sxs-lookup"><span data-stu-id="36093-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="36093-132">Das Cookie verwendet die folgende Syntax, wobei die Groß-/Kleinschreibung beachtet wird:</span><span class="sxs-lookup"><span data-stu-id="36093-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="36093-133">**Cookie: MSTS =**_ipaddressandportnumber_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="36093-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="36093-134">Dabei ist " *ipaddressandportnumber* " die IP-Adresse und die Portnummer in der Netzwerk-Byte-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="36093-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="36093-135">Beispielsweise ist das Cookie, das für den Zugriff auf die IP-Adresse von 172.31.249.216 verwendet wird, Portnummer 3389 wie folgt:</span><span class="sxs-lookup"><span data-stu-id="36093-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="36093-136">**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="36093-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="36093-137">Die letzten vier Nullen sind optional und reserviert.</span><span class="sxs-lookup"><span data-stu-id="36093-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="36093-138">Der abschließende Dezimaltrennzeichen ist erforderlich, ebenso wie der nachfolgende Wagen Rücklauf und Zeilenvorschub.</span><span class="sxs-lookup"><span data-stu-id="36093-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="36093-139">Die Länge der Zeichenfolge in Zeichen muss ein gleich Vielfaches von 2 sein. Fügen Sie daher ggf. ein Leerzeichen hinzu.</span><span class="sxs-lookup"><span data-stu-id="36093-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="36093-140">Wenn kein Cookie angegeben ist, lautet der Standardwert **Cookie: mstshash =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="36093-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="36093-141">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="36093-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36093-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36093-142">Requirements</span></span>



| <span data-ttu-id="36093-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36093-143">Requirement</span></span> | <span data-ttu-id="36093-144">Wert</span><span class="sxs-lookup"><span data-stu-id="36093-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36093-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36093-145">Minimum supported client</span></span><br/> | <span data-ttu-id="36093-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36093-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="36093-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36093-147">Minimum supported server</span></span><br/> | <span data-ttu-id="36093-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36093-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="36093-149">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="36093-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="36093-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36093-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="36093-151">DLL</span><span class="sxs-lookup"><span data-stu-id="36093-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36093-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36093-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="36093-153">IID</span><span class="sxs-lookup"><span data-stu-id="36093-153">IID</span></span><br/>                      | <span data-ttu-id="36093-154">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="36093-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36093-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36093-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36093-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="36093-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="36093-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="36093-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="36093-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="36093-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="36093-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="36093-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="36093-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="36093-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="36093-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="36093-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="36093-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="36093-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="36093-163">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="36093-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





