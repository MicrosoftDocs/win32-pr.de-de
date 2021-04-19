---
title: Imsrdpclientadvancedsettings dedieredterminal (Eigenschaft)
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings dedieredterminal (Eigenschaft)
ms.assetid: 40d54c88-dcac-4e7d-b389-a65caeb6960e
ms.tgt_platform: multiple
keywords:
- Dedigateway-Terminal Remotedesktopdienste (Eigenschaft)
- Dedigateedterminal-Eigenschaft Remotedesktopdienste, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, dedialisiedterminal-Eigenschaft
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
- Dedialisiedterminal-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, dedialisiedterminal (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DedicatedTerminal
- IMsRdpClientAdvancedSettings.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.DedicatedTerminal
- IMsRdpClientAdvancedSettings2.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.DedicatedTerminal
- IMsRdpClientAdvancedSettings3.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.DedicatedTerminal
- IMsRdpClientAdvancedSettings4.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.DedicatedTerminal
- IMsRdpClientAdvancedSettings5.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.DedicatedTerminal
- IMsRdpClientAdvancedSettings6.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.DedicatedTerminal
- IMsRdpClientAdvancedSettings7.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.DedicatedTerminal
- IMsRdpClientAdvancedSettings8.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.put_DedicatedTerminal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee005439b38e21c5ed05d035545cc5600993cd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353314"
---
# <a name="imsrdpclientadvancedsettingsdedicatedterminal-property"></a><span data-ttu-id="f957d-121">Imsrdpclientadvancedsettings::D EDI| edterminal-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f957d-121">IMsRdpClientAdvancedSettings::DedicatedTerminal property</span></span>

<span data-ttu-id="f957d-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f957d-122">This property is not supported.</span></span>

<span data-ttu-id="f957d-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f957d-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f957d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="f957d-124">Syntax</span></span>


```C++
HRESULT put_DedicatedTerminal(
  [in]  LONG dedicatedTerminal
);

HRESULT get_DedicatedTerminal(
  [out] LONG *pdedicatedTerminal
);
```



## <a name="property-value"></a><span data-ttu-id="f957d-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f957d-125">Property value</span></span>

<span data-ttu-id="f957d-126">Legen Sie diesen Parameter auf 0 fest, um die Funktion zu deaktivieren, oder einen Wert ungleich NULL, um das Feature zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f957d-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f957d-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="f957d-127">Error codes</span></span>

<span data-ttu-id="f957d-128">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="f957d-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f957d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f957d-129">Requirements</span></span>



| <span data-ttu-id="f957d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f957d-130">Requirement</span></span> | <span data-ttu-id="f957d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f957d-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f957d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f957d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f957d-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f957d-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f957d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f957d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f957d-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f957d-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f957d-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="f957d-136">End of client support</span></span><br/>    | <span data-ttu-id="f957d-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f957d-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f957d-138">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="f957d-138">End of server support</span></span><br/>    | <span data-ttu-id="f957d-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f957d-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="f957d-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f957d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f957d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f957d-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f957d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f957d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f957d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f957d-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f957d-144">IID</span><span class="sxs-lookup"><span data-stu-id="f957d-144">IID</span></span><br/>                      | <span data-ttu-id="f957d-145">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="f957d-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f957d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f957d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f957d-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f957d-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f957d-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f957d-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f957d-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f957d-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f957d-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f957d-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f957d-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f957d-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f957d-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f957d-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f957d-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f957d-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f957d-154">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="f957d-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





