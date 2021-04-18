---
title: IMsRdpClient6 TransportSettings2-Eigenschaft
description: Ruft die IMsRdpClientTransportSettings2-Schnittstelle ab.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- TransportSettings2-Eigenschaft Remotedesktopdienste
- TransportSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6-Schnittstelle Remotedesktopdienste, TransportSettings2-Eigenschaft
- TransportSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, TransportSettings2-Eigenschaft
- TransportSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, TransportSettings2-Eigenschaft
- TransportSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings2-Eigenschaft
- TransportSettings2-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings2-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338326"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="6d492-114">IMsRdpClient6:: TransportSettings2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6d492-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="6d492-115">Ruft die [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="6d492-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="6d492-116">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6d492-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d492-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d492-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="6d492-118">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6d492-118">Property value</span></span>

<span data-ttu-id="6d492-119">Ein [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6d492-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d492-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d492-120">Requirements</span></span>



| <span data-ttu-id="6d492-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d492-121">Requirement</span></span> | <span data-ttu-id="6d492-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6d492-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d492-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d492-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6d492-124">Windows Vista mit SP1</span><span class="sxs-lookup"><span data-stu-id="6d492-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="6d492-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d492-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6d492-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d492-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6d492-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6d492-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d492-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d492-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d492-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6d492-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d492-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d492-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d492-131">IID</span><span class="sxs-lookup"><span data-stu-id="6d492-131">IID</span></span><br/>                      | <span data-ttu-id="6d492-132">IID \_ IMsRdpClient6 ist als d43b7d80-8517-4b6d-9eac-96ad6800d7f2 definiert.</span><span class="sxs-lookup"><span data-stu-id="6d492-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6d492-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d492-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d492-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6d492-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6d492-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6d492-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6d492-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6d492-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6d492-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6d492-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6d492-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="6d492-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





