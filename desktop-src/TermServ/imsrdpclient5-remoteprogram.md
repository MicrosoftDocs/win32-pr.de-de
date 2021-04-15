---
title: IMsRdpClient5 remoteprogram (Eigenschaft)
description: Ruft ein Objekt ab, das die itsremoteprogram-Schnittstelle unterstützt.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- Remoteprogram-Eigenschaft Remotedesktopdienste
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient5-Schnittstelle
- IMsRdpClient5 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient6-Schnittstelle
- IMsRdpClient6 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
- Remoteprogram-Eigenschaft Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10 Interface Remotedesktopdienste, remoteprogram-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475789"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="56a72-116">IMsRdpClient5:: remoteprogram (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="56a72-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="56a72-117">Ruft ein Objekt ab, das die [**itsremoteprogram**](itsremoteprogram.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56a72-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="56a72-118">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56a72-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a72-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a72-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="56a72-120">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56a72-120">Property value</span></span>

<span data-ttu-id="56a72-121">Ein [**itsremoteprogram**](itsremoteprogram.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="56a72-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a72-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56a72-122">Requirements</span></span>



| <span data-ttu-id="56a72-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56a72-123">Requirement</span></span> | <span data-ttu-id="56a72-124">Wert</span><span class="sxs-lookup"><span data-stu-id="56a72-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a72-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56a72-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56a72-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56a72-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="56a72-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56a72-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56a72-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56a72-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="56a72-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="56a72-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="56a72-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a72-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56a72-131">DLL</span><span class="sxs-lookup"><span data-stu-id="56a72-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a72-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a72-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="56a72-133">IID</span><span class="sxs-lookup"><span data-stu-id="56a72-133">IID</span></span><br/>                      | <span data-ttu-id="56a72-134">IID \_ IMsRdpClient5 ist als 4eb5335b-6429-477d-B922-e06a28ecd8bf definiert.</span><span class="sxs-lookup"><span data-stu-id="56a72-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="56a72-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56a72-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a72-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="56a72-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="56a72-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="56a72-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="56a72-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="56a72-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="56a72-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="56a72-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="56a72-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="56a72-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="56a72-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="56a72-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





