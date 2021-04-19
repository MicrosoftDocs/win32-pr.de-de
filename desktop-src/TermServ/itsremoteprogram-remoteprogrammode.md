---
title: "\"Itsremoteprogram\"-remoteprogrammode-Eigenschaft"
description: Der RemoteApp-Modus von Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Remoteprogrammode-Eigenschaft Remotedesktopdienste
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, itsremoteprogram-Schnittstelle
- Itsremoteprogram-Schnittstelle Remotedesktopdienste, remoteprogrammode-Eigenschaft
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, ITSRemoteProgram2-Schnittstelle
- ITSRemoteProgram2 Interface Remotedesktopdienste, remoteprogrammode-Eigenschaft
- Remoteprogrammode-Eigenschaft Remotedesktopdienste, ITSRemoteProgram3-Schnittstelle
- ITSRemoteProgram3 Interface Remotedesktopdienste, remoteprogrammode-Eigenschaft
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337525"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="a0166-110">Itsremoteprogram:: remoteprogrammode-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0166-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="a0166-111">Der RemoteApp-Modus von Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a0166-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="a0166-112">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a0166-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0166-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0166-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="a0166-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a0166-114">Property value</span></span>

<span data-ttu-id="a0166-115">Der RemoteApp-Modus.</span><span class="sxs-lookup"><span data-stu-id="a0166-115">The RemoteApp mode.</span></span> <span data-ttu-id="a0166-116">Wenn der Wert auf **Variant \_ true** festgelegt ist, wird der RemoteApp-Modus aktiviert, und die Remote Sitzung hostet RemoteApp-Programme.</span><span class="sxs-lookup"><span data-stu-id="a0166-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="a0166-117">Wenn der Wert auf **Variant \_ false** (Standardeinstellung) festgelegt ist, ist der RemoteApp-Modus nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a0166-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="a0166-118">Die Remote Sitzung hostet einen Remote Desktop.</span><span class="sxs-lookup"><span data-stu-id="a0166-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0166-119">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a0166-119">Error codes</span></span>

<span data-ttu-id="a0166-120">Gibt bei Erfolg **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a0166-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0166-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0166-121">Requirements</span></span>



| <span data-ttu-id="a0166-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0166-122">Requirement</span></span> | <span data-ttu-id="a0166-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a0166-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0166-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0166-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0166-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0166-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0166-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0166-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0166-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0166-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0166-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a0166-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0166-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0166-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0166-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a0166-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0166-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0166-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0166-132">IID</span><span class="sxs-lookup"><span data-stu-id="a0166-132">IID</span></span><br/>                      | <span data-ttu-id="a0166-133">IID \_ itsremoteprogram ist als FDD029F9-467A-4c49-8529-64B521DBD1B4 definiert.</span><span class="sxs-lookup"><span data-stu-id="a0166-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a0166-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0166-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0166-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="a0166-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="a0166-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="a0166-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="a0166-137">**Itsremoteprogram**</span><span class="sxs-lookup"><span data-stu-id="a0166-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





