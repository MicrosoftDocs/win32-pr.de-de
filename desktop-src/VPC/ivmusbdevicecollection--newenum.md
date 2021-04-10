---
title: Ivmusbdevicecollection _NewEnum-Eigenschaft (vpccominterfaces. h)
description: Ruft einen Enumerator für die Auflistung ab. | Ivmusbdevicecollection _NewEnum-Eigenschaft (vpccominterfaces. h)
ms.assetid: f14f64a0-e65a-44d6-b053-54bbcb9ea804
keywords:
- Virtual PC für _NewEnum-Eigenschaft
- _NewEnum Virtual PC-Eigenschaft, ivmusbdebug ecollection-Schnittstelle
- Ivmusbdebug Interface Virtual PC, _NewEnum-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection._NewEnum
- IVMUSBDeviceCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e1e2a4d80691be26161ae4835ccb85c0e722d8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961524"
---
# <a name="ivmusbdevicecollection_newenum-property"></a><span data-ttu-id="2a098-107">Ivmusbdebug:: \_ netwenum-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a098-107">IVMUSBDeviceCollection::\_NewEnum property</span></span>

<span data-ttu-id="2a098-108">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2a098-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a098-109">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a098-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a098-110">Ruft einen Enumerator für die Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="2a098-110">Retrieves an enumerator for the collection.</span></span>

<span data-ttu-id="2a098-111">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2a098-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a098-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a098-112">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="2a098-113">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2a098-113">Property value</span></span>

<span data-ttu-id="2a098-114">Der [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerator.</span><span class="sxs-lookup"><span data-stu-id="2a098-114">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2a098-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="2a098-115">Error codes</span></span>



| <span data-ttu-id="2a098-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="2a098-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2a098-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2a098-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2a098-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a098-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2a098-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a098-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2a098-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2a098-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2a098-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="2a098-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2a098-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2a098-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2a098-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2a098-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2a098-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a098-124">Requirements</span></span>



| <span data-ttu-id="2a098-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a098-125">Requirement</span></span> | <span data-ttu-id="2a098-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2a098-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a098-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a098-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2a098-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a098-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a098-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a098-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2a098-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2a098-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a098-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2a098-131">End of client support</span></span><br/>    | <span data-ttu-id="2a098-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a098-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a098-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="2a098-133">Product</span></span><br/>                  | <span data-ttu-id="2a098-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a098-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a098-135">Header</span><span class="sxs-lookup"><span data-stu-id="2a098-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a098-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a098-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a098-137">IID</span><span class="sxs-lookup"><span data-stu-id="2a098-137">IID</span></span><br/>                      | <span data-ttu-id="2a098-138">IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749</span><span class="sxs-lookup"><span data-stu-id="2a098-138">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="2a098-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a098-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a098-140">**Ivmusbde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="2a098-140">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

