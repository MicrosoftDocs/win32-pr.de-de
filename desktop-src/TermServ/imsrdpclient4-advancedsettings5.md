---
title: IMsRdpClient4 AdvancedSettings5-Eigenschaft
description: Ruft einen Zeiger auf eine IMsRdpClientAdvancedSettings4-Schnittstelle ab.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- AdvancedSettings5-Eigenschaft Remotedesktopdienste
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient4-Schnittstelle
- IMsRdpClient4-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
- AdvancedSettings5-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings5-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519019"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="098be-118">IMsRdpClient4:: AdvancedSettings5-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="098be-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="098be-119">Ruft einen Zeiger auf eine [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="098be-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="098be-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="098be-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="098be-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="098be-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="098be-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="098be-122">Property value</span></span>

<span data-ttu-id="098be-123">Ein Zeiger auf die [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="098be-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="098be-124">Die-Schnittstelle kann verwendet werden, um erweiterte Einstellungen für das Client Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="098be-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="098be-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="098be-125">Error codes</span></span>

<span data-ttu-id="098be-126">Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="098be-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="098be-127">Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="098be-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="098be-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="098be-128">Remarks</span></span>

<span data-ttu-id="098be-129">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="098be-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="098be-130">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="098be-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="098be-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="098be-131">Requirements</span></span>



| <span data-ttu-id="098be-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="098be-132">Requirement</span></span> | <span data-ttu-id="098be-133">Wert</span><span class="sxs-lookup"><span data-stu-id="098be-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="098be-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="098be-134">Minimum supported client</span></span><br/> | <span data-ttu-id="098be-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="098be-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="098be-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="098be-136">Minimum supported server</span></span><br/> | <span data-ttu-id="098be-137">Windows Server 2008, Windows Server 2008 mit SP1</span><span class="sxs-lookup"><span data-stu-id="098be-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="098be-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="098be-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="098be-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="098be-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="098be-140">DLL</span><span class="sxs-lookup"><span data-stu-id="098be-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="098be-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="098be-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="098be-142">IID</span><span class="sxs-lookup"><span data-stu-id="098be-142">IID</span></span><br/>                      | <span data-ttu-id="098be-143">IMsRdpClient4 wird als 095e0738-d97d-488b-b9f 6-dd0e8d66c0de definiert.</span><span class="sxs-lookup"><span data-stu-id="098be-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="098be-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="098be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098be-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="098be-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="098be-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="098be-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="098be-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="098be-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="098be-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="098be-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="098be-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="098be-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="098be-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="098be-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="098be-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="098be-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





