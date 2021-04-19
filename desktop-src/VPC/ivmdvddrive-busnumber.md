---
title: Ivmdvddrive busnumber-Eigenschaft (vpccominterfaces. h)
description: Ruft die Busnummer ab, an die dieses Gerät angefügt wird.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Busnumber-Eigenschaft virtueller PC
- Busnumber-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, busnumber-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345314"
---
# <a name="ivmdvddrivebusnumber-property"></a><span data-ttu-id="c2a47-106">Ivmdvddrive:: busnumber (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c2a47-106">IVMDVDDrive::BusNumber property</span></span>

<span data-ttu-id="c2a47-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2a47-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c2a47-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c2a47-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c2a47-109">Ruft die Busnummer ab, an die dieses Gerät angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c2a47-109">Retrieves the bus number to which this device is attached.</span></span>

<span data-ttu-id="c2a47-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2a47-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a47-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a47-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="c2a47-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2a47-112">Property value</span></span>

<span data-ttu-id="c2a47-113">Die Busnummer.</span><span class="sxs-lookup"><span data-stu-id="c2a47-113">The bus number.</span></span> <span data-ttu-id="c2a47-114">Beispielsweise würde dieser Wert auf einem IDE-Bus entweder den primären oder den sekundären Standort darstellen.</span><span class="sxs-lookup"><span data-stu-id="c2a47-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c2a47-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c2a47-115">Error codes</span></span>



| <span data-ttu-id="c2a47-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c2a47-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="c2a47-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c2a47-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2a47-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c2a47-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="c2a47-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a47-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c2a47-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c2a47-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="c2a47-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c2a47-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="c2a47-122"><dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt></span><span class="sxs-lookup"><span data-stu-id="c2a47-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="c2a47-123">Der Busstandort für dieses DVD-Laufwerk wurde nicht ordnungsgemäß initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c2a47-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="c2a47-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c2a47-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="c2a47-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c2a47-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="c2a47-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2a47-126">Requirements</span></span>



| <span data-ttu-id="c2a47-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a47-127">Requirement</span></span> | <span data-ttu-id="c2a47-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a47-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a47-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a47-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a47-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a47-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c2a47-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2a47-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a47-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c2a47-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c2a47-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a47-133">End of client support</span></span><br/>    | <span data-ttu-id="c2a47-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c2a47-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c2a47-135">Produkt</span><span class="sxs-lookup"><span data-stu-id="c2a47-135">Product</span></span><br/>                  | <span data-ttu-id="c2a47-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c2a47-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c2a47-137">Header</span><span class="sxs-lookup"><span data-stu-id="c2a47-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a47-138"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a47-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c2a47-139">IID</span><span class="sxs-lookup"><span data-stu-id="c2a47-139">IID</span></span><br/>                      | <span data-ttu-id="c2a47-140">IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.</span><span class="sxs-lookup"><span data-stu-id="c2a47-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c2a47-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2a47-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a47-142">**Ivmdvddrive**</span><span class="sxs-lookup"><span data-stu-id="c2a47-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

