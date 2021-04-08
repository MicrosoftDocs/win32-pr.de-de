---
title: IMsRdpClient7 RemoteProgram2-Eigenschaft
description: Ruft ein Objekt ab, das die ITSRemoteProgram2-Schnittstelle unterstützt.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- RemoteProgram2-Eigenschaft Remotedesktopdienste
- RemoteProgram2-Eigenschaften Remotedesktopdienste, IMsRdpClient7-Schnittstelle
- IMsRdpClient7-Schnittstelle Remotedesktopdienste, RemoteProgram2-Eigenschaft
- RemoteProgram2-Eigenschaften Remotedesktopdienste, IMsRdpClient8-Schnittstelle
- IMsRdpClient8-Schnittstelle Remotedesktopdienste, RemoteProgram2-Eigenschaft
- RemoteProgram2-Eigenschaften Remotedesktopdienste, IMsRdpClient9-Schnittstelle
- IMsRdpClient9-Schnittstelle Remotedesktopdienste, RemoteProgram2-Eigenschaft
- RemoteProgram2-Eigenschaften Remotedesktopdienste, IMsRdpClient10-Schnittstelle
- IMsRdpClient10-Schnittstelle Remotedesktopdienste, RemoteProgram2-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949565"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="2b3b3-112">IMsRdpClient7:: RemoteProgram2-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2b3b3-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="2b3b3-113">Ruft ein Objekt ab, das die [**ITSRemoteProgram2**](itsremoteprogram2.md) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2b3b3-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="2b3b3-114">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b3b3-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b3b3-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b3b3-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="2b3b3-116">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2b3b3-116">Property value</span></span>

<span data-ttu-id="2b3b3-117">Die Adresse eines [**ITSRemoteProgram2**](itsremoteprogram2.md) -Schnittstellen Zeigers, der das-Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b3b3-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b3b3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b3b3-118">Requirements</span></span>



| <span data-ttu-id="2b3b3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b3b3-119">Requirement</span></span> | <span data-ttu-id="2b3b3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2b3b3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3b3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b3b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3b3-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b3b3-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="2b3b3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b3b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3b3-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b3b3-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="2b3b3-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2b3b3-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b3b3-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b3b3-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b3b3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2b3b3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b3b3-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b3b3-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b3b3-129">IID</span><span class="sxs-lookup"><span data-stu-id="2b3b3-129">IID</span></span><br/>                      | <span data-ttu-id="2b3b3-130">IID \_ IMsRdpClient7 ist als b2a5b5ce-3461-444a-91d4-add26d070638 definiert.</span><span class="sxs-lookup"><span data-stu-id="2b3b3-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2b3b3-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b3b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3b3-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="2b3b3-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="2b3b3-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="2b3b3-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="2b3b3-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="2b3b3-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="2b3b3-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="2b3b3-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





