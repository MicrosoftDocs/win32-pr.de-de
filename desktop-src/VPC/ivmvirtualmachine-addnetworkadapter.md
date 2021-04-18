---
title: Ivmvirtualmachine addnetworkadapter-Methode (vpccominterfaces. h)
description: Fügt der virtuellen Maschine eine Netzwerkschnittstelle hinzu.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Addnetworkadapter-Methode Virtual PC
- Addnetworkadapter-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, addnetworkadapter-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345493"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="39003-106">Ivmvirtualmachine:: addnetworkadapter-Methode</span><span class="sxs-lookup"><span data-stu-id="39003-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="39003-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="39003-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39003-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39003-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39003-109">Fügt der virtuellen Maschine eine Netzwerkschnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="39003-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="39003-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="39003-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="39003-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39003-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39003-112">*Network Adapter* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="39003-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="39003-113">Ein [**ivmnetworkadapter**](ivmnetworkadapter.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="39003-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39003-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39003-114">Return value</span></span>

<span data-ttu-id="39003-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="39003-115">This method can return one of these values.</span></span>



| <span data-ttu-id="39003-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="39003-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="39003-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39003-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="39003-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39003-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="39003-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="39003-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="39003-120"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39003-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="39003-121">Der *NetworkAdapter* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="39003-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="39003-122"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="39003-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="39003-123">Die Konfiguration ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="39003-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="39003-124"><dt>**VM \_ E \_ Pref \_ \_**</dt> unzulässiger Wert <dt>0xa0040301</dt></span><span class="sxs-lookup"><span data-stu-id="39003-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="39003-125">Es können höchstens vier (4) Netzwerkadapter hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="39003-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="39003-126"><dt>**VM \_ E- \_ VM wird \_ ausgeführt \_ oder \_**</dt> <dt>0xa004020b</dt> gespeichert</span><span class="sxs-lookup"><span data-stu-id="39003-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="39003-127">Der virtuelle Computer befindet sich im Zustand "wird ausgeführt" oder "gespeichert".</span><span class="sxs-lookup"><span data-stu-id="39003-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="39003-128"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="39003-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="39003-129">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="39003-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="39003-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39003-130">Remarks</span></span>

<span data-ttu-id="39003-131">Sie können einem beendeten virtuellen Computer nur eine neue Netzwerkschnittstelle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="39003-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="39003-132">Der neu erstellte Netzwerkadapter ist nicht mit einem virtuellen Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="39003-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="39003-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39003-133">Requirements</span></span>



| <span data-ttu-id="39003-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39003-134">Requirement</span></span> | <span data-ttu-id="39003-135">Wert</span><span class="sxs-lookup"><span data-stu-id="39003-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39003-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39003-136">Minimum supported client</span></span><br/> | <span data-ttu-id="39003-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39003-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39003-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39003-138">Minimum supported server</span></span><br/> | <span data-ttu-id="39003-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="39003-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39003-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="39003-140">End of client support</span></span><br/>    | <span data-ttu-id="39003-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39003-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39003-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="39003-142">Product</span></span><br/>                  | <span data-ttu-id="39003-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39003-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39003-144">Header</span><span class="sxs-lookup"><span data-stu-id="39003-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="39003-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39003-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39003-146">IID</span><span class="sxs-lookup"><span data-stu-id="39003-146">IID</span></span><br/>                      | <span data-ttu-id="39003-147">IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.</span><span class="sxs-lookup"><span data-stu-id="39003-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="39003-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39003-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39003-149">**Ivmvirtualmachine**</span><span class="sxs-lookup"><span data-stu-id="39003-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

