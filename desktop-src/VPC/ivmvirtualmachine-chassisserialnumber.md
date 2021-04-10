---
title: Ivmvirtualmachine chassisserialnumber-Eigenschaft (vpccominterfaces. h)
description: Seriennummer des Chassis.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- Chassisserialnumber-Eigenschaft virtueller PC
- Chassisserialnumber-Eigenschaft Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, chassisserialnumber (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040703"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a><span data-ttu-id="0eeec-106">Ivmvirtualmachine:: chassisserialnumber (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0eeec-106">IVMVirtualMachine::ChassisSerialNumber property</span></span>

<span data-ttu-id="0eeec-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0eeec-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0eeec-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0eeec-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0eeec-109">Ruft die Seriennummer des Chassis ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="0eeec-109">Retrieves and sets the chassis serial number.</span></span>

<span data-ttu-id="0eeec-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0eeec-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eeec-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eeec-111">Syntax</span></span>


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="0eeec-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0eeec-112">Property value</span></span>

<span data-ttu-id="0eeec-113">Gibt die Seriennummer des Chassis an.</span><span class="sxs-lookup"><span data-stu-id="0eeec-113">Specifies the chassis serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0eeec-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="0eeec-114">Error codes</span></span>



| <span data-ttu-id="0eeec-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="0eeec-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="0eeec-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0eeec-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0eeec-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="0eeec-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0eeec-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0eeec-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="0eeec-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="0eeec-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0eeec-121"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="0eeec-122">Der-Parameter ist größer als 32 Zeichen, eine leere Zeichenfolge oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="0eeec-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0eeec-123"><dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="0eeec-124">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="0eeec-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0eeec-125"><dt>VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_ </dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="0eeec-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="0eeec-126">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="0eeec-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="0eeec-127"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="0eeec-128">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0eeec-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="0eeec-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0eeec-129">Remarks</span></span>

<span data-ttu-id="0eeec-130">Diese Eigenschaft enthält keine gültigen Informationen, bis der virtuelle Computer zum ersten Mal gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="0eeec-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="0eeec-131">Eine leere Zeichenfolge wird zurückgegeben, wenn Sie vor dem ersten Start gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="0eeec-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eeec-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0eeec-132">Requirements</span></span>



| <span data-ttu-id="0eeec-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0eeec-133">Requirement</span></span> | <span data-ttu-id="0eeec-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0eeec-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eeec-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0eeec-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0eeec-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0eeec-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0eeec-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0eeec-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0eeec-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0eeec-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0eeec-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0eeec-139">End of client support</span></span><br/>    | <span data-ttu-id="0eeec-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0eeec-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0eeec-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="0eeec-141">Product</span></span><br/>                  | <span data-ttu-id="0eeec-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0eeec-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0eeec-143">Header</span><span class="sxs-lookup"><span data-stu-id="0eeec-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eeec-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eeec-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0eeec-145">IID</span><span class="sxs-lookup"><span data-stu-id="0eeec-145">IID</span></span><br/>                      | <span data-ttu-id="0eeec-146">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="0eeec-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0eeec-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0eeec-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eeec-148">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="0eeec-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

