---
title: IMsRdpClient6 AdvancedSettings7-Eigenschaft
description: Ruft die IMsRdpClientAdvancedSettings6-Schnittstelle ab.
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- AdvancedSettings7-Eigenschaft Remotedesktopdienste
- AdvancedSettings7-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, AdvancedSettings7-Eigenschaft
- AdvancedSettings7-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings7-Eigenschaft
- AdvancedSettings7-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings7-Eigenschaft
- AdvancedSettings7-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings7-Eigenschaft
- AdvancedSettings7-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings7-Eigenschaft
- AdvancedSettings7-Eigenschaft Remotedesktopdienste, MsRdpClient6-Objekt
- MsRdpClient6-Objekt Remotedesktopdienste, AdvancedSettings7-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391679"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="d0319-116">IMsRdpClient6:: AdvancedSettings7-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d0319-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="d0319-117">Ruft die [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="d0319-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="d0319-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d0319-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0319-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0319-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="d0319-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d0319-120">Property value</span></span>

<span data-ttu-id="d0319-121">Ein [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d0319-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0319-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0319-122">Requirements</span></span>



| <span data-ttu-id="d0319-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0319-123">Requirement</span></span> | <span data-ttu-id="d0319-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d0319-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0319-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0319-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0319-126">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="d0319-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="d0319-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0319-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0319-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0319-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d0319-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d0319-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0319-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0319-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0319-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d0319-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0319-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0319-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0319-133">IID</span><span class="sxs-lookup"><span data-stu-id="d0319-133">IID</span></span><br/>                      | <span data-ttu-id="d0319-134">IID \_ IMsRdpClient6 ist als d43b7d80-8517-4b6d-9eac-96ad6800d7f2 definiert.</span><span class="sxs-lookup"><span data-stu-id="d0319-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0319-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0319-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0319-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d0319-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d0319-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d0319-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d0319-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d0319-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d0319-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d0319-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d0319-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d0319-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





