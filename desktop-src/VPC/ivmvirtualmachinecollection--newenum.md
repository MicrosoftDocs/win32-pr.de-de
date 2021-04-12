---
title: Ivmvirtualmachinecollection _NewEnum-Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die Auflistung ab. | Ivmvirtualmachinecollection _NewEnum-Eigenschaft (vpccominterfaces. h)
ms.assetid: 86b51542-139c-4e2b-baec-2c90956d99b3
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum Virtual PC-Eigenschaft, ivmvirtualmachinecollection-Schnittstelle
- Ivmvirtualmachinecollection Interface Virtual PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection._NewEnum
- IVMVirtualMachineCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea610b005ea9482d59de65311256f77446e442cd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353209"
---
# <a name="ivmvirtualmachinecollection_newenum-property"></a><span data-ttu-id="08035-107">Ivmvirtualmachinecollection:: \_ netwenum-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08035-107">IVMVirtualMachineCollection::\_NewEnum property</span></span>

<span data-ttu-id="08035-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08035-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="08035-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="08035-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="08035-110">Ruft einen Enumerator für die Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="08035-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="08035-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="08035-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="08035-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="08035-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="08035-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="08035-113">Property value</span></span>

<span data-ttu-id="08035-114">Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.</span><span class="sxs-lookup"><span data-stu-id="08035-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08035-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="08035-115">Error codes</span></span>



| <span data-ttu-id="08035-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="08035-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="08035-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08035-117">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="08035-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="08035-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="08035-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="08035-119">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="08035-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="08035-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="08035-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="08035-121">The parameter is **NULL**.</span></span><br/>    |
| <dl> <span data-ttu-id="08035-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="08035-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="08035-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="08035-123">An unexpected error occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="08035-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08035-124">Requirements</span></span>



| <span data-ttu-id="08035-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08035-125">Requirement</span></span> | <span data-ttu-id="08035-126">Wert</span><span class="sxs-lookup"><span data-stu-id="08035-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08035-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08035-127">Minimum supported client</span></span><br/> | <span data-ttu-id="08035-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08035-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08035-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08035-129">Minimum supported server</span></span><br/> | <span data-ttu-id="08035-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="08035-130">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="08035-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="08035-131">End of client support</span></span><br/>    | <span data-ttu-id="08035-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="08035-132">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="08035-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="08035-133">Product</span></span><br/>                  | <span data-ttu-id="08035-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="08035-134">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="08035-135">Header</span><span class="sxs-lookup"><span data-stu-id="08035-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="08035-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="08035-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="08035-137">IID</span><span class="sxs-lookup"><span data-stu-id="08035-137">IID</span></span><br/>                      | <span data-ttu-id="08035-138">IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.</span><span class="sxs-lookup"><span data-stu-id="08035-138">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08035-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08035-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08035-140">**Ivmvirtualmachinecollection**</span><span class="sxs-lookup"><span data-stu-id="08035-140">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

