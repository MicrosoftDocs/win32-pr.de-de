---
title: IMsRdpClient3 AdvancedSettings4-Eigenschaft
description: Ruft einen Zeiger auf die IMsRdpClientAdvancedSettings3-Schnittstelle ab.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- AdvancedSettings4-Eigenschaft Remotedesktopdienste
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient3-Schnittstelle
- IMsRdpClient3-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
- AdvancedSettings4-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings4-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858718"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="4556b-120">IMsRdpClient3:: AdvancedSettings4-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4556b-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="4556b-121">Ruft einen Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="4556b-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="4556b-122">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4556b-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4556b-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="4556b-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="4556b-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4556b-124">Property value</span></span>

<span data-ttu-id="4556b-125">Zeiger auf die [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4556b-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="4556b-126">Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4556b-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4556b-127">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4556b-127">Error codes</span></span>

<span data-ttu-id="4556b-128">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4556b-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="4556b-129">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="4556b-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4556b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4556b-130">Remarks</span></span>

<span data-ttu-id="4556b-131">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="4556b-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="4556b-132">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4556b-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4556b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4556b-133">Requirements</span></span>



| <span data-ttu-id="4556b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4556b-134">Requirement</span></span> | <span data-ttu-id="4556b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="4556b-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4556b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4556b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4556b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4556b-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4556b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4556b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4556b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4556b-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4556b-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4556b-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4556b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4556b-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4556b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4556b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4556b-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4556b-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4556b-144">IID</span><span class="sxs-lookup"><span data-stu-id="4556b-144">IID</span></span><br/>                      | <span data-ttu-id="4556b-145">IID \_ IMsRdpClient3 ist als 91b7cbc5-a72e-4fa0-9300-d647d7e897ff definiert.</span><span class="sxs-lookup"><span data-stu-id="4556b-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4556b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4556b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4556b-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4556b-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4556b-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4556b-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4556b-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4556b-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4556b-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4556b-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4556b-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4556b-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4556b-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4556b-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4556b-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4556b-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4556b-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="4556b-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





