---
title: IMsRdpClientAdvancedSettings2 maxreconnectattempts (Eigenschaft)
description: Gibt an, wie oft versucht werden soll, während der automatischen erneuten Verbindung erneut eine Verbindung herzustellen.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
- Maxreconnectattempts-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, maxreconnectattempts-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337941"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="5083a-118">IMsRdpClientAdvancedSettings2:: maxreconnectattempts-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5083a-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="5083a-119">Gibt an, wie oft versucht werden soll, während der automatischen erneuten Verbindung erneut eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="5083a-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="5083a-120">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5083a-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5083a-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="5083a-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="5083a-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5083a-122">Property value</span></span>

<span data-ttu-id="5083a-123">Die neue Anzahl der Wiederholungen.</span><span class="sxs-lookup"><span data-stu-id="5083a-123">The new number of retries.</span></span> <span data-ttu-id="5083a-124">Gültige Werte sind 0 bis einschließlich 200.</span><span class="sxs-lookup"><span data-stu-id="5083a-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5083a-125">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="5083a-125">Error codes</span></span>

<span data-ttu-id="5083a-126">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5083a-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5083a-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5083a-127">Remarks</span></span>

<span data-ttu-id="5083a-128">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="5083a-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="5083a-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5083a-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5083a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5083a-130">Requirements</span></span>



| <span data-ttu-id="5083a-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5083a-131">Requirement</span></span> | <span data-ttu-id="5083a-132">Wert</span><span class="sxs-lookup"><span data-stu-id="5083a-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5083a-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5083a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5083a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5083a-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="5083a-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5083a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5083a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5083a-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="5083a-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5083a-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="5083a-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5083a-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5083a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5083a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5083a-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5083a-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="5083a-141">IID</span><span class="sxs-lookup"><span data-stu-id="5083a-141">IID</span></span><br/>                      | <span data-ttu-id="5083a-142">IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.</span><span class="sxs-lookup"><span data-stu-id="5083a-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5083a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5083a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5083a-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5083a-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5083a-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5083a-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5083a-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5083a-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5083a-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5083a-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5083a-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5083a-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5083a-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5083a-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5083a-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5083a-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





