---
title: Ivmnetworkadapter attachdevirtualnetwork-Methode (vpccominterfaces. h)
description: Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Attachdevirtualnetwork-Methode Virtual PC
- Attachdevirtualnetwork-Methode Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, attachdevirtualnetwork-Methode
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477187"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="9cb12-106">Ivmnetworkadapter:: attachdevirtualnetwork-Methode</span><span class="sxs-lookup"><span data-stu-id="9cb12-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="9cb12-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9cb12-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9cb12-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9cb12-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9cb12-109">Fügt die Netzwerkschnittstelle an das angegebene virtuelle Netzwerk an.</span><span class="sxs-lookup"><span data-stu-id="9cb12-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb12-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9cb12-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="9cb12-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cb12-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cb12-112">*VirtualNetwork* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9cb12-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cb12-113">Das virtuelle Netzwerk, mit dem diese virtuelle NIC verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="9cb12-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="9cb12-114">Siehe [**ivmvirtualnetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="9cb12-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cb12-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cb12-115">Return value</span></span>

<span data-ttu-id="9cb12-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9cb12-116">This method can return one of these values.</span></span>



| <span data-ttu-id="9cb12-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="9cb12-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="9cb12-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9cb12-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cb12-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="9cb12-120">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9cb12-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="9cb12-121"><dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="9cb12-122">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="9cb12-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="9cb12-123"><dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="9cb12-124">Der-Parameter enthält kein gültiges virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9cb12-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="9cb12-125"><dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Zugriff \_ verweigert)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="9cb12-126">Der Zugriff auf das angeforderte virtuelle Netzwerk wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="9cb12-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="9cb12-127"><dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="9cb12-128">Der virtuelle Computer ist ungültig oder nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9cb12-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="9cb12-129"><dt>**VM \_ E \_ ungültige \_ virtuelle \_ Netzwerk- \_ ID**</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="9cb12-130">Der-Parameter ist kein vorhandenes virtuelles Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9cb12-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="9cb12-131"><dt>**DISP \_ E- \_ Ausnahme**</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="9cb12-132">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9cb12-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="9cb12-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cb12-133">Requirements</span></span>



| <span data-ttu-id="9cb12-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cb12-134">Requirement</span></span> | <span data-ttu-id="9cb12-135">Wert</span><span class="sxs-lookup"><span data-stu-id="9cb12-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb12-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cb12-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9cb12-137">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cb12-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cb12-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cb12-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9cb12-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9cb12-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9cb12-140">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9cb12-140">End of client support</span></span><br/>    | <span data-ttu-id="9cb12-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cb12-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9cb12-142">Produkt</span><span class="sxs-lookup"><span data-stu-id="9cb12-142">Product</span></span><br/>                  | <span data-ttu-id="9cb12-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9cb12-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9cb12-144">Header</span><span class="sxs-lookup"><span data-stu-id="9cb12-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cb12-145"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cb12-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9cb12-146">IID</span><span class="sxs-lookup"><span data-stu-id="9cb12-146">IID</span></span><br/>                      | <span data-ttu-id="9cb12-147">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="9cb12-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="9cb12-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cb12-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb12-149">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="9cb12-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

