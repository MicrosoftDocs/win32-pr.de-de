---
title: IMsRdpClientAdvancedSettings2 canautoreconnetct (Eigenschaft)
description: Gibt an, ob das Client Steuerelement automatisch eine Verbindung mit der aktuellen Sitzung herstellen kann, wenn eine Netzwerkverbindung getrennt wird.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Canautoreconnetct-Eigenschaft Remotedesktopdienste
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings2-Schnittstelle
- IMsRdpClientAdvancedSettings2 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings3-Schnittstelle
- IMsRdpClientAdvancedSettings3 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings4-Schnittstelle
- IMsRdpClientAdvancedSettings4 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings5-Schnittstelle
- IMsRdpClientAdvancedSettings5 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings6-Schnittstelle
- IMsRdpClientAdvancedSettings6 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings7-Schnittstelle
- IMsRdpClientAdvancedSettings7 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
- Canautoreconnetct-Eigenschaft Remotedesktopdienste, IMsRdpClientAdvancedSettings8-Schnittstelle
- IMsRdpClientAdvancedSettings8 Interface Remotedesktopdienste, canautoreconnetct (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858662"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="651f6-118">IMsRdpClientAdvancedSettings2:: canautoreconnetct (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="651f6-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="651f6-119">Gibt an, ob das Client Steuerelement automatisch eine Verbindung mit der aktuellen Sitzung herstellen kann, wenn eine Netzwerkverbindung getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="651f6-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="651f6-120">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="651f6-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="651f6-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="651f6-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="651f6-122">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="651f6-122">Property value</span></span>

<span data-ttu-id="651f6-123">Empfängt **Variant \_ true** , wenn das Steuerelement automatisch eine Verbindung herstellen kann, und andernfalls **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="651f6-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="651f6-124">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="651f6-124">Error codes</span></span>

<span data-ttu-id="651f6-125">Gibt **\_ OK** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="651f6-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="651f6-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="651f6-126">Remarks</span></span>

<span data-ttu-id="651f6-127">Situationen, in denen die automatische Verbindungs Wiederherstellung möglicherweise nicht aktiviert ist, sind u. a. solche, in denen ein Administrator die automatische erneute Verbindungs Herstellung mit Gruppenrichtlinien deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="651f6-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="651f6-128">Diese Eigenschaft kann nicht festgelegt werden, wenn das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="651f6-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="651f6-129">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="651f6-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="651f6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="651f6-130">Requirements</span></span>



| <span data-ttu-id="651f6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="651f6-131">Requirement</span></span> | <span data-ttu-id="651f6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="651f6-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="651f6-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="651f6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="651f6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="651f6-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="651f6-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="651f6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="651f6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="651f6-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="651f6-137">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="651f6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="651f6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="651f6-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="651f6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="651f6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="651f6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="651f6-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="651f6-141">IID</span><span class="sxs-lookup"><span data-stu-id="651f6-141">IID</span></span><br/>                      | <span data-ttu-id="651f6-142">IID \_ IMsRdpClientAdvancedSettings2 ist als 9ac42117-2b76-4320-aa44-0e616ab8437b definiert.</span><span class="sxs-lookup"><span data-stu-id="651f6-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="651f6-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="651f6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651f6-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="651f6-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="651f6-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="651f6-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="651f6-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="651f6-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="651f6-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="651f6-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="651f6-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="651f6-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="651f6-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="651f6-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="651f6-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="651f6-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





