---
title: Imsrdpclientadvancedsettings-Eigenschaft inputeventsatonce
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings-Eigenschaft inputeventsatonce
ms.assetid: 2f24b2cd-136d-4bde-9808-e5cb02bd7ce8
ms.tgt_platform: multiple
keywords:
- Inputeventsatonce-Eigenschaft Remotedesktopdienste
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
- Inputeventsatonce-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste-Eigenschaft, inputeventsatonce-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.InputEventsAtOnce
- IMsRdpClientAdvancedSettings.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.put_InputEventsAtOnce
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999d00cb706e4fdd4cf0c9ed606c33de4a81e8d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365264"
---
# <a name="imsrdpclientadvancedsettingsinputeventsatonce-property"></a><span data-ttu-id="05502-121">Imsrdpclientadvancedsettings:: inputeventsatonce-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="05502-121">IMsRdpClientAdvancedSettings::InputEventsAtOnce property</span></span>

<span data-ttu-id="05502-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05502-122">This property is not supported.</span></span>

<span data-ttu-id="05502-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="05502-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="05502-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="05502-124">Syntax</span></span>


```C++
HRESULT put_InputEventsAtOnce(
  [in]  LONG inputEventsAtOnce
);

HRESULT get_InputEventsAtOnce(
  [out] LONG *pinputEventsAtOnce
);
```



## <a name="property-value"></a><span data-ttu-id="05502-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="05502-125">Property value</span></span>

<span data-ttu-id="05502-126">Die neue Anzahl von Eingabe Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="05502-126">The new number of input events.</span></span> <span data-ttu-id="05502-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="05502-127">The default is 10.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05502-128">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="05502-128">Error codes</span></span>

<span data-ttu-id="05502-129">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="05502-129">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="05502-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05502-130">Requirements</span></span>



| <span data-ttu-id="05502-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05502-131">Requirement</span></span> | <span data-ttu-id="05502-132">Wert</span><span class="sxs-lookup"><span data-stu-id="05502-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05502-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05502-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05502-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05502-134">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="05502-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05502-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05502-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05502-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="05502-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="05502-137">End of client support</span></span><br/>    | <span data-ttu-id="05502-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05502-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="05502-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="05502-139">End of server support</span></span><br/>    | <span data-ttu-id="05502-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="05502-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="05502-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="05502-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="05502-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05502-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="05502-143">DLL</span><span class="sxs-lookup"><span data-stu-id="05502-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05502-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05502-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="05502-145">IID</span><span class="sxs-lookup"><span data-stu-id="05502-145">IID</span></span><br/>                      | <span data-ttu-id="05502-146">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="05502-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05502-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05502-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05502-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="05502-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="05502-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="05502-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="05502-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="05502-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="05502-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="05502-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="05502-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="05502-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="05502-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="05502-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="05502-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="05502-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="05502-155">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="05502-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





