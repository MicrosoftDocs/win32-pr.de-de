---
title: IMsRdpClientNonScriptable3 aushandatesecuritylayer (Eigenschaft)
description: Gibt an oder Ruft ab, ob die Sicherheitsschicht für die Aushandlung für die Verbindung aktiviert ist.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5 Object Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6 Object Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7 Object Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8 Object Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
- Aushandatesecuritylayer-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9 Object Remotedesktopdienste, aushandatesecuritylayer (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338338"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="774a8-120">IMsRdpClientNonScriptable3:: aushandatesecuritylayer (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="774a8-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="774a8-121">Gibt an oder Ruft ab, ob die Sicherheitsschicht für die Aushandlung für die Verbindung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="774a8-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="774a8-122">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="774a8-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="774a8-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="774a8-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="774a8-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="774a8-124">Property value</span></span>

<span data-ttu-id="774a8-125">Gibt an, ob die Aushandlung der Sicherheitsebene aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="774a8-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="774a8-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="774a8-126">Remarks</span></span>

<span data-ttu-id="774a8-127">Wenn diese Eigenschaft auf **Variant \_ false** festgelegt ist und Authentifizierung auf Netzwerkebene (NLA) auf dem Client Betriebssystem aktiviert ist, aushandelt der Client die Sicherheitsschicht nicht und verwendet stattdessen NLA, um die RDP-Verbindung zu sichern.</span><span class="sxs-lookup"><span data-stu-id="774a8-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="774a8-128">Wenn diese Eigenschaft auf **Variant \_ true** festgelegt ist, verhandelt der Client zwischen NLA und grundlegender RDP-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="774a8-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="774a8-129">Die Deaktivierung der sicherheitsebenenaushandlung ist nur möglich, wenn eine Verbindung mit einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) hergestellt wird, auf dem Windows Vista oder höher ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="774a8-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="774a8-130">Wenn diese Eigenschaft aktiviert ist und der Client versucht, eine Verbindung mit einem RD-Sitzungshost Server herzustellen, auf dem ein älteres Betriebssystem ausgeführt wird, tritt bei der Verbindung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="774a8-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="774a8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="774a8-131">Requirements</span></span>



| <span data-ttu-id="774a8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="774a8-132">Requirement</span></span> | <span data-ttu-id="774a8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="774a8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="774a8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="774a8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="774a8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="774a8-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="774a8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="774a8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="774a8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="774a8-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="774a8-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="774a8-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="774a8-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="774a8-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="774a8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="774a8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="774a8-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="774a8-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="774a8-142">IID</span><span class="sxs-lookup"><span data-stu-id="774a8-142">IID</span></span><br/>                      | <span data-ttu-id="774a8-143">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="774a8-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="774a8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="774a8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774a8-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="774a8-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="774a8-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="774a8-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="774a8-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="774a8-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





