---
title: IMsRdpClient5 TransportSettings (Eigenschaft)
description: Ruft ab, was durch ein Skript an die imsrdpclienttransportsettings-Schnittstelle übermittelt wurde.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
- TransportSettings-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103163"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="5a8f3-116">IMsRdpClient5:: TransportSettings (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a8f3-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="5a8f3-117">Ruft ab, was durch ein Skript an die [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstelle übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="5a8f3-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="5a8f3-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5a8f3-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8f3-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a8f3-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="5a8f3-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5a8f3-120">Property value</span></span>

<span data-ttu-id="5a8f3-121">Ein [**imsrdpclienttransportsettings**](imsrdpclienttransportsettings.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="5a8f3-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a8f3-122">Requirements</span></span>



| <span data-ttu-id="5a8f3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a8f3-123">Requirement</span></span> | <span data-ttu-id="5a8f3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5a8f3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8f3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a8f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8f3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a8f3-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5a8f3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a8f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8f3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a8f3-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5a8f3-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5a8f3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a8f3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a8f3-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a8f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5a8f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a8f3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a8f3-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a8f3-133">IID</span><span class="sxs-lookup"><span data-stu-id="5a8f3-133">IID</span></span><br/>                      | <span data-ttu-id="5a8f3-134">IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.</span><span class="sxs-lookup"><span data-stu-id="5a8f3-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5a8f3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a8f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8f3-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5a8f3-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5a8f3-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5a8f3-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5a8f3-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5a8f3-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="5a8f3-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





