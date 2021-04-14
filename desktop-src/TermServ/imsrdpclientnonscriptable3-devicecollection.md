---
title: IMsRdpClientNonScriptable3-Eigenschaft "tvicecollection"
description: Ruft die Auflistung von Plug & Play (PNP)-Geräte Objekten ab, die umgeleitet werden sollen.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Die Eigenschaft "tvicecollection" Remotedesktopdienste
- Eigenschaften Remotedesktopdienste von "tvicecollection", IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3-Schnittstelle Remotedesktopdienste, Eigenschaft "tvicecollection"
- Eigenschaften Remotedesktopdienste von "tvicecollection", IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4-Schnittstelle Remotedesktopdienste, Eigenschaft "tvicecollection"
- Eigenschaften Remotedesktopdienste von "tvicecollection", IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5-Schnittstelle Remotedesktopdienste, Eigenschaft "tvicecollection"
- Die Eigenschaft "tvicecollection" Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, Eigenschaft "tvicecollection"
- Die Eigenschaft "tvicecollection" Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, Eigenschaft "tvicecollection"
- Die Eigenschaft "tvicecollection" Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, Eigenschaft "tvicecollection"
- Die Eigenschaft "tvicecollection" Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, Eigenschaft "tvicecollection"
- Die Eigenschaft "tvicecollection" Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, Eigenschaft "tvicecollection"
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391672"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="8eb68-120">IMsRdpClientNonScriptable3::D evicecollection-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8eb68-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="8eb68-121">Ruft die Auflistung von Plug & Play (PNP)-Geräte Objekten ab, die umgeleitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8eb68-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="8eb68-122">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8eb68-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb68-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb68-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="8eb68-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8eb68-124">Property value</span></span>

<span data-ttu-id="8eb68-125">Ruft die Auflistung von PNP-Geräte Objekten vom Typ [**imsrdpdevice**](imsrdpdevice.md)ab.</span><span class="sxs-lookup"><span data-stu-id="8eb68-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb68-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eb68-126">Requirements</span></span>



| <span data-ttu-id="8eb68-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eb68-127">Requirement</span></span> | <span data-ttu-id="8eb68-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8eb68-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb68-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eb68-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8eb68-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8eb68-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="8eb68-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eb68-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8eb68-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8eb68-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="8eb68-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8eb68-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="8eb68-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb68-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8eb68-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8eb68-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eb68-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eb68-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="8eb68-137">IID</span><span class="sxs-lookup"><span data-stu-id="8eb68-137">IID</span></span><br/>                      | <span data-ttu-id="8eb68-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="8eb68-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eb68-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eb68-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb68-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8eb68-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="8eb68-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8eb68-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8eb68-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="8eb68-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





