---
title: Ivmvirtualmachine baseboardserialnumber-Eigenschaft (vpccominterfaces. h)
description: Die Seriennummer des Basis Boards.
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- Baseboardserialnumber-Eigenschaft virtueller PC
- Baseboardserialnumber-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, baseboardserialnumber (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a6e239216eb5eadd492cb0a021d9f9c69610342
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391488"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a><span data-ttu-id="e7dd3-106">Ivmvirtualmachine:: baseboardserialnumber-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e7dd3-106">IVMVirtualMachine::BaseBoardSerialNumber property</span></span>

<span data-ttu-id="e7dd3-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e7dd3-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e7dd3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e7dd3-109">Ruft die Seriennummer des Basis Boards ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-109">Retrieves and sets the base board serial number.</span></span>

<span data-ttu-id="e7dd3-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7dd3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7dd3-111">Syntax</span></span>


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="e7dd3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7dd3-112">Property value</span></span>

<span data-ttu-id="e7dd3-113">Gibt die Seriennummer des Basis Boards an.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-113">Specifies the base board serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e7dd3-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="e7dd3-114">Error codes</span></span>



| <span data-ttu-id="e7dd3-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="e7dd3-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="e7dd3-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e7dd3-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7dd3-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="e7dd3-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e7dd3-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="e7dd3-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e7dd3-121"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="e7dd3-122">Der-Parameter ist größer als 32 Zeichen, eine leere Zeichenfolge oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e7dd3-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="e7dd3-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e7dd3-125"><dt>VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_ </dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="e7dd3-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="e7dd3-126">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="e7dd3-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="e7dd3-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="e7dd3-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="e7dd3-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7dd3-129">Remarks</span></span>

<span data-ttu-id="e7dd3-130">Diese Eigenschaft enthält keine gültigen Informationen, bis der virtuelle Computer zum ersten Mal gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="e7dd3-131">Eine leere Zeichenfolge wird zurückgegeben, wenn Sie vor dem ersten Start gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7dd3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7dd3-132">Requirements</span></span>



| <span data-ttu-id="e7dd3-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7dd3-133">Requirement</span></span> | <span data-ttu-id="e7dd3-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e7dd3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7dd3-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7dd3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e7dd3-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7dd3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7dd3-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7dd3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e7dd3-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e7dd3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e7dd3-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="e7dd3-139">End of client support</span></span><br/>    | <span data-ttu-id="e7dd3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7dd3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e7dd3-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="e7dd3-141">Product</span></span><br/>                  | <span data-ttu-id="e7dd3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e7dd3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e7dd3-143">Header</span><span class="sxs-lookup"><span data-stu-id="e7dd3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7dd3-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e7dd3-145">IID</span><span class="sxs-lookup"><span data-stu-id="e7dd3-145">IID</span></span><br/>                      | <span data-ttu-id="e7dd3-146">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="e7dd3-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e7dd3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7dd3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7dd3-148">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="e7dd3-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

