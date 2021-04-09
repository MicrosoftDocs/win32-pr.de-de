---
title: Ivmvirtualnetwork-Namenseigenschaft (vpccominterfaces. h)
description: Eindeutiger Name der virtuellen Netzwerk Instanz.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Name-Eigenschaft virtueller PC
- Name-Eigenschaft Virtual PC, ivmvirtualnetwork-Schnittstelle
- Ivmvirtualnetwork Interface Virtual PC, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957019"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="c8ae2-106">Ivmvirtualnetwork:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c8ae2-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="c8ae2-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8ae2-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8ae2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8ae2-109">Ruft den eindeutigen Namen der virtuellen Netzwerk Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="c8ae2-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ae2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8ae2-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="c8ae2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c8ae2-112">Property value</span></span>

<span data-ttu-id="c8ae2-113">Den Namen des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8ae2-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8ae2-114">Error codes</span></span>



| <span data-ttu-id="c8ae2-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="c8ae2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c8ae2-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c8ae2-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8ae2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8ae2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c8ae2-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="c8ae2-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8ae2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c8ae2-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="c8ae2-121"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c8ae2-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c8ae2-122">Es ist ein unerwarteter Fehler aufgetreten, oder die virtuelle Netzwerk Instanz ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8ae2-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8ae2-123">Remarks</span></span>

<span data-ttu-id="c8ae2-124">Bei Namen von virtuellen Netzwerken wird die Groß-/Kleinschreibung nicht beachtet, z. b. "mynetwork" und "mynetwork" beziehen sich auf dasselbe virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ae2-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ae2-125">Requirements</span></span>



| <span data-ttu-id="c8ae2-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ae2-126">Requirement</span></span> | <span data-ttu-id="c8ae2-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ae2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ae2-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ae2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ae2-129">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c8ae2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8ae2-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8ae2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ae2-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8ae2-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8ae2-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c8ae2-132">End of client support</span></span><br/>    | <span data-ttu-id="c8ae2-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8ae2-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8ae2-134">Produkt</span><span class="sxs-lookup"><span data-stu-id="c8ae2-134">Product</span></span><br/>                  | <span data-ttu-id="c8ae2-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8ae2-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8ae2-136">Header</span><span class="sxs-lookup"><span data-stu-id="c8ae2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ae2-137"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ae2-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8ae2-138">IID</span><span class="sxs-lookup"><span data-stu-id="c8ae2-138">IID</span></span><br/>                      | <span data-ttu-id="c8ae2-139">IID \_ ivmvirtualnetwork ist als 431cb7a1-2469-4563-b94e-38b987adca63 definiert.</span><span class="sxs-lookup"><span data-stu-id="c8ae2-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c8ae2-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ae2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ae2-141">**Ivmvirtualnetwork**</span><span class="sxs-lookup"><span data-stu-id="c8ae2-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

