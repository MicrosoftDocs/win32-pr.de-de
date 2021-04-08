---
title: Ivmhostinfo-netzwerkadaptereigenschaft (vpccominterfaces. h)
description: Ruft eine Aufzähl Bare Auflistung von NICs auf dem Host Computer ab.
ms.assetid: 17393d7a-c883-4d67-826b-83b886c0d7a6
keywords:
- NetworkAdapters-Eigenschaft virtueller PC
- NetworkAdapters-Eigenschaft Virtual PC, ivmhostinfo-Schnittstelle
- Ivmhostinfo Interface Virtual PC, Network Adapters (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHostInfo.NetworkAdapters
- IVMHostInfo.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeff5c6d459fb8f6999f896c3c13fcd980bf70ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949383"
---
# <a name="ivmhostinfonetworkadapters-property"></a><span data-ttu-id="060f6-106">Ivmhostinfo:: NetworkAdapters (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="060f6-106">IVMHostInfo::NetworkAdapters property</span></span>

<span data-ttu-id="060f6-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="060f6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="060f6-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="060f6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="060f6-109">Ruft eine Aufzähl Bare Auflistung von NICs auf dem Host Computer ab.</span><span class="sxs-lookup"><span data-stu-id="060f6-109">Retrieves an enumerable collection of NICs in the host machine.</span></span>

<span data-ttu-id="060f6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="060f6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="060f6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="060f6-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] VARIANT *hostNICs
);
```



## <a name="property-value"></a><span data-ttu-id="060f6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="060f6-112">Property value</span></span>

<span data-ttu-id="060f6-113">Eine Auflistung von Netzwerkschnittstellenkarten.</span><span class="sxs-lookup"><span data-stu-id="060f6-113">A collection of network interface cards.</span></span> <span data-ttu-id="060f6-114">Dies ist ein Array von **BSTR** -Werten.</span><span class="sxs-lookup"><span data-stu-id="060f6-114">This is an array of **BSTR** values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="060f6-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="060f6-115">Error codes</span></span>



| <span data-ttu-id="060f6-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="060f6-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="060f6-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="060f6-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="060f6-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="060f6-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="060f6-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="060f6-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="060f6-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="060f6-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="060f6-121">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="060f6-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="060f6-122"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="060f6-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="060f6-123">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="060f6-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="060f6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="060f6-124">Requirements</span></span>



| <span data-ttu-id="060f6-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="060f6-125">Requirement</span></span> | <span data-ttu-id="060f6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="060f6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="060f6-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="060f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="060f6-128">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="060f6-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="060f6-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="060f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="060f6-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="060f6-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="060f6-131">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="060f6-131">End of client support</span></span><br/>    | <span data-ttu-id="060f6-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="060f6-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="060f6-133">Produkt</span><span class="sxs-lookup"><span data-stu-id="060f6-133">Product</span></span><br/>                  | <span data-ttu-id="060f6-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="060f6-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="060f6-135">Header</span><span class="sxs-lookup"><span data-stu-id="060f6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="060f6-136"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="060f6-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="060f6-137">IID</span><span class="sxs-lookup"><span data-stu-id="060f6-137">IID</span></span><br/>                      | <span data-ttu-id="060f6-138">IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.</span><span class="sxs-lookup"><span data-stu-id="060f6-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="060f6-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="060f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="060f6-140">**Ivmhostinfo**</span><span class="sxs-lookup"><span data-stu-id="060f6-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

