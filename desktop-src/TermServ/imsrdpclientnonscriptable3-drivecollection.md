---
title: IMsRdpClientNonScriptable3 drivecollection (Eigenschaft)
description: Ruft die Auflistung der zu umgeleiteten Laufwerks Objekte ab.
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- Drivecollection-Eigenschaft Remotedesktopdienste
- Drivecollection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable3-Schnittstelle
- IMsRdpClientNonScriptable3 Interface Remotedesktopdienste, drivecollection (Eigenschaft)
- Drivecollection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable4-Schnittstelle
- IMsRdpClientNonScriptable4 Interface Remotedesktopdienste, drivecollection (Eigenschaft)
- Drivecollection-Eigenschaft Remotedesktopdienste, IMsRdpClientNonScriptable5-Schnittstelle
- IMsRdpClientNonScriptable5 Interface Remotedesktopdienste, drivecollection (Eigenschaft)
- Drivecollection-Eigenschaft Remotedesktopdienste, MsRdpClient5-Objekt
- MsRdpClient5-Objekt Remotedesktopdienste, drivecollection-Eigenschaft
- Drivecollection-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, drivecollection-Eigenschaft
- Drivecollection-Eigenschaft Remotedesktopdienste, MsRdpClient7-Objekt
- MsRdpClient7-Objekt Remotedesktopdienste, drivecollection-Eigenschaft
- Drivecollection-Eigenschaft Remotedesktopdienste, MsRdpClient8-Objekt
- MsRdpClient8-Objekt Remotedesktopdienste, drivecollection-Eigenschaft
- Drivecollection-Eigenschaft Remotedesktopdienste, MsRdpClient9-Objekt
- MsRdpClient9-Objekt Remotedesktopdienste, drivecollection-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475783"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="617fe-120">IMsRdpClientNonScriptable3::D rivecollection (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="617fe-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="617fe-121">Ruft die Auflistung der zu umgeleiteten Laufwerks Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="617fe-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="617fe-122">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="617fe-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="617fe-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="617fe-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="617fe-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="617fe-124">Property value</span></span>

<span data-ttu-id="617fe-125">Ruft die Auflistung der Laufwerks Objekte des Typs [**imsrdpdrive**](imsrdpdrive.md)ab.</span><span class="sxs-lookup"><span data-stu-id="617fe-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="617fe-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="617fe-126">Requirements</span></span>



| <span data-ttu-id="617fe-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="617fe-127">Requirement</span></span> | <span data-ttu-id="617fe-128">Wert</span><span class="sxs-lookup"><span data-stu-id="617fe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="617fe-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="617fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="617fe-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="617fe-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="617fe-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="617fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="617fe-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="617fe-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="617fe-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="617fe-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="617fe-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="617fe-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="617fe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="617fe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="617fe-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="617fe-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="617fe-137">IID</span><span class="sxs-lookup"><span data-stu-id="617fe-137">IID</span></span><br/>                      | <span data-ttu-id="617fe-138">IID \_ IMsRdpClientNonScriptable3 ist als b3378d90-0728-45c7-8ed7-b6159fb92219 definiert.</span><span class="sxs-lookup"><span data-stu-id="617fe-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="617fe-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="617fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="617fe-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="617fe-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="617fe-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="617fe-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="617fe-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="617fe-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





