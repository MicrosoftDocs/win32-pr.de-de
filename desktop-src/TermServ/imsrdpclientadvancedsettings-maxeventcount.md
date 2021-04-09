---
title: Imsrdpclientadvancedsettings maxeventcount (Eigenschaft)
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings maxeventcount (Eigenschaft)
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- maxeventcount-Eigenschaft Remotedesktopdienste
- maxeventcount-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, maxeventcount-Eigenschaft
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
- maxeventcount-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, maxeventcount (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869776"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="1df61-121">Imsrdpclientadvancedsettings:: maxeventcount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1df61-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="1df61-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1df61-122">This property is not supported.</span></span>

<span data-ttu-id="1df61-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1df61-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1df61-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1df61-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="1df61-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1df61-125">Property value</span></span>

<span data-ttu-id="1df61-126">Die neue Ereignis Anzahl.</span><span class="sxs-lookup"><span data-stu-id="1df61-126">The new event count.</span></span> <span data-ttu-id="1df61-127">Der Standard ist 100.</span><span class="sxs-lookup"><span data-stu-id="1df61-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1df61-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1df61-128">Error codes</span></span>

<span data-ttu-id="1df61-129">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="1df61-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1df61-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1df61-130">Remarks</span></span>

<span data-ttu-id="1df61-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1df61-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1df61-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1df61-132">Requirements</span></span>



| <span data-ttu-id="1df61-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1df61-133">Requirement</span></span> | <span data-ttu-id="1df61-134">Wert</span><span class="sxs-lookup"><span data-stu-id="1df61-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df61-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1df61-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1df61-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1df61-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1df61-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1df61-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1df61-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1df61-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1df61-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1df61-139">End of client support</span></span><br/>    | <span data-ttu-id="1df61-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1df61-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1df61-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1df61-141">End of server support</span></span><br/>    | <span data-ttu-id="1df61-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1df61-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1df61-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1df61-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1df61-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df61-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1df61-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1df61-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1df61-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1df61-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1df61-147">IID</span><span class="sxs-lookup"><span data-stu-id="1df61-147">IID</span></span><br/>                      | <span data-ttu-id="1df61-148">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="1df61-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1df61-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1df61-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df61-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1df61-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1df61-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1df61-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1df61-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1df61-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1df61-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1df61-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1df61-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1df61-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1df61-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1df61-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1df61-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1df61-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1df61-157">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="1df61-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





