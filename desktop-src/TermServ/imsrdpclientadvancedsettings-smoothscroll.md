---
title: Imsrdpclientadvancedsettings-smoothscroll-Eigenschaft
description: Diese Eigenschaft wird nicht unterstützt. | Imsrdpclientadvancedsettings-smoothscroll-Eigenschaft
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- Eigenschaften Remotedesktopdienste "smoothscroll"
- Eigenschaften Remotedesktopdienste von smoothscroll, imsrdpclientadvancedsettings-Schnittstelle
- Imsrdpclientadvancedsettings-Schnittstelle Remotedesktopdienste, smoothscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, gläscroll-Eigenschaft
- Eigenschaften Remotedesktopdienste von smoothscroll, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, gläscroll-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62be8fe85415792116c23b4e12d9ab56fb89e0f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106364334"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a><span data-ttu-id="d4573-121">Imsrdpclientadvancedsettings:: smoothscroll-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d4573-121">IMsRdpClientAdvancedSettings::SmoothScroll property</span></span>

<span data-ttu-id="d4573-122">Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4573-122">This property is not supported.</span></span>

<span data-ttu-id="d4573-123">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d4573-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4573-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4573-124">Syntax</span></span>


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a><span data-ttu-id="d4573-125">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d4573-125">Property value</span></span>

<span data-ttu-id="d4573-126">Legen Sie diesen Parameter auf 0 fest, um den Smooth Scroll-Wert oder einen Wert ungleich 0 (null) zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d4573-126">Set this parameter to 0 to disable smooth scrolling or a nonzero value to enable smooth scrolling.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d4573-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d4573-127">Error codes</span></span>

<span data-ttu-id="d4573-128">Gibt **" \_ false**" zurück.</span><span class="sxs-lookup"><span data-stu-id="d4573-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4573-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4573-129">Requirements</span></span>



| <span data-ttu-id="d4573-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4573-130">Requirement</span></span> | <span data-ttu-id="d4573-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d4573-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4573-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4573-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d4573-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d4573-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4573-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4573-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d4573-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d4573-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4573-136">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d4573-136">End of client support</span></span><br/>    | <span data-ttu-id="d4573-137">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d4573-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d4573-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d4573-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4573-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4573-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d4573-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d4573-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4573-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4573-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d4573-142">IID</span><span class="sxs-lookup"><span data-stu-id="d4573-142">IID</span></span><br/>                      | <span data-ttu-id="d4573-143">IID \_ imsrdpclientadvancedsettings ist als 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2 definiert.</span><span class="sxs-lookup"><span data-stu-id="d4573-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4573-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4573-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4573-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d4573-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d4573-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d4573-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d4573-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d4573-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d4573-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d4573-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d4573-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d4573-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d4573-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d4573-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d4573-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d4573-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d4573-152">**Imsrdpclientadvancedsettings**</span><span class="sxs-lookup"><span data-stu-id="d4573-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





