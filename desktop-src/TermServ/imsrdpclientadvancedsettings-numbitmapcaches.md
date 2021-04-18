---
title: Imsrdpclientadvancedsettings-Eigenschaft numbitmapcaches
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings-Eigenschaft numbitmapcaches
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- Numbitmapcaches-Eigenschaft Remotedesktopdienste
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, numbitmapcaches-Eigenschaft
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
- Numbitmapcaches-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, numbitmapcaches (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354322"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="d6dc4-121">Imsrdpclientadvancedsettings:: numbitmapcaches (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d6dc4-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="d6dc4-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-122">This property is not supported.</span></span>

<span data-ttu-id="d6dc4-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dc4-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6dc4-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="d6dc4-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d6dc4-125">Property value</span></span>

<span data-ttu-id="d6dc4-126">Die neue Anzahl von Caches.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-126">The new number of caches.</span></span> <span data-ttu-id="d6dc4-127">Der Standardwert ist 3. Dies führt zu einer optimalen Leistung.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6dc4-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d6dc4-128">Error codes</span></span>

<span data-ttu-id="d6dc4-129">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6dc4-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6dc4-130">Remarks</span></span>

<span data-ttu-id="d6dc4-131">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d6dc4-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6dc4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6dc4-132">Requirements</span></span>



| <span data-ttu-id="d6dc4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6dc4-133">Requirement</span></span> | <span data-ttu-id="d6dc4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d6dc4-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dc4-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6dc4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dc4-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6dc4-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d6dc4-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6dc4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dc4-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6dc4-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d6dc4-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d6dc4-139">End of client support</span></span><br/>    | <span data-ttu-id="d6dc4-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6dc4-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d6dc4-141">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="d6dc4-141">End of server support</span></span><br/>    | <span data-ttu-id="d6dc4-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6dc4-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d6dc4-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d6dc4-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6dc4-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6dc4-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d6dc4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d6dc4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6dc4-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6dc4-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d6dc4-147">IID</span><span class="sxs-lookup"><span data-stu-id="d6dc4-147">IID</span></span><br/>                      | <span data-ttu-id="d6dc4-148">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="d6dc4-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6dc4-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6dc4-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dc4-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d6dc4-157">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="d6dc4-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





