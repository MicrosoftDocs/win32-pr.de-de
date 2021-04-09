---
title: IMsRdpClient7 AdvancedSettings8-Eigenschaft
description: Ruft ein Objekt ab, das die IMsRdpClientAdvancedSettings7-Schnittstelle unterstützt.
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- AdvancedSettings8-Eigenschaft Remotedesktopdienste
- AdvancedSettings8-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, AdvancedSettings8-Eigenschaft
- AdvancedSettings8-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, AdvancedSettings8-Eigenschaft
- AdvancedSettings8-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, AdvancedSettings8-Eigenschaft
- AdvancedSettings8-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, AdvancedSettings8-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103090"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="c3dc7-112">IMsRdpClient7:: AdvancedSettings8-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c3dc7-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="c3dc7-113">Ruft ein Objekt ab, das die [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3dc7-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="c3dc7-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c3dc7-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3dc7-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3dc7-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="c3dc7-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c3dc7-116">Property value</span></span>

<span data-ttu-id="c3dc7-117">Die Adresse eines [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) -Schnittstellen Zeigers, der das-Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="c3dc7-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3dc7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3dc7-118">Requirements</span></span>



| <span data-ttu-id="c3dc7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3dc7-119">Requirement</span></span> | <span data-ttu-id="c3dc7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c3dc7-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3dc7-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3dc7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c3dc7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3dc7-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="c3dc7-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3dc7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c3dc7-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3dc7-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="c3dc7-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c3dc7-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="c3dc7-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3dc7-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c3dc7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c3dc7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3dc7-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3dc7-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c3dc7-129">IID</span><span class="sxs-lookup"><span data-stu-id="c3dc7-129">IID</span></span><br/>                      | <span data-ttu-id="c3dc7-130">IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.</span><span class="sxs-lookup"><span data-stu-id="c3dc7-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c3dc7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3dc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3dc7-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="c3dc7-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="c3dc7-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="c3dc7-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="c3dc7-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="c3dc7-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="c3dc7-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="c3dc7-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





