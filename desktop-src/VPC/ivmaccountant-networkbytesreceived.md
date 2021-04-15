---
title: Ivmaccountant-networkbytesempfangenschaft (vpccominterfaces. h)
description: Die Gesamtanzahl der Bytes, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- Networkbytesempfangene Eigenschaft virtueller PC
- Networkbytesempfangene Eigenschaft Virtual PC, ivmaccountant-Schnittstelle
- Ivmaccountant Interface Virtual PC, networkbytesempfangenschaft
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e14d7454516ff4e83771744c74f31ee594aa67f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479014"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a><span data-ttu-id="974c0-106">Ivmaccountant:: networkbytesempfangenschaft</span><span class="sxs-lookup"><span data-stu-id="974c0-106">IVMAccountant::NetworkBytesReceived property</span></span>

<span data-ttu-id="974c0-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="974c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="974c0-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="974c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="974c0-109">Ruft die Gesamtanzahl der Bytes ab, die von allen virtuellen Netzwerkadaptern für diesen virtuellen Computer empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="974c0-109">Retrieves the total number of bytes received by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="974c0-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="974c0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="974c0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="974c0-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a><span data-ttu-id="974c0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="974c0-112">Property value</span></span>

<span data-ttu-id="974c0-113">Die Gesamtanzahl der empfangenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="974c0-113">The total number of bytes received.</span></span> <span data-ttu-id="974c0-114">Diese Daten werden als **Variante** des Typs **VT \_ Decimal** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="974c0-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="974c0-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="974c0-115">Error codes</span></span>



| <span data-ttu-id="974c0-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="974c0-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="974c0-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="974c0-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="974c0-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="974c0-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="974c0-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="974c0-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="974c0-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="974c0-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="974c0-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="974c0-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="974c0-122"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="974c0-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="974c0-123">Der virtuelle Computer wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="974c0-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="974c0-124"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="974c0-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="974c0-125">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="974c0-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="974c0-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="974c0-126">Remarks</span></span>

<span data-ttu-id="974c0-127">Beachten Sie, dass die Netzwerk-e/a-Statistiken auf Null zurückgesetzt werden, wenn ein virtueller Computer hochgefahren, zurückgesetzt oder aus dem gespeicherten Zustand wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="974c0-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="974c0-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="974c0-128">Requirements</span></span>



| <span data-ttu-id="974c0-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="974c0-129">Requirement</span></span> | <span data-ttu-id="974c0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="974c0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="974c0-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="974c0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="974c0-132">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="974c0-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="974c0-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="974c0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="974c0-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="974c0-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="974c0-135">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="974c0-135">End of client support</span></span><br/>    | <span data-ttu-id="974c0-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="974c0-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="974c0-137">Produkt</span><span class="sxs-lookup"><span data-stu-id="974c0-137">Product</span></span><br/>                  | <span data-ttu-id="974c0-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="974c0-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="974c0-139">Header</span><span class="sxs-lookup"><span data-stu-id="974c0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="974c0-140"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="974c0-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="974c0-141">IID</span><span class="sxs-lookup"><span data-stu-id="974c0-141">IID</span></span><br/>                      | <span data-ttu-id="974c0-142">IID \_ ivmaccountant ist als 6376c067-7b57-4d63-B754-06e2e4f 51d73 definiert.</span><span class="sxs-lookup"><span data-stu-id="974c0-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="974c0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="974c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="974c0-144">**Ivmaccountant**</span><span class="sxs-lookup"><span data-stu-id="974c0-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

