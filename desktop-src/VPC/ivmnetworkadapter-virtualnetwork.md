---
title: Ivmnetworkadapter-VirtualNetwork-Eigenschaft (vpccominterfaces. h)
description: Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- VirtualNetwork-Eigenschaft virtueller PC
- VirtualNetwork-Eigenschaft Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, VirtualNetwork-Eigenschaft
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040046"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="56a30-106">Ivmnetworkadapter:: VirtualNetwork-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56a30-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="56a30-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="56a30-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="56a30-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56a30-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="56a30-109">Ruft das virtuelle Netzwerk ab, an das die Netzwerkschnittstelle angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="56a30-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="56a30-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56a30-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a30-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="56a30-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="56a30-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="56a30-112">Property value</span></span>

<span data-ttu-id="56a30-113">Eine [**ivmvirtualnetwork**](ivmvirtualnetwork.md) -Schnittstelle, die das virtuelle Netzwerk darstellt, an das diese virtuelle Netzwerkschnittstelle angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="56a30-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56a30-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="56a30-114">Error codes</span></span>



| <span data-ttu-id="56a30-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="56a30-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="56a30-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="56a30-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56a30-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="56a30-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="56a30-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="56a30-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="56a30-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="56a30-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="56a30-121"><dt>S \_ Falsch</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="56a30-122">Diese Netzwerkschnittstelle ist nicht verbunden und nicht mit einem virtuellen Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="56a30-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="56a30-123"><dt>VM \_ E \_ ungültige \_ virtuelle \_ Netzwerk- \_ ID</dt> <dt>0xa00400702</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="56a30-124">Diese Schnittstelle ist mit einem virtuellen Netzwerk mit einer ungültigen ID verbunden.</span><span class="sxs-lookup"><span data-stu-id="56a30-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="56a30-125"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="56a30-126">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="56a30-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="56a30-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56a30-127">Requirements</span></span>



| <span data-ttu-id="56a30-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56a30-128">Requirement</span></span> | <span data-ttu-id="56a30-129">Wert</span><span class="sxs-lookup"><span data-stu-id="56a30-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="56a30-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56a30-130">Minimum supported client</span></span><br/> | <span data-ttu-id="56a30-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56a30-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56a30-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56a30-132">Minimum supported server</span></span><br/> | <span data-ttu-id="56a30-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="56a30-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="56a30-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="56a30-134">End of client support</span></span><br/>    | <span data-ttu-id="56a30-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56a30-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="56a30-136">Produkt</span><span class="sxs-lookup"><span data-stu-id="56a30-136">Product</span></span><br/>                  | <span data-ttu-id="56a30-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="56a30-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="56a30-138">Header</span><span class="sxs-lookup"><span data-stu-id="56a30-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a30-139"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a30-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="56a30-140">IID</span><span class="sxs-lookup"><span data-stu-id="56a30-140">IID</span></span><br/>                      | <span data-ttu-id="56a30-141">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="56a30-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="56a30-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56a30-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a30-143">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="56a30-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

