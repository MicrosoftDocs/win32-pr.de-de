---
title: Ivmusbdevicecollection Count-Eigenschaft (vpccominterfaces. h)
description: Ruft die Anzahl der USB-Geräte in dieser Sammlung ab.
ms.assetid: 8d17397b-4f4a-475d-99fe-4df0d74fe5a5
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmusbdebug ecollection-Schnittstelle
- Ivmusbdebug Interface Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMUSBDeviceCollection.Count
- IVMUSBDeviceCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5a0c2146df70f0432a19d65daad44ba6f1ec372
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477049"
---
# <a name="ivmusbdevicecollectioncount-property"></a><span data-ttu-id="1caf0-106">Ivmusbdebug:: count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1caf0-106">IVMUSBDeviceCollection::Count property</span></span>

<span data-ttu-id="1caf0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1caf0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1caf0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1caf0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1caf0-109">Ruft die Anzahl der USB-Geräte in dieser Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="1caf0-109">Retrieves the number of USB devices in this collection.</span></span>

<span data-ttu-id="1caf0-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1caf0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caf0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1caf0-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="1caf0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1caf0-112">Property value</span></span>

<span data-ttu-id="1caf0-113">Die Anzahl der USB-Geräte.</span><span class="sxs-lookup"><span data-stu-id="1caf0-113">The number of USB devices.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1caf0-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="1caf0-114">Error codes</span></span>



| <span data-ttu-id="1caf0-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="1caf0-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1caf0-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1caf0-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1caf0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1caf0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1caf0-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1caf0-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1caf0-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1caf0-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1caf0-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1caf0-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1caf0-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1caf0-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1caf0-122">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="1caf0-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1caf0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1caf0-123">Requirements</span></span>



| <span data-ttu-id="1caf0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1caf0-124">Requirement</span></span> | <span data-ttu-id="1caf0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1caf0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1caf0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1caf0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1caf0-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1caf0-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1caf0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1caf0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1caf0-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1caf0-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1caf0-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1caf0-130">End of client support</span></span><br/>    | <span data-ttu-id="1caf0-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1caf0-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1caf0-132">Produkt</span><span class="sxs-lookup"><span data-stu-id="1caf0-132">Product</span></span><br/>                  | <span data-ttu-id="1caf0-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1caf0-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1caf0-134">Header</span><span class="sxs-lookup"><span data-stu-id="1caf0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1caf0-135"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1caf0-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1caf0-136">IID</span><span class="sxs-lookup"><span data-stu-id="1caf0-136">IID</span></span><br/>                      | <span data-ttu-id="1caf0-137">IID \_ ivmusbdevicecollection ist als 4f-cd6a5--ID definiert. d1c-9s4d-e90abb8b3749</span><span class="sxs-lookup"><span data-stu-id="1caf0-137">IID\_IVMUSBDeviceCollection is defined as 4FBCD6A5-F53C-4d1c-9F4D-E90ABB8B3749</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="1caf0-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1caf0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1caf0-139">**Ivmusbde vicecollection**</span><span class="sxs-lookup"><span data-stu-id="1caf0-139">**IVMUSBDeviceCollection**</span></span>](ivmusbdevicecollection.md)
</dt> </dl>

 

