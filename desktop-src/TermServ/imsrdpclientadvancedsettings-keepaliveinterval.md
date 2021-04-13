---
title: Imsrdpclientadvancedsettings keepAliveInterval (Eigenschaft)
description: Gibt ein Intervall in Millisekunden an, in dem der Client Keep-Alive-Nachrichten an den Server sendet.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- keepaliveingeterval-Eigenschaft Remotedesktopdienste
- keepAliveInterval-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, keepAliveInterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
- keepaliveingeterval-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, keepaliveingeterval-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391738"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="656a2-120">Imsrdpclientadvancedsettings:: keepAliveInterval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="656a2-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="656a2-121">Gibt ein Intervall in Millisekunden an, in dem der Client Keep-Alive-Nachrichten an den Server sendet.</span><span class="sxs-lookup"><span data-stu-id="656a2-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="656a2-122">Eine Gruppenrichtlinien Einstellung, die angibt, ob persistente Clientverbindungen mit dem Server zulässig sind, können diese Eigenschafts Einstellung überschreiben.</span><span class="sxs-lookup"><span data-stu-id="656a2-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="656a2-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="656a2-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="656a2-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="656a2-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="656a2-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="656a2-125">Property value</span></span>

<span data-ttu-id="656a2-126">Das neue Intervall in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="656a2-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="656a2-127">Der Standardwert der-Eigenschaft ist 0 (null), wodurch Keep-Alive-Nachrichten deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="656a2-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="656a2-128">Der minimale gültige Wert dieser Eigenschaft ist 10.000, der 10 Sekunden darstellt.</span><span class="sxs-lookup"><span data-stu-id="656a2-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="656a2-129">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="656a2-129">Error codes</span></span>

<span data-ttu-id="656a2-130">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="656a2-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="656a2-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="656a2-131">Remarks</span></span>

<span data-ttu-id="656a2-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="656a2-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="656a2-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656a2-133">Requirements</span></span>



| <span data-ttu-id="656a2-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="656a2-134">Requirement</span></span> | <span data-ttu-id="656a2-135">Wert</span><span class="sxs-lookup"><span data-stu-id="656a2-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656a2-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="656a2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="656a2-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="656a2-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="656a2-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="656a2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="656a2-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="656a2-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="656a2-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="656a2-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="656a2-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="656a2-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="656a2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="656a2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="656a2-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="656a2-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="656a2-144">IID</span><span class="sxs-lookup"><span data-stu-id="656a2-144">IID</span></span><br/>                      | <span data-ttu-id="656a2-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="656a2-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="656a2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="656a2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656a2-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="656a2-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="656a2-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="656a2-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="656a2-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="656a2-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="656a2-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="656a2-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="656a2-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="656a2-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="656a2-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="656a2-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="656a2-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="656a2-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="656a2-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="656a2-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





