---
title: Methode ' ivmnetworkadapter detachfromvirtualnetwork ' (vpccominterfaces. h)
description: Trennt die Netzwerkschnittstelle von Ihrem virtuellen Netzwerk.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- Detachfromvirtualnetwork-Methode Virtual PC
- Detachfromvirtualnetwork-Methode Virtual PC, ivmnetworkadapter-Schnittstelle
- Ivmnetworkadapter Interface Virtual PC, detachfromvirtualnetwork-Methode
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391985"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="89757-106">Ivmnetworkadapter::D etachfromvirtualnetwork-Methode</span><span class="sxs-lookup"><span data-stu-id="89757-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="89757-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="89757-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="89757-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="89757-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="89757-109">Trennt die Netzwerkschnittstelle von Ihrem virtuellen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="89757-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="89757-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="89757-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="89757-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="89757-111">Parameters</span></span>

<span data-ttu-id="89757-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="89757-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89757-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89757-113">Return value</span></span>

<span data-ttu-id="89757-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="89757-114">This method can return one of these values.</span></span>



| <span data-ttu-id="89757-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="89757-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="89757-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89757-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="89757-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="89757-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="89757-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="89757-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="89757-119"><dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="89757-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="89757-120">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="89757-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="89757-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89757-121">Requirements</span></span>



| <span data-ttu-id="89757-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89757-122">Requirement</span></span> | <span data-ttu-id="89757-123">Wert</span><span class="sxs-lookup"><span data-stu-id="89757-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="89757-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89757-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89757-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89757-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89757-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89757-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89757-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="89757-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="89757-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="89757-128">End of client support</span></span><br/>    | <span data-ttu-id="89757-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="89757-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="89757-130">Produkt</span><span class="sxs-lookup"><span data-stu-id="89757-130">Product</span></span><br/>                  | <span data-ttu-id="89757-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="89757-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="89757-132">Header</span><span class="sxs-lookup"><span data-stu-id="89757-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="89757-133"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="89757-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="89757-134">IID</span><span class="sxs-lookup"><span data-stu-id="89757-134">IID</span></span><br/>                      | <span data-ttu-id="89757-135">IID \_ ivmnetworkadapter ist als e32e4165-22b8-4DC0-8d57-850171ae207a definiert.</span><span class="sxs-lookup"><span data-stu-id="89757-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="89757-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89757-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89757-137">**Ivmnetworkadapter**</span><span class="sxs-lookup"><span data-stu-id="89757-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

