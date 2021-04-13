---
title: Ivmvirtualmachine removenetworkadapter-Methode (vpccominterfaces. h)
description: Entfernt eine Netzwerkschnittstelle von der virtuellen Maschine.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Removenetworkadapter-Methode Virtual PC
- Removenetworkadapter-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, removenetworkadapter-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478348"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="eabbe-106">Ivmvirtualmachine:: removenetworkadapter-Methode</span><span class="sxs-lookup"><span data-stu-id="eabbe-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="eabbe-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eabbe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="eabbe-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="eabbe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="eabbe-109">Entfernt eine Netzwerkschnittstelle von der virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="eabbe-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="eabbe-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="eabbe-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="eabbe-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="eabbe-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eabbe-112">*Network Adapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eabbe-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eabbe-113">Ein [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt, das den zu entfernenden Netzwerkadapter darstellt.</span><span class="sxs-lookup"><span data-stu-id="eabbe-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eabbe-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eabbe-114">Return value</span></span>

<span data-ttu-id="eabbe-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eabbe-115">This method can return one of these values.</span></span>



| <span data-ttu-id="eabbe-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="eabbe-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="eabbe-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eabbe-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="eabbe-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="eabbe-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="eabbe-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="eabbe-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="eabbe-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="eabbe-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="eabbe-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="eabbe-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="eabbe-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="eabbe-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="eabbe-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="eabbe-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="eabbe-124"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="eabbe-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="eabbe-125">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="eabbe-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="eabbe-126"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="eabbe-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="eabbe-127">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eabbe-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="eabbe-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eabbe-128">Remarks</span></span>

<span data-ttu-id="eabbe-129">Eine vorhandene Netzwerkschnittstelle kann nur von einer virtuellen Maschine entfernt werden, die angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="eabbe-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="eabbe-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eabbe-130">Requirements</span></span>



| <span data-ttu-id="eabbe-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eabbe-131">Requirement</span></span> | <span data-ttu-id="eabbe-132">Wert</span><span class="sxs-lookup"><span data-stu-id="eabbe-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eabbe-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eabbe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eabbe-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eabbe-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eabbe-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eabbe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eabbe-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eabbe-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="eabbe-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="eabbe-137">End of client support</span></span><br/>    | <span data-ttu-id="eabbe-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="eabbe-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="eabbe-139">Produkt</span><span class="sxs-lookup"><span data-stu-id="eabbe-139">Product</span></span><br/>                  | <span data-ttu-id="eabbe-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="eabbe-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="eabbe-141">Header</span><span class="sxs-lookup"><span data-stu-id="eabbe-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="eabbe-142"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="eabbe-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="eabbe-143">IID</span><span class="sxs-lookup"><span data-stu-id="eabbe-143">IID</span></span><br/>                      | <span data-ttu-id="eabbe-144">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="eabbe-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="eabbe-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eabbe-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eabbe-146">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="eabbe-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

