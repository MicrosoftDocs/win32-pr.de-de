---
title: IMsRdpClient7 TransportSettings3-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientTransportSettings3-Schnittstelle unterstützt.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- TransportSettings3-Eigenschaft Remotedesktopdienste
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
- TransportSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, TransportSettings3-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740561"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="26052-112">IMsRdpClient7:: TransportSettings3-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="26052-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="26052-113">Ruft ein Objekt ab, das die [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26052-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="26052-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="26052-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="26052-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="26052-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="26052-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="26052-116">Property value</span></span>

<span data-ttu-id="26052-117">Die Adresse eines [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) -Schnittstellen Zeigers, der das-Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="26052-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="26052-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26052-118">Requirements</span></span>



| <span data-ttu-id="26052-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26052-119">Requirement</span></span> | <span data-ttu-id="26052-120">Wert</span><span class="sxs-lookup"><span data-stu-id="26052-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26052-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26052-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26052-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26052-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="26052-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26052-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26052-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26052-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="26052-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="26052-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="26052-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26052-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="26052-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26052-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26052-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26052-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="26052-129">IID</span><span class="sxs-lookup"><span data-stu-id="26052-129">IID</span></span><br/>                      | <span data-ttu-id="26052-130">IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.</span><span class="sxs-lookup"><span data-stu-id="26052-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="26052-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26052-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26052-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="26052-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="26052-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="26052-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="26052-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="26052-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="26052-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="26052-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





