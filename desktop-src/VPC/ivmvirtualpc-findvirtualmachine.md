---
title: Ivmvirtualpc findvirtualmachine-Methode (vpccominterfaces. h)
description: Ruft ein Objekt für virtuelle Maschinen ab, das mit der angeforderten Konfiguration übereinstimmt.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Findvirtualmachine-Methode Virtual PC
- Findvirtualmachine-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, findvirtualmachine-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105201"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="15b97-106">Ivmvirtualpc:: findvirtualmachine-Methode</span><span class="sxs-lookup"><span data-stu-id="15b97-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="15b97-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="15b97-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="15b97-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="15b97-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="15b97-109">Ruft ein Objekt für virtuelle Maschinen ab, das mit der angeforderten Konfiguration übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="15b97-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="15b97-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b97-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="15b97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="15b97-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15b97-112">*ConfigurationName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15b97-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15b97-113">Der Name des virtuellen Computers, der gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="15b97-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="15b97-114">*virtualmachine* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="15b97-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="15b97-115">Ein Zeiger auf ein neues [**ivmvirtualmachine**](ivmvirtualmachine.md) -Objekt, das diesen virtuellen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="15b97-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15b97-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15b97-116">Return value</span></span>

<span data-ttu-id="15b97-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="15b97-117">This method can return one of these values.</span></span>



| <span data-ttu-id="15b97-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="15b97-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="15b97-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15b97-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="15b97-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="15b97-121">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="15b97-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="15b97-122"><dt>**S \_ Falsch**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="15b97-123">Die angegebene Konfiguration wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="15b97-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="15b97-124"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="15b97-125">Der *ConfigurationName* -Parameter ist ungültig, oder *virtualmachine* ist **null**.</span><span class="sxs-lookup"><span data-stu-id="15b97-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="15b97-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="15b97-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="15b97-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="15b97-128"><dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="15b97-129">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="15b97-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15b97-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15b97-130">Remarks</span></span>

<span data-ttu-id="15b97-131">Bei den Namen der virtuellen Computer wird die Groß-/Kleinschreibung nicht beachtet, z. b. "MyVM" und "MyVM" beziehen sich auf denselben virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="15b97-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="15b97-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15b97-132">Requirements</span></span>



| <span data-ttu-id="15b97-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15b97-133">Requirement</span></span> | <span data-ttu-id="15b97-134">Wert</span><span class="sxs-lookup"><span data-stu-id="15b97-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15b97-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15b97-135">Minimum supported client</span></span><br/> | <span data-ttu-id="15b97-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15b97-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15b97-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15b97-137">Minimum supported server</span></span><br/> | <span data-ttu-id="15b97-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="15b97-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="15b97-139">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="15b97-139">End of client support</span></span><br/>    | <span data-ttu-id="15b97-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="15b97-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="15b97-141">Produkt</span><span class="sxs-lookup"><span data-stu-id="15b97-141">Product</span></span><br/>                  | <span data-ttu-id="15b97-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="15b97-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="15b97-143">Header</span><span class="sxs-lookup"><span data-stu-id="15b97-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="15b97-144"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="15b97-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="15b97-145">IID</span><span class="sxs-lookup"><span data-stu-id="15b97-145">IID</span></span><br/>                      | <span data-ttu-id="15b97-146">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="15b97-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="15b97-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15b97-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15b97-148">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="15b97-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

