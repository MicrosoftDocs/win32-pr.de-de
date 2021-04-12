---
title: Ivmvirtualmachinecollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der virtuellen Computer in dieser Sammlung ab.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmvirtualmachinecollection-Schnittstelle
- Ivmvirtualmachinecollection Interface Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105650"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="a95ee-106">Ivmvirtualmachinecollection:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a95ee-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="a95ee-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a95ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a95ee-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a95ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a95ee-109">Ruft die Anzahl der virtuellen Computer in dieser Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="a95ee-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="a95ee-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a95ee-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a95ee-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a95ee-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="a95ee-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a95ee-112">Property value</span></span>

<span data-ttu-id="a95ee-113">Die Anzahl der virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a95ee-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a95ee-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a95ee-114">Error codes</span></span>



| <span data-ttu-id="a95ee-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a95ee-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a95ee-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a95ee-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a95ee-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a95ee-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a95ee-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a95ee-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a95ee-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a95ee-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a95ee-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a95ee-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="a95ee-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a95ee-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a95ee-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a95ee-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a95ee-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a95ee-123">Requirements</span></span>



| <span data-ttu-id="a95ee-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a95ee-124">Requirement</span></span> | <span data-ttu-id="a95ee-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a95ee-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a95ee-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a95ee-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a95ee-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a95ee-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a95ee-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a95ee-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a95ee-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a95ee-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a95ee-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a95ee-130">End of client support</span></span><br/>    | <span data-ttu-id="a95ee-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a95ee-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="a95ee-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="a95ee-132">Product</span></span><br/>                  | <span data-ttu-id="a95ee-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a95ee-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="a95ee-134">Header</span><span class="sxs-lookup"><span data-stu-id="a95ee-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a95ee-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a95ee-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="a95ee-136">IID</span><span class="sxs-lookup"><span data-stu-id="a95ee-136">IID</span></span><br/>                      | <span data-ttu-id="a95ee-137">IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.</span><span class="sxs-lookup"><span data-stu-id="a95ee-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a95ee-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a95ee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a95ee-139">**Ivmvirtualmachinecollection**</span><span class="sxs-lookup"><span data-stu-id="a95ee-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

