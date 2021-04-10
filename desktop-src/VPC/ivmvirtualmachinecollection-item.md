---
title: Ivmvirtualmachinecollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das virtuelle Maschinen Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmvirtualmachinecollection-Schnittstelle
- Ivmvirtualmachinecollection Interface Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040042"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="d3d48-106">Ivmvirtualmachinecollection:: Item (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d3d48-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="d3d48-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3d48-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3d48-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3d48-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3d48-109">Ruft das virtuelle Maschinen Objekt ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="d3d48-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="d3d48-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d3d48-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d48-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d48-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="d3d48-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d3d48-112">Property value</span></span>

<span data-ttu-id="d3d48-113">Das [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3d48-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3d48-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d3d48-114">Error codes</span></span>



| <span data-ttu-id="d3d48-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="d3d48-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d3d48-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3d48-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3d48-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d3d48-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d3d48-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3d48-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="d3d48-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d3d48-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d3d48-120">Der *virtualmachine* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="d3d48-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="d3d48-121"><dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="d3d48-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="d3d48-122">Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d3d48-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="d3d48-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d3d48-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d3d48-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="d3d48-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="d3d48-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3d48-125">Requirements</span></span>



| <span data-ttu-id="d3d48-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3d48-126">Requirement</span></span> | <span data-ttu-id="d3d48-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d3d48-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d48-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3d48-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d48-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3d48-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3d48-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3d48-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d48-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d3d48-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d3d48-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="d3d48-132">End of client support</span></span><br/>    | <span data-ttu-id="d3d48-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3d48-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="d3d48-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="d3d48-134">Product</span></span><br/>                  | <span data-ttu-id="d3d48-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3d48-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="d3d48-136">Header</span><span class="sxs-lookup"><span data-stu-id="d3d48-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3d48-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d48-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="d3d48-138">IID</span><span class="sxs-lookup"><span data-stu-id="d3d48-138">IID</span></span><br/>                      | <span data-ttu-id="d3d48-139">IID \_ ivmvirtualmachinecollection ist als 59F 31786-2a3d-4sbf-9896-d85338ca0da1 definiert.</span><span class="sxs-lookup"><span data-stu-id="d3d48-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3d48-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3d48-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d48-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="d3d48-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="d3d48-142">**Ivmvirtualmachinecollection**</span><span class="sxs-lookup"><span data-stu-id="d3d48-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

