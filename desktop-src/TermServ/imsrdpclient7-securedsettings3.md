---
title: IMsRdpClient7 SecuredSettings3-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientSecuredSettings2-Schnittstelle unterstützt.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- SecuredSettings3-Eigenschaft Remotedesktopdienste
- SecuredSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, SecuredSettings3-Eigenschaft
- SecuredSettings3-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, SecuredSettings3-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391678"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="164e2-112">IMsRdpClient7:: SecuredSettings3-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="164e2-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="164e2-113">Ruft ein Objekt ab, das die [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="164e2-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="164e2-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="164e2-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="164e2-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="164e2-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="164e2-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="164e2-116">Property value</span></span>

<span data-ttu-id="164e2-117">Die Adresse eines [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) -Schnittstellen Zeigers, der das-Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="164e2-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="164e2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="164e2-118">Requirements</span></span>



| <span data-ttu-id="164e2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="164e2-119">Requirement</span></span> | <span data-ttu-id="164e2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="164e2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="164e2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="164e2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="164e2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="164e2-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="164e2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="164e2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="164e2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="164e2-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="164e2-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="164e2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="164e2-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="164e2-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="164e2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="164e2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="164e2-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="164e2-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="164e2-129">IID</span><span class="sxs-lookup"><span data-stu-id="164e2-129">IID</span></span><br/>                      | <span data-ttu-id="164e2-130">IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.</span><span class="sxs-lookup"><span data-stu-id="164e2-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="164e2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="164e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164e2-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="164e2-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="164e2-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="164e2-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="164e2-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="164e2-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="164e2-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="164e2-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





