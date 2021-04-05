---
title: IMsRdpClient5 AdvancedSettings6-Eigenschaft
description: Ruft die IMsRdpClientAdvancedSettings5-Schnittstelle ab.
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- AdvancedSettings6-Eigenschaft Remotedesktopdienste
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
- AdvancedSettings6-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings6-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859263"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="9e1e3-116">IMsRdpClient5:: AdvancedSettings6-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9e1e3-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="9e1e3-117">Ruft die [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9e1e3-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="9e1e3-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9e1e3-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e1e3-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e1e3-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="9e1e3-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9e1e3-120">Property value</span></span>

<span data-ttu-id="9e1e3-121">Ein [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="9e1e3-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e1e3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e1e3-122">Requirements</span></span>



| <span data-ttu-id="9e1e3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e1e3-123">Requirement</span></span> | <span data-ttu-id="9e1e3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9e1e3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1e3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e1e3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e1e3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e1e3-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9e1e3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e1e3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e1e3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e1e3-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9e1e3-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9e1e3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e1e3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e1e3-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e1e3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9e1e3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e1e3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e1e3-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e1e3-133">IID</span><span class="sxs-lookup"><span data-stu-id="9e1e3-133">IID</span></span><br/>                      | <span data-ttu-id="9e1e3-134">IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.</span><span class="sxs-lookup"><span data-stu-id="9e1e3-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="9e1e3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e1e3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1e3-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9e1e3-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9e1e3-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9e1e3-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9e1e3-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9e1e3-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9e1e3-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





