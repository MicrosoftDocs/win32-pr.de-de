---
title: Ivmaccountant diskbyteswritten-Eigenschaft (vpccominterfaces. h)
description: Die Gesamtanzahl der Bytes, die von allen Speicher Controllern für diesen virtuellen Computer geschrieben wurden.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- Diskbyteswritten-Eigenschaft virtueller PC
- Diskbyteswritten-Eigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, diskbyteswritten (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859245"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a><span data-ttu-id="a4cc7-106">Ivmaccountant::D iskbyteswritten-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4cc7-106">IVMAccountant::DiskBytesWritten property</span></span>

<span data-ttu-id="a4cc7-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a4cc7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a4cc7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a4cc7-109">Ruft die Gesamtanzahl der Bytes ab, die von allen Speicher Controllern für diesen virtuellen Computer geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-109">Retrieves the total number of bytes written by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="a4cc7-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4cc7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4cc7-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a><span data-ttu-id="a4cc7-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a4cc7-112">Property value</span></span>

<span data-ttu-id="a4cc7-113">Die gesamte Anzahl der gelesenen Bytes</span><span class="sxs-lookup"><span data-stu-id="a4cc7-113">The total number of bytes.</span></span> <span data-ttu-id="a4cc7-114">Diese Daten werden als **Variante** des Typs **VT \_ Decimal** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a4cc7-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a4cc7-115">Error codes</span></span>



| <span data-ttu-id="a4cc7-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="a4cc7-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a4cc7-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a4cc7-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a4cc7-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4cc7-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a4cc7-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="a4cc7-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a4cc7-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a4cc7-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="a4cc7-122"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a4cc7-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="a4cc7-123">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="a4cc7-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a4cc7-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a4cc7-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="a4cc7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4cc7-126">Remarks</span></span>

<span data-ttu-id="a4cc7-127">Beachten Sie, dass die Datenträger-e/a-Statistiken auf 0 (null) zurückgesetzt werden, wenn ein virtueller Computer hochgefahren, zurückgesetzt oder aus dem gespeicherten Zustand</span><span class="sxs-lookup"><span data-stu-id="a4cc7-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4cc7-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4cc7-128">Requirements</span></span>



| <span data-ttu-id="a4cc7-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4cc7-129">Requirement</span></span> | <span data-ttu-id="a4cc7-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a4cc7-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4cc7-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4cc7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a4cc7-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4cc7-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4cc7-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4cc7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a4cc7-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a4cc7-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a4cc7-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="a4cc7-135">End of client support</span></span><br/>    | <span data-ttu-id="a4cc7-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4cc7-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a4cc7-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="a4cc7-137">Product</span></span><br/>                  | <span data-ttu-id="a4cc7-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a4cc7-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a4cc7-139">Header</span><span class="sxs-lookup"><span data-stu-id="a4cc7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4cc7-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4cc7-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a4cc7-141">IID</span><span class="sxs-lookup"><span data-stu-id="a4cc7-141">IID</span></span><br/>                      | <span data-ttu-id="a4cc7-142">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="a4cc7-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="a4cc7-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4cc7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cc7-144">**Ivmaccountant**</span><span class="sxs-lookup"><span data-stu-id="a4cc7-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

