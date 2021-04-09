---
title: Ivmvirtualmachine-Buchhaltungs Eigenschaft (vpccominterfaces. h)
description: Ruft einen Buchhalter für diesen virtuellen Computer ab.
ms.assetid: 5e512b83-8630-46ee-b521-c8a8193727f5
keywords:
- Buchhaltungs Eigenschaft virtueller PC
- Buchhaltungs Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, Buchhaltungs Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Accountant
- IVMVirtualMachine.get_Accountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af1212de041b1d4c5bda59b9b12ab1d715be67cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106046"
---
# <a name="ivmvirtualmachineaccountant-property"></a><span data-ttu-id="b8a58-106">Ivmvirtualmachine:: Accountant-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b8a58-106">IVMVirtualMachine::Accountant property</span></span>

<span data-ttu-id="b8a58-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8a58-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8a58-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8a58-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8a58-109">Ruft einen Buchhalter für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b8a58-109">Retrieves an accountant for this virtual machine.</span></span>

<span data-ttu-id="b8a58-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b8a58-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a58-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8a58-111">Syntax</span></span>


```C++
HRESULT get_Accountant(
  [out, retval] IVMAccountant **accountant
);
```



## <a name="property-value"></a><span data-ttu-id="b8a58-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b8a58-112">Property value</span></span>

<span data-ttu-id="b8a58-113">Das [**ivmaccountant**](ivmaccountant.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b8a58-113">The [**IVMAccountant**](ivmaccountant.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8a58-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b8a58-114">Error codes</span></span>



| <span data-ttu-id="b8a58-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="b8a58-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b8a58-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b8a58-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b8a58-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b8a58-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b8a58-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8a58-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b8a58-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b8a58-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b8a58-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b8a58-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b8a58-121"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="b8a58-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b8a58-122">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="b8a58-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b8a58-123"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b8a58-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b8a58-124">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="b8a58-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b8a58-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8a58-125">Requirements</span></span>



| <span data-ttu-id="b8a58-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8a58-126">Requirement</span></span> | <span data-ttu-id="b8a58-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b8a58-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a58-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8a58-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a58-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8a58-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8a58-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8a58-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a58-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8a58-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8a58-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b8a58-132">End of client support</span></span><br/>    | <span data-ttu-id="b8a58-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8a58-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8a58-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="b8a58-134">Product</span></span><br/>                  | <span data-ttu-id="b8a58-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8a58-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8a58-136">Header</span><span class="sxs-lookup"><span data-stu-id="b8a58-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a58-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a58-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b8a58-138">IID</span><span class="sxs-lookup"><span data-stu-id="b8a58-138">IID</span></span><br/>                      | <span data-ttu-id="b8a58-139">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="b8a58-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b8a58-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8a58-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a58-141">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="b8a58-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

